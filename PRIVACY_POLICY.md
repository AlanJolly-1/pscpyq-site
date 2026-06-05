# Privacy Policy

**App name:** PSC PYQ  
**Android package:** `com.pscprepcompanion.app`  
**Effective date:** 2026-06-05

This Privacy Policy explains how PSC PYQ (“the app”, “we”, “us”) handles information when you use the app. For data-principal rights, retention, security, and India DPDP Act alignment, see also our [Data Compliance](./DATA_COMPLIANCE.md) document.

## Summary

- You may use the app with an account or in guest mode.
- Signed-in users: account profile, coin wallet, paper unlocks, and Pro subscription status are stored on our servers (Supabase).
- Quiz history, stats, in-progress quizzes, and daily-goal progress are stored on your device only (for all users).
- Coin packs and Pro are purchased through **Google Play on Android**; coin packs on the web (where supported) use **Razorpay**.
- We do not sell your personal information.

## Information we collect

### Account data

When you sign up we store your email address and, if you provide them, your name and phone number on the profile screen.

### Quiz activity (device only)

Questions you answer, your selected option, whether the answer was correct, session history, badges, and resume state are kept in the app’s local storage on your phone. This data is not uploaded to our servers.

### Device-local preferences

Theme, animations, guest-mode flag, quiz history, in-progress quiz state, and guest coin balance (in guest mode).

### Crash diagnostics

In production builds we use Sentry for unhandled errors (stack traces and basic device info, not your answers or profile details).

### Coin wallet (signed-in users)

Coin balance, reward claim dates (signup bonus, daily login, daily goal), and which full paper sessions you unlocked. Daily goal eligibility (e.g. 20 answers today) is calculated on your device before you claim; the server only records that you claimed the reward so it cannot be claimed twice the same day.

### Coin purchases

**Android:** Coin packs are one-time in-app purchases through Google Play. Google processes payment; we receive a purchase token to verify on our servers and credit your balance.

**Web (where supported):** Coin packs may be purchased through Razorpay (UPI, cards, netbanking). Razorpay processes payment; we verify the order on our servers before crediting coins.

We do not receive your full payment card or UPI credentials from Google or Razorpay.

### Referrals (signed-in users)

If you use the referral feature, we store the link between referrer and referred accounts and the referrer email used for the reward programme.

### Feedback and question reports (optional)

You may submit app feedback or report a question issue. These may include your message and app version. If you are signed in, we may associate the submission with your account until you delete it (the link is then removed).

### Pro subscription (Android)

If you subscribe, Google processes recurring payments. We store subscription status and expiry on your account. Cancel in Google Play → Subscriptions.

### Rewarded ads (Android, optional)

If you choose to watch a video ad for bonus coins while signed in, Google AdMob may collect device and ad-interaction data needed to serve ads. Coins are credited only after you complete a rewarded ad.

## How we use information

We use this data only to operate the app: sign-in, local practice features, coin wallet and Pro access, Google Play purchase verification, optional rewarded ads, and stability. We do not sell your personal data. AdMob is used only when you choose to watch a rewarded ad.

## Where data is stored

Account, coin-wallet, unlock, and subscription data for signed-in users is stored in our Supabase project. Row-Level Security limits each user to their own rows. Quiz activity and guest-mode coins use the app’s sandboxed storage on your phone.

## Guest mode

You can use the app without signing in. Guest quiz data and guest coins stay on your device and are not uploaded. Signing in later does not automatically upload local guest history.

## Your rights and choices

- View and edit profile (name, phone) on the Profile screen.
- Clear local quiz history or discard in-progress quizzes from Profile.
- Delete your account from Profile. This removes server-side profile, coin wallet, unlocks, referral records, and subscription records. It does not cancel Google Play billing — cancel subscriptions in Google Play. Local quiz history on your device is cleared when you delete your account from the app.
- Request a copy of, correction of, or grievance about your data by emailing **geocartindia@gmail.com** (see [Data Compliance](./DATA_COMPLIANCE.md) for timelines and details).

## Children’s privacy

The app is not directed at children under 13. Contact us if you believe a child has provided personal data.

## Changes

We may update this policy. The effective date above changes when we do. Continued use after an update means you accept the revised policy.

## Contact

Privacy questions: **geocartindia@gmail.com**
