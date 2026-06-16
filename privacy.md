# Privacy Policy

**App:** Dosion — Supplement Tracker
**Developer / Data Controller:** Artem Odintsov
**Contact:** dosion@bioaionics.com
**Effective date:** 30 April 2026
**Last updated:** 16 June 2026
**Version:** 1.1

---

## 1. Who we are

Dosion ("the App") is developed and operated by Artem Odintsov, established in Berlin, Germany, European Union ("we", "us", "our").

For the purposes of Regulation (EU) 2016/679 (GDPR), we act as the **data controller** for personal data processed through the App.

We are a small independent developer and are not legally required to appoint a Data Protection Officer. For all privacy-related questions, contact us at: **dosion@bioaionics.com**.

---

## 2. Scope

This Policy applies to personal data processed when you install and use Dosion on an Apple device running iOS 18 or later.

It does **not** cover:

- Data processed by **Apple Inc.** through Sign in with Apple, App Store, Apple Health (HealthKit), iCloud, StoreKit, or TestFlight — governed by [Apple's Privacy Policy](https://www.apple.com/legal/privacy/).
- Third-party websites you visit through links inside the App (for example iHerb) — governed by their own policies.

---

## 3. Data we collect and process

### 3.1 Data you provide directly

| Category | Examples |
|----------|----------|
| Account identifiers (Apple Sign-in only) | Apple user identifier, display name (if shared), email or Apple private relay address (`@privaterelay.appleid.com`) |
| Supplement stack | Names, brands, doses, units, schedules, cycle settings, intake logs, inventory notes |
| Wellbeing check-ins | Mood, energy, sleep, focus, stress, tags, free-text notes |
| Profile and preferences | Goal, meal times, wake/bed times, currency, appearance settings |
| Profile photo | Optional; stored as a local JPEG file in the App's Application Support directory. If you enable iCloud sync, the photo is also replicated to your private CloudKit container as an encrypted asset (see section 6) |
| Support messages | Content you choose to send via the in-app feedback email flow |

### 3.2 Apple Health (HealthKit)

If you connect Apple Health, the App may **read**:

- Sleep analysis
- Workouts
- Resting heart rate
- Heart rate variability (HRV, SDNN)
- Active energy
- Biological sex

If you enable HealthKit write-back (Dosion Pro), the App may **write** dietary nutrient samples (vitamins, minerals, omega-3, and other mapped nutrients) to Apple Health, marked as "user entered", only after you confirm an intake as taken.

**Our HealthKit commitments:**

- HealthKit data is processed entirely on-device.
- HealthKit-derived personal characteristics (such as biological sex and the last HealthKit sync timestamp) are stored locally on your device only. They are **not** transmitted to our servers, **not** shared with any third party, and **not** synced to iCloud.
- Raw HealthKit samples are not retained beyond the daily snapshot needed for Insights analysis.
- You can revoke iOS-level HealthKit permission at any time in **iOS Settings → Privacy → Health → Dosion**. Inside the App (**Me → Apple Health**), you can also disconnect HealthKit at the App level, which stops the App from reading or writing HealthKit data; the iOS-level permission grant must be revoked separately in iOS Settings if you want to remove it entirely.

### 3.3 Device permissions

| Permission | Purpose | Notes |
|------------|---------|-------|
| Camera | Scan supplement labels and barcodes; take a profile photo | Processed on-device; images are not uploaded |
| Photo Library | Attach a supplement package photo when scanning is unavailable; set a profile photo | Processed on-device; images are not uploaded |
| Notifications | Local reminders to take supplements and refill low stock | Reminder titles and bodies may include the supplement name (and brand, where available). Notifications are scheduled and rendered locally; we do not send remote push notifications |
| Apple Health | As described in section 3.2 | Gated by explicit iOS permission prompt |

You can revoke any permission at any time in iOS Settings → Privacy.

### 3.4 Diagnostic metadata in feedback emails

When you use the in-app "Report a bug" or "Request a feature" flow, your default mail app opens with a pre-filled email containing non-personal diagnostic metadata:

- App version and build
- iOS version
- Device model class
- Authentication mode (Apple Sign-in or Guest)
- Apple Health connection state (connected / not connected)
- Number of supplements in your stack (count only)

This metadata does **not** include the names or details of your supplements, the contents of your intake logs or check-ins, your HealthKit values, your Apple ID, or your contact information.

You review and control the email before sending. We receive only what you choose to send.

### 3.5 Beta testing (TestFlight)

If you participate in Dosion's beta via Apple TestFlight, Apple collects crash reports and usage data on our behalf subject to Apple's privacy policy and TestFlight's terms. We may receive anonymised crash information from Apple. We do not collect additional data from beta participants beyond what is described in this Policy.

### 3.6 Data we do NOT collect

- No third-party analytics or advertising SDKs
- No advertising identifiers (IDFA)
- No tracking across apps or websites (no ATT permission is requested)
- No third-party crash reporting SDKs
- No advertising or behavioural profiling

---

## 4. Avatars

Profile avatars in Dosion work as follows:

- If you set a profile photo via Edit picture, it is stored as a local JPEG file on your device and displayed from there. If you enable iCloud sync, it is also replicated as a CloudKit asset to your private CloudKit container.
- If no photo is set, the App displays your initials generated on-device from your display name. No external service is contacted for avatar generation.

---

## 5. Purposes and legal bases

| Purpose | Personal data involved | Legal basis (GDPR Art. 6) |
|---------|----------------------|--------------------------|
| Provide core App functionality | Stack, intake, schedule, profile data | Art. 6(1)(b) — performance of a contract |
| Optional Apple Health integration | HealthKit reads and writes (also Art. 9(2)(a)) | Art. 6(1)(a) — consent |
| Optional iCloud sync | Stack, logs, profile preferences, profile photo | Art. 6(1)(a) — consent |
| Local reminders | Schedule data | Art. 6(1)(b) |
| Subscription and entitlement management | Apple-issued StoreKit receipts and transaction IDs | Art. 6(1)(b) |
| Respond to support requests | Diagnostic metadata, message content | Art. 6(1)(f) — legitimate interest in supporting users |
| Legal compliance and defence of claims | As required | Art. 6(1)(c) and Art. 6(1)(f) |

You may withdraw consent at any time. Withdrawal does not affect the lawfulness of processing before withdrawal.

---

## 6. Storage and local-first architecture

Dosion is **local-first**. Your data is stored in a SwiftData database on your device, with small preferences in iOS system storage, your profile photo in the App's Application Support directory, and a small App Group container shared with the Dosion home-screen widget extension.

**What stays on-device only (always):**

- HealthKit-derived characteristics (such as biological sex and last HealthKit sync timestamp)
- Wellbeing check-ins
- Local notifications schedule
- Entitlement cache and one-time install state flags
- App Group container values shared with the widget extension
- Local feature caches (e.g., USDA food search cache)

**What is optionally synced through iCloud (only when you enable iCloud sync with Apple Sign-in):**

- Supplements
- Intake logs
- Profile preferences (goal, meal times, currency, appearance)
- Profile photo (replicated as a CloudKit asset)

CloudKit is operated by Apple Inc. Data in your CloudKit container is subject to Apple's privacy policy and is associated with your Apple ID. We have no direct access to your CloudKit container.

**Guest mode:** all data remains on your device. iCloud sync is unavailable in guest mode. When you delete the App from your device, iOS removes the App's local data; we do not retain any copy.

---

## 7. Third-party services

| Service | Operator | Purpose | Data transferred |
|---------|----------|---------|-----------------|
| Dosion Food API | Us, hosted on Cloudflare Workers | Food and nutrition search | Search query text or scanned barcode. No account identifier. Operational logs retained ~30 days, then deleted. |
| USDA FoodData Central | U.S. Dept. of Agriculture | Upstream nutrition database | Called server-side from our Worker. No user data is sent. |
| Open Food Facts | Open Food Facts (France) | Barcode enrichment fallback | The scanned barcode value only. |
| NIH Dietary Supplement Label Database (DSLD) | U.S. National Institutes of Health | Barcode/UPC enrichment fallback | The scanned UPC value only. |
| UPCItemDB | UPCitemdb.com (United States) | Generic barcode lookup fallback | The scanned UPC value only. |
| iHerb | iHerb LLC (United States) | Optional shopping links | No data sent by us. iHerb may apply its own cookies and referral tracking. We may earn a referral commission. |
| Apple iCloud (CloudKit) | Apple Inc. | Optional sync | Data listed in section 6. |
| Apple StoreKit | Apple Inc. | Subscription billing and entitlement | Apple-managed receipts and transaction IDs. We do not see your payment details. |
| Apple Translation | Apple Inc. | On-device query translation for non-English food searches | Text processed on-device; not sent to our servers. |

### International data transfers

Our Food API runs on Cloudflare's global network, which may process requests in data centres outside the EEA. Cloudflare acts as our data processor and we have a Data Processing Addendum in place. Transfers outside the EEA are covered by Standard Contractual Clauses (SCCs) adopted by the European Commission.

NIH DSLD and UPCItemDB are based in the United States. When you trigger a barcode lookup, the barcode value is transmitted to those services over HTTPS.

---

## 8. Data retention

| Data | Retention period |
|------|-----------------|
| All local App data (stack, logs, check-ins, profile) | Until you delete the App or use Settings → Delete Account |
| iCloud-synced data | Until you delete the App, use Settings → Delete Account, or remove the App's iCloud container from Apple ID settings |
| Profile photo file (local + CloudKit asset, if synced) | Until you remove it or delete the App / account |
| Diagnostic metadata in support emails | Up to 3 years |
| Cloudflare Worker operational logs | Approximately 30 days |

When you use Settings → Delete Account, the App removes all local SwiftData records, in-App preferences, cached entitlement state, your local profile photo file, and feature caches.

---

## 9. Your rights under GDPR

As a data subject under GDPR, you have the right to:

- **Access** — request a copy of personal data we hold about you.
- **Portability** — receive your data in a machine-readable format (use Settings → Export Data in the App).
- **Rectification** — correct inaccurate personal data.
- **Erasure** — request deletion of your personal data (use Settings → Delete Account in the App, or contact us).
- **Restriction** — ask us to restrict processing of your data in certain circumstances.
- **Object** — object to processing based on legitimate interests.
- **Withdraw consent** — withdraw consent for optional features (Apple Health, iCloud sync) at any time in iOS Settings or the App's Me tab.

To exercise any right, contact us at **dosion@bioaionics.com**. We will respond within 30 days.

You also have the right to **lodge a complaint** with the competent supervisory authority. As our establishment is in Germany, the lead supervisory authority is:

> **Berliner Beauftragte für Datenschutz und Informationsfreiheit**
> Friedrichstr. 219, 10969 Berlin
> [www.datenschutz-berlin.de](https://www.datenschutz-berlin.de)

---

## 10. Security

We implement the following measures:

- Data is stored in the iOS-encrypted on-device SwiftData store, protected by the device passcode and Secure Enclave where applicable.
- iCloud sync uses Apple's CloudKit encryption at rest and in transit.
- Communication between the App and our Food API uses HTTPS.
- API keys and server-side credentials are never embedded in the App binary.
- We maintain no central database of user data.

No method of transmission or storage is 100% secure. We will notify affected users and relevant supervisory authorities in the event of a data breach as required by GDPR Art. 33–34.

---

## 11. Children

The App is not directed at children. You must be at least **16 years old** to use Dosion. We do not knowingly collect personal data from persons under 16. If you believe a child under 16 has provided us with personal data, contact us and we will delete it promptly.

---

## 12. Changes to this Policy

We may update this Policy from time to time. When we do, we will update the "Last updated" date at the top of this page. For material changes, we will provide notice through the App or the App Store listing. Continued use of the App after the effective date of a revised Policy constitutes your acceptance of the changes.

---

## 13. Contact

**Artem Odintsov**
Email: **dosion@bioaionics.com**
