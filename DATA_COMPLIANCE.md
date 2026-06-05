# Data Compliance

**App name:** PSC PYQ  
**Website:** [pscpyq.online](https://pscpyq.online)  
**Android package:** `com.pscprepcompanion.app`  
**Effective date:** 2026-06-05  
**Data protection contact:** geocartindia@gmail.com
 
This document describes how PSC PYQ handles personal data in line with applicable privacy laws, including India's **Digital Personal Data Protection Act, 2023 (DPDP Act)** and common app-store requirements (Google Play Data safety, account deletion). It supplements our [Privacy Policy](./PRIVACY_POLICY.md).

> This is an operational compliance summary for users and store reviewers. It is not legal advice.

## 1. Who we are (Data Fiduciary)

PSC PYQ is operated as an independent study app. For personal data processed through the app and website, we act as the **Data Fiduciary** under the DPDP Act — we decide why and how your data is processed.

**Grievance / data requests:** geocartindia@gmail.com  
Subject line suggestion: `PSC PYQ — Data request`

We aim to acknowledge data requests within **7 business days** and resolve them within **30 days**, unless a longer period is required by law or the complexity of the request.

## 2. What personal data we process

| Category | Examples | Where stored | Who it applies to |
|----------|----------|--------------|-------------------|
| Account | Email; optional name and phone | Supabase (servers) | Signed-in users |
| Coin wallet | Balance, reward claims, paper unlocks | Supabase | Signed-in users |
| Purchases | Google Play purchase tokens; Razorpay order/payment references | Supabase | Signed-in users |
| Pro subscription | Plan status, expiry | Supabase | Signed-in users |
| Referrals | Link between referrer and referred accounts; referrer email | Supabase | Signed-in users |
| Quiz activity | Answers, scores, history, badges, in-progress state | **Your device only** (AsyncStorage / local storage) | All users |
| Preferences | Theme, animations, guest flag | Your device | All users |
| Guest coins | Balance and unlock list | Your device | Guest mode |
| App feedback | Optional message; app version; platform | Supabase (user link optional) | Anyone who submits feedback |
| Question reports | Report text; question snapshot; app version | Supabase (user link optional) | Anyone who reports a question |
| Crash diagnostics | Stack traces, basic device info | Sentry | Production app builds |
| Rewarded ads (optional) | Ad interaction / device signals | Google AdMob | Signed-in Android users who choose to watch |

We **do not** collect precise location, contacts, photos, microphone, or government ID numbers.

## 3. Why we process data (Purposes)

We process personal data only to:

- Create and manage your account and profile
- Operate quiz practice, progress, and preferences on your device
- Run the coin wallet, paper unlocks, referrals, and promo codes fairly
- Verify Google Play and Razorpay purchases and manage Pro access
- Respond to support, feedback, and question-issue reports
- Improve stability and fix crashes
- Serve **optional** rewarded ads when you explicitly choose to watch them

We **do not sell** your personal data.

## 4. Legal basis and consent

- **Contract / service delivery:** Account, wallet, purchases, and subscription data needed to provide the app you signed up for.
- **Consent:** Optional profile fields (name, phone), rewarded ads, and optional feedback/report messages you choose to submit.
- **Legitimate interests:** Fraud prevention, purchase verification, and app security — balanced against your rights.
- **Legal obligation:** Where we must retain certain records (e.g. payment disputes) as required by applicable law or payment platforms.

By creating an account or continuing to use PSC PYQ after reading our Privacy Policy, you are informed of our data practices. You may withdraw consent for optional processing (e.g. stop using rewarded ads) without affecting core study features.

## 5. Where data is stored and cross-border transfer

- **Primary database & auth:** [Supabase](https://supabase.com) (PostgreSQL). Infrastructure may be located outside India (e.g. United States or European Union regions, depending on project configuration).
- **Payments:** Google Play (Android); Razorpay (web, where supported) — processed under their terms and locations.
- **Ads:** Google AdMob (Android, optional).
- **Crash reporting:** [Sentry](https://sentry.io).

When data is processed outside India, we rely on our processors' contractual safeguards and security practices. By using the app you acknowledge that some service providers may process limited data in other countries to operate the service.

## 6. Security measures

- **Row-Level Security (RLS)** on Supabase tables so signed-in users can only access their own account rows.
- **HTTPS** for network communication between the app and our servers.
- **Service-role keys** used only inside server-side Edge Functions — never shipped in the app.
- **Minimal collection** — quiz answers and session history are not uploaded to our servers.
- **Access controls** — administrative database access is limited to operators who need it to run the service.

No method of transmission or storage is 100% secure. We work to protect your data but cannot guarantee absolute security.

## 7. Data retention

| Data | Retention |
|------|-----------|
| Account, wallet, unlocks, subscription | Until you delete your account, then removed via cascade delete |
| Referral records | Until either party deletes their account (cascade) |
| Purchase / fulfillment records | Removed on account deletion; we may retain anonymized aggregates for accounting |
| App feedback & question reports | Kept for product quality; if you delete your account, your `user_id` link is **removed** (set to null) but the message content may remain without account identification |
| Quiz history & preferences | On your device until you clear history, delete your account (app clears local data), or uninstall |
| Sentry crash events | Per Sentry project retention settings |
| AdMob data | Per Google's policies |

## 8. Your rights (Data Principal)

Depending on your location, you may have the following rights:

### Access and portability
- View profile fields in the app (Profile screen).
- Request a copy of server-held personal data by emailing **geocartindia@gmail.com**.

### Correction
- Edit your name and phone on the Profile screen.
- Email us if account email corrections are needed (email changes may require identity verification).

### Erasure (right to be forgotten)
- **Signed-in:** Profile → **Delete account** (see [Account Deletion Policy](./ACCOUNT_DELETION_POLICY.md)).
- **Guest / local only:** Uninstall the app or clear app storage (Android: Settings → Apps → PSC PYQ → Storage → Clear storage).
- Account deletion removes server-side profile, wallet, unlocks, subscription records, and auth credentials. It does **not** cancel Google Play billing.

### Withdraw consent / opt out
- Skip sign-in (guest mode) to avoid server account data.
- Do not watch rewarded ads.
- Clear local quiz history from Profile.

### Grievance (India — DPDP Act)
If you are dissatisfied with how we handle your personal data:

1. Email **geocartindia@gmail.com** with details of your concern.
2. We will investigate and respond within the timelines in section 1.
3. If you remain unsatisfied, you may escalate to the **Data Protection Board of India** when that mechanism is available under applicable rules.

### Other regions
Users in the EU/UK and other jurisdictions may have additional rights (restriction, objection, complaint to a supervisory authority). Contact us at the email above and we will respond in line with applicable law.

## 9. Children's data

PSC PYQ is intended for exam aspirants and is **not directed at children**.

- Under our Terms, users must be at least **13** years old.
- Under India's DPDP Act, a **child** is anyone under **18**. We do not knowingly collect personal data from children without verifiable parental consent. If you believe a minor has provided data without consent, contact us and we will delete it.

## 10. Third-party processors

| Processor | Purpose | Their policy |
|-----------|---------|--------------|
| Supabase | Auth, database, Edge Functions | [Supabase Privacy](https://supabase.com/privacy) |
| Google Play | Android purchases & subscriptions | [Google Privacy Policy](https://policies.google.com/privacy) |
| Razorpay | Web coin-pack payments | [Razorpay Privacy](https://razorpay.com/privacy/) |
| Google AdMob | Optional rewarded ads | [Google Privacy Policy](https://policies.google.com/privacy) |
| Sentry | Crash / error reporting | [Sentry Privacy](https://sentry.io/privacy/) |

We require these providers to handle data only for the services they provide to us and under their own compliance programmes.

## 11. Data breach notification

If a personal data breach is likely to affect your rights, we will take reasonable steps to investigate, mitigate harm, and notify affected users and regulators **as required by applicable law** (including the DPDP Act when applicable).

## 12. Google Play Data safety alignment

For Play Console Data safety declarations, the app generally:

- **Collects:** email, optional name/phone, purchase history (via Play), app interactions (coins/unlocks), crash logs, optional ad interaction if user watches rewarded ads.
- **Does not collect:** location, contacts, photos, financial account numbers (payments handled by Google/Razorpay).
- **Encrypted in transit:** Yes (HTTPS).
- **Users can request deletion:** Yes — in-app account deletion + email for data copies.

Quiz practice content and answers remain **on-device** and are not declared as server-collected personal data.

## 13. Changes

We may update this document when our data practices or legal requirements change. The effective date at the top will be revised accordingly. Material changes may also be reflected in the [Privacy Policy](./PRIVACY_POLICY.md).

## 14. Related documents

- [Privacy Policy](./PRIVACY_POLICY.md)
- [Terms of Service](./TERMS_OF_SERVICE.md)
- [Account Deletion Policy](./ACCOUNT_DELETION_POLICY.md)

## 15. Contact

Data protection questions, access requests, correction, erasure, or grievances:

**geocartindia@gmail.com**
