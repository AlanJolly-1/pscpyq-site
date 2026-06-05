# Account Deletion Policy

**App name:** PSC PYQ  
**Android package:** `com.pscprepcompanion.app`  
**Effective date:** 2026-06-05

## Do you create user accounts?

Yes. You may sign in with email (or continue in guest mode without a server account).

## What data exists and where it is stored

| Data | Signed-in users | Guest mode |
|------|-----------------|------------|
| Profile (email, name, phone) | Supabase | Not stored on servers |
| Quiz sessions and answers | Device only | Device only |
| Coin wallet, unlocks, subscription status | Supabase | Device only (guest coins) |
| Referrals | Supabase | Not stored on servers |
| Theme and preferences | Device only | Device only |
| App feedback / question reports (if submitted) | Supabase (user link removed on delete) | Supabase (anonymous) |

## How to delete your account (signed-in users)

1. Open the app → **Profile**.
2. Tap **Delete account** and confirm.

This calls our server to remove your authentication record and cascades deletion of your profile, coin wallet, paper unlocks, referral records, and subscription records we store. Quiz history on your device is cleared by the app after deletion. Optional feedback or question reports you previously submitted may remain without your account identifier.

**Important:** Deleting your account does **not** cancel an active **Google Play** subscription or refund coin purchases. Cancel subscriptions in **Google Play → Subscriptions**. Refund requests follow [Google Play’s policies](https://support.google.com/googleplay/answer/2479637).

## How to delete guest / local data only

If you use guest mode or want to wipe local data without a server account:

- **Option A:** Uninstall the app.
- **Option B (Android):** Settings → Apps → PSC PYQ → Storage → **Clear storage / Clear data**.

## What gets deleted

**Account deletion (signed-in):** server profile, coin balance and unlocks on servers, referral records, subscription records on servers, sign-in credentials, and local quiz history cleared by the app.

**Clear storage / uninstall:** all local data including guest quiz history, guest coin wallet, and preferences.

## Contact

Questions: **geocartindia@gmail.com**
