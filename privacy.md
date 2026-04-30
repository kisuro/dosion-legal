# Privacy Policy

**App:** Dosion — Supplement Tracker
**Developer / Data Controller:** [Your Legal Name / Company Name]
**Registered address:** [Street, Number, Postcode, City, Greece, European Union]
**Contact:** [your@email.com]
**Effective date:** [DD Month YYYY]
**Last updated:** [DD Month YYYY]

---

## 1. Who we are

Dosion ("the App") is developed and operated by [Your Legal Name / Company Name], established in Greece, European Union ("we", "us", "our").

For the purposes of Regulation (EU) 2016/679 (GDPR) and Greek Law 4624/2019, we act as the **data controller** for personal data processed through the App.

We are a small independent developer and are not legally required to appoint a Data Protection Officer. For all privacy-related questions, contact us at: **[your@email.com]**.

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
|---|---|
| Account identifiers (Apple Sign-in only) | Apple user identifier, display name (if shared), email or Apple private relay address (`@privaterelay.appleid.com`) |
| Supplement stack | Names, brands, doses, units, schedules, cycle settings, intake logs, inventory notes |
| Wellbeing check-ins | Mood, energy, sleep, focus, stress, digestion, tags, free-text notes |
| Profile and preferences | Goal, meal times, wake/bed times, currency, appearance settings |
| Profile photo | Optional; stored only on-device as a local JPEG file |
| Support messages | Content you choose to send via the in-app feedback email flow |

### 3.2 Apple Health (HealthKit)

If you connect Apple Health, the App may **read**:

- Sleep analysis
- Workouts
- Body mass (weight)
- Resting heart rate
- Heart rate variability (HRV, SDNN)
- Active energy
- Date of birth
- Biological sex

If you enable HealthKit write-back (Dosion Pro), the App may **write** dietary nutrient samples (vitamins, minerals, omega-3, and other mapped nutrients) to Apple Health, marked as "user entered", only after you confirm an intake as taken.

**Our HealthKit commitments:**

- HealthKit data is processed entirely on-device.
- HealthKit-derived personal characteristics (weight, birth year, biological sex, last sync timestamp) are stored locally on your device only. They are **not** transmitted to our servers, **not** shared with any third party, and **not** synced to iCloud.
- Raw HealthKit samples are not retained beyond the daily snapshot needed for Insights analysis.
- You can revoke access at any time in iOS Settings → Privacy → Health, or inside Dosion under Me → Apple Health.

### 3.3 Device permissions

| Permission | Purpose | Notes |
|---|---|---|
| Camera | Scan supplement labels and barcodes; take a profile photo | Processed on-device; images are not uploaded |
| Photo Library | Attach a supplement package photo when scanning is unavailable; set a profile photo | Processed on-device; images are not uploaded |
| Notifications | Local reminders to take supplements and refill low stock | Scheduled locally; we do not send remote push notifications |
| Apple Health | As described in section 3.2 | Gated by explicit iOS permission prompt |

You can revoke any permission at any time in iOS Settings → Privacy.

### 3.4 Diagnostic metadata in feedback emails

When you use the in-app "Report a bug" or "Request a feature" flow, your default mail app opens with a pre-filled email. This email includes non-personal diagnostic metadata to help us reproduce issues: App version and build, iOS version, device model class, locale, and a redacted state summary. This metadata contains no health data, no contact data, no Apple ID, and no supplement content.

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

- If you set a profile photo via Edit picture, it is stored as a local JPEG file on your device and displayed from there.
- If no photo is set, the App displays your initials generated on-device from your display name. No external service is contacted for avatar generation.

---

## 5. Purposes and legal bases

| Purpose | Personal data involved | Legal basis (GDPR Art. 6) |
|---|---|---|
| Provide core App functionality | Stack, intake, schedule, profile data | Art. 6(1)(b) — performance of a contract |
| Optional Apple Health integration | HealthKit reads and writes (also Art. 9(2)(a)) | Art. 6(1)(a) — consent |
| Optional iCloud sync | Stack, logs, check-ins, profile preferences | Art. 6(1)(a) — consent |
| Local reminders | Schedule data | Art. 6(1)(b) |
| Subscription and entitlement management | Apple-issued StoreKit receipts and transaction IDs | Art. 6(1)(b) |
| Respond to support requests | Diagnostic metadata, message content | Art. 6(1)(f) — legitimate interest in supporting users |
| Legal compliance and defence of claims | As required | Art. 6(1)(c) and Art. 6(1)(f) |

You may withdraw consent at any time. Withdrawal does not affect the lawfulness of processing before withdrawal.

---

## 6. Storage and local-first architecture

Dosion is **local-first**. Your data is stored in a SwiftData database on your device, with small preferences in iOS system storage and your profile photo in the App's Application Support directory.

**What stays on-device only (always):**
- HealthKit-derived characteristics (weight, birth year, biological sex, last sync timestamp)
- Profile photo file
- Local notifications schedule
- Entitlement cache

**What is optionally synced through iCloud (only when you enable iCloud sync with Apple Sign-in):**
- Supplements
- Intake logs
- Wellbeing check-ins
- Profile preferences (goal, meal times, currency, appearance)

CloudKit is operated by Apple Inc. Data in your CloudKit container is subject to Apple's privacy policy and is associated with your Apple ID. We have no direct access to your CloudKit container.

**Guest mode:** all data remains on your device and is permanently deleted when you delete the App.

---

## 7. Third-party services

| Service | Operator | Purpose | Data transferred |
|---|---|---|---|
| Dosion Food API | Us, hosted on Cloudflare Workers | Food and nutrition search | Search query text or scanned barcode. No account identifier. Operational logs are retained for approximately 30 days for abuse prevention, then deleted. |
| USDA FoodData Central | U.S. Dept. of Agriculture | Upstream nutrition database | Called server-side from our Worker. No user data is sent. |
| Open Food Facts | Open Food Facts (France) | Barcode enrichment fallback | The scanned barcode value only. |
| iHerb | iHerb LLC (United States) | Optional shopping links, opened in in-app browser | No data sent by us. iHerb may apply its own cookies and referral tracking per its privacy policy. We may earn a referral commission on qualifying purchases at no cost to you. |
| Apple iCloud (CloudKit) | Apple Inc. | Optional sync | Data listed in section 6. |
| Apple StoreKit | Apple Inc. | Subscription billing and entitlement | Apple-managed receipts and transaction IDs. We do not see your payment details. |
| Apple Translation | Apple Inc. | On-device query translation for non-English food searches | Text processed on-device by the Apple Translation framework; not sent to our servers. |

### International data transfers

Our Food API runs on Cloudflare's global network, which may process requests in data centres outside the EEA. Cloudflare acts as our data processor and we have a Data Processing Addendum in place. Transfers outside the EEA are covered by Standard Contractual Clauses (SCCs) adopted by the European Commission.

For iHerb links, iHerb LLC is established in the United States. Any data collected by iHerb when you visit their site is subject to their own privacy policy and transfer mechanisms.

Apple iCloud infrastructure is subject to Apple's own transfer mechanisms documented in Apple's Privacy Policy.

---

## 8. Data retention

| Data | Retention period |
|---|---|
| All local App data (stack, logs, check-ins, profile) | Until you delete the App or use Settings → Delete Account |
| iCloud-synced data | Until you delete the App, use Settings → Delete Account, or remove the App's iCloud container from Apple ID settings |
| Profile photo file | Until you remove it or delete the App / account |
| Diagnostic metadata in support emails | We retain support correspondence for as long as reasonably necessary to resolve the issue, up to 3 years |
| Cloudflare Worker operational logs | Approximately 30 days |

When you use Settings → Delete Account, all local SwiftData records, preferences, and local files are removed. Apple-managed data (CloudKit container, StoreKit history, Sign in with Apple association) is handled per Apple's own policies.

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

To exercise any right, contact us at **[your@email.com]**. We will respond within 30 days.

You also have the right to **lodge a complaint** with the Hellenic Data Protection Authority (HDPA):

> **Αρχή Προστασίας Δεδομένων Προσωπικού Χαρακτήρα (ΑΠΔΠΧ)**
> Kifissias 1-3, 115 23 Athens, Greece
> www.dpa.gr | contact@dpa.gr | +30 210 6475 600

---

## 10. Security

We implement the following measures:

- Data is stored in the iOS-encrypted on-device SwiftData store, protected by the device passcode and Secure Enclave where applicable.
- iCloud sync uses Apple's CloudKit encryption at rest and in transit.
- Communication between the App and our Food API uses HTTPS (TLS 1.2+).
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

**[Your Legal Name / Company Name]**
[Street, Number, Postcode, City, Greece, EU]
Email: **[your@email.com]**
