# Two-Factor Authentication (2FA)

CopyOdds logs you in with an **email verification code** by default (no traditional password). We recommend enabling both an Authenticator and a Passkey to strengthen withdrawal and login security respectively.

![Security settings](../.gitbook/assets/settings_security_doc.png)

***

## Available methods

| Method | Purpose |
|--------|---------|
| **Email OTP** | Login, binding verification |
| **Authenticator (TOTP)** | **Withdrawal step-up verification (the only method)**; also hardens account security |
| **Passkey** | Face / fingerprint / screen lock for quick **login** verification |
| **Telegram** | Optional login / binding method (see Settings) |
| **Device management** | View and remove devices; new devices may affect withdrawals |

***

## Recommended setup order

1. Bind and verify your email
2. **Enable Authenticator (required before withdrawing)**
3. Add a **Passkey** on devices you use often (for easier login)
4. Get familiar with the **Devices** list and remove any device you don't recognize

***

## Authenticator (TOTP)

1. Open **Settings → Security**
2. Follow the guide to scan the QR code / enter the key in your Authenticator app
3. Enter the 6-digit code to finish enabling it

**You can't withdraw without an Authenticator.** When withdrawing, just enter the 6-digit code from the app.

***

## Passkey

1. Open Settings in a supported browser / OS
2. Add a Passkey and complete biometric or screen-lock verification as prompted
3. On the login page you can choose Passkey for quick login

Note: a Passkey **cannot** replace the Authenticator for confirming withdrawals. Support varies across browsers, WebViews, and OS versions; if login fails, fall back to the email code.

***

## Devices and sessions

- View logged-in devices at `/settings/devices`
- After logging in on a new device or environment, **withdrawals may be temporarily locked** for a while (security cooldown)
- On public computers, don't trust unknown extensions long-term or save codes in insecure places

***

## Lost your authenticator?

If you can still access your email:

1. Log in with an email code
2. Re-bind the Authenticator (and any Passkeys you need) in Settings
3. Check the device list and remove the lost device

If you can't access your email either: contact support and prepare identity verification materials (per the support process).
