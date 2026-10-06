# Devices & Passkeys

This page covers two security topics: **which devices have logged into your account**, and **how to log in quickly with Face ID / fingerprint**.

Entry: Settings → Security → **Devices** → `/settings/devices`; Passkeys are managed in Settings → `/settings/passkeys`

***

## 1. Devices

### What you'll see

| Field | Meaning |
|-------|---------|
| Device name | e.g. your phone model or OS name; shows "Unknown device" if it can't be identified |
| **Current device** | The one you're using right now |
| **Last active** | When it was last used |
| Active sessions | How many login sessions are on this device |
| Withdrawal available at | New devices usually have to wait a while before they can withdraw |

### Removing a device

1. Find a device you don't recognize → tap **Remove**
2. After you confirm, the device is removed and **its login sessions are invalidated immediately**

### When to remove one

- You switched phones / computers and the old device is still listed
- There's a device in your login history you don't recognize
- You suspect someone else is using your account

> After removal, that device must log in again (email code / Telegram / Passkey).

***

## 2. Passkeys

A Passkey lets you log in with your phone's **Face ID, fingerprint, or screen lock** instead of entering a code.

### Adding a Passkey

1. Settings → Passkeys → **Add passkey**
2. Complete Face ID / fingerprint verification as prompted
3. Once done, the Passkey appears in the list with its creation time, last used time, and whether it's synced

### Using it to log in

Choose **Passkey** on the login page — no email needed.

### Deleting a Passkey

Select it → **Delete** → confirm. After deleting, that device can no longer log in with a Passkey.

### Troubleshooting

| Symptom | What to do |
|---------|------------|
| Face ID doesn't pop up when adding | Cancel and **tap "Add Passkey" again**, completing verification as soon as the prompt appears; dismiss notification banners first |
| Says this device isn't supported | Use the system's built-in browser (Safari on iOS, Chrome on Android), or just use an email code |
| Says a Passkey with the same name already exists | Delete the old "Android device" entry first; if you're using a proxy / VPN, turn it off and try again |
| Login fails | Log in with an email code instead; a Passkey failure doesn't affect your account security |

> Passkeys can only be used for login and **cannot be used for withdrawal verification**.
