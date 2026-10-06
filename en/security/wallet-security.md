# Wallet Security

CopyOdds uses a **custodial trading account** model: you don't need to safeguard trading private keys yourself, but you do need to protect your login methods and withdrawal verification.

Full description in the App: **Asset security guarantee** → `/wallets/security`.

![Asset security guarantee](../.gitbook/assets/wallet_security_doc.png)

***

## Core mechanisms

| Capability | Description |
|------------|-------------|
| **Dedicated wallet** | Each user has a separate custodial wallet; assets are managed in isolation |
| **Private key isolation** | Wallet private keys are separately encrypted and isolated, never exposed directly to the everyday trading interface |
| **Withdrawal protection** | Withdrawals require step-up verification; changes to key security settings may trigger re-verification / a cooldown |

***

## Platform security guarantee (summary)

If user assets are lost as a direct result of a security incident in the CopyOdds **platform itself**, such as a security vulnerability or server breach, the platform will provide compensation in accordance with its security guarantee policy (subject to the product page and legal terms).

Please note:

- The platform will **never** ask for your seed phrase, private key, password, or verification codes via DM, email, or support
- Prediction market trading losses, user mistakes (wrong chain, wrong address), phishing scams, etc. are not covered under "platform security incident compensation"
- Always use the official domain

***

## What you need to do yourself

1. Only use the official website / App: **copyodds.io**
2. **Enable Authenticator** (required for withdrawals; see [Two-Factor Authentication (2FA)](2fa.md))
3. Optionally add a Passkey for easier login
4. Manage your logged-in devices and don't trust unknown "support agents"
5. Deposit using the address on the page, and check it with **Verify deposit address**
6. Test your first deposit and withdrawal with small amounts

***

## Related pages

- Deposit / Withdraw: `/wallets/deposit`, `/wallets/withdraw`
- Security settings: `/settings`
- Device management: `/settings/devices`
- Passkeys: `/settings/passkeys`
