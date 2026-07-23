# dosion-legal

**Source of truth** for Dosion public legal documents.

| File | Live URL |
|------|----------|
| `privacy.md` | https://dosion.bioaionics.com/privacy |
| `terms.md` | https://dosion.bioaionics.com/terms |

## How updates reach the site

1. Edit and push `privacy.md` / `terms.md` on `main` in this repo.
2. The **dosion-landing** Cloudflare Worker fetches these files via jsDelivr (`cdn.jsdelivr.net/gh/kisuro/dosion-legal@main/…`) and renders HTML.
3. No copy-paste into the landing static tree is required for normal updates.

Landing repo: https://github.com/kisuro/dosion-landing  
Fetch URL pattern: `https://cdn.jsdelivr.net/gh/kisuro/dosion-legal@main/{privacy,terms}.md`

If the live page looks stale after a push, purge jsDelivr (`https://purge.jsdelivr.net/gh/kisuro/dosion-legal@main/privacy.md`) and/or bump `LEGAL_RENDER_VERSION` in the landing Worker, then redeploy landing.

## Editing checklist

- Keep App Store / runtime claims accurate (CloudKit sync scope, HealthKit on-device, StoreKit product IDs `com.bioaionics.dosion.pro.*`).
- Bump **Last updated** and **Version** in the markdown header when making material changes.
- After push, hard-refresh live URLs (Worker edge cache: up to ~1 hour `s-maxage`).
