# Settings

Entry: **Settings** → `/settings`

The Settings page gathers every switch other than copy trading in one place. If you're not logged in, you'll only see a login prompt.

***

## 1. General

| Item | Description |
|------|-------------|
| **Language** | Switch the interface language; afterward the URL gets a language prefix (e.g. `/zh`) |
| **Name** | Enter your first and last name to help support verify your identity |

***

## 2. Copy trading

- **Custodial trading address**: opened automatically after login; this is your actual receiving / trading address
- If it shows "not yet opened", follow the prompt to open it on this page before depositing
- For first-time use: run through the flow with a small deposit + small withdrawal before using larger amounts

***

## 3. Notifications

You can toggle each type of alert separately:

| Category | Alerts |
|----------|--------|
| Trading | Trader order detected, order submitted, order failed, order filled, order canceled |
| Budget & limits | Budget warning, insufficient balance |
| System | Auto-redeem, session about to expire |

> Preferences take effect as soon as they're saved; more advanced channels such as real-time push are rolling out gradually, and the page will show their current status.

***

## 4. Account linking

| Link | Purpose |
|------|---------|
| **Email** | Receive codes to log in; once linked, you can log in with either email or Telegram |
| **Telegram** | Log in with Telegram |
| **Web3 wallet** | Record your external wallet information |

> If the email / Telegram you link already belongs to another account, linking **keeps the current account**, and the other account can no longer log in that way.

***

## 5. Security

An account security status card:

| Item | Description |
|------|-------------|
| **Active sessions** | Number of current login sessions and their expiry |
| **Devices** | Manage devices you've logged in on; see [Devices & Passkeys](devices-and-passkeys.md) |
| **Terms status** | Whether you've accepted the user agreement |
| **Trading status** | Normal / Restricted |
| **Withdrawal verification** | Description of the step-up verification method required before withdrawing |

### Withdrawal step-up verification

You must confirm your identity before every withdrawal. **Currently only Authenticator codes are supported**; if not bound, enable it in Settings first. Passkeys and email codes cannot be used for withdrawals.

***

## 6. About

| Entry | Content |
|-------|---------|
| **User Agreement** | `/settings/terms` |
| **Privacy Policy** | `/settings/privacy` |
| **Version** | `/settings/version` — see the current version, whether a new version is available, and the Android download |

***

## 7. Log out

You can log out at the bottom of the Settings page. After logging out, you'll need to log in again to use copy trading, the wallet, and other features; your rules themselves are not deleted.
