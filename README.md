# dosion-legal

**Source of truth** for Dosion public legal documents.

| File | Live URL |
|------|----------|
| `privacy.md` | https://dosion.bioaionics.com/privacy |
| `terms.md` | https://dosion.bioaionics.com/terms |

## How updates reach the site

1. Edit and push `privacy.md` / `terms.md` on `main` in this repo.
2. The **dosion-landing** Cloudflare Worker fetches these files from GitHub raw and renders HTML.
3. No copy-paste into the landing static tree is required for normal updates.

Landing repo: https://github.com/kisuro/dosion-landing  
Worker fetch base: `https://raw.githubusercontent.com/kisuro/dosion-legal/main/{privacy,terms}.md`

Static `privacy/` / `terms/` HTML under the landing repo (if present) is **fallback only** when GitHub fetch fails — do not treat it as the editable source.

## Editing checklist

- Keep App Store / runtime claims accurate (CloudKit sync scope, HealthKit on-device, StoreKit product IDs `com.bioaionics.dosion.pro.*`).
- Bump **Last updated** and **Version** in the markdown header when making material changes.
- After push, hard-refresh live URLs (Worker edge cache: up to ~1 hour `s-maxage`).
