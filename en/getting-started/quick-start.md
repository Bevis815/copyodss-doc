# Quick Start

Follow these steps to go from opening the App to your first copy rule. Always use the official domains **copyodds.io / app.copyodds.io**.

![Login page](../.gitbook/assets/login_doc.png)

***

## 1. Log in or create an account

1. Open the App and go to **Login**.
2. Enter your email → **Send code** → enter the 6-digit code → log in.
3. **A new email automatically creates an account** (no separate sign-up page with your name; if the screen still asks for a name / terms, just follow the prompts).
4. Optional: log in with a **Passkey** or **Telegram**.
5. If you arrive through an invite link, the invite code is usually filled in automatically.

### Notes

- Codes are typically valid for about 5 minutes; you can't resend immediately after sending
- If the email doesn't arrive, check your spam / promotions folder
- Passkeys must be registered on a supported device and browser (manage them in Settings)

***

## 2. Deposit USDC / USDT

1. Open **Assets / Deposit** → `/wallets/deposit`
2. **Pick a network**: Polygon (PoS) or BSC (must match the network you withdraw from on your exchange)
3. **Pick an asset**: USDC or USDT only
4. Copy the address on this page or scan the QR code to transfer (**Polygon and BSC addresses are different — never mix them up**)
5. Wait for on-chain confirmation; BSC may take a few extra minutes

![Deposit page](../.gitbook/assets/usdc1_doc.png)

See [Deposit](../wallet/deposit.md) and [Supported Networks](../wallet/supported-networks.md) for details.

***

## 3. Buy Platform Gas

1. Open **Gas Store** → `/store`
2. Check your current Gas and USDC balances
3. Pick a package → pay with your custodial USDC
4. Gas is credited instantly (non-withdrawable)

![Gas Store](../.gitbook/assets/store_doc.png)

Fees in short: each copy fill costs about **0.5%** of its notional amount in Gas; **1 USDC ≈ 100 Gas**. See [Platform Gas](../wallet/gas.md).

***

## 4. Pick a trader and copy

1. Open **Smart money** → `/smart-money` (the App's default home page)
2. Use categories, quick filters, or advanced filters to pick a trader
3. Tap **Follow**, or open the profile first and follow from there
4. In the wizard, set the copy mode (fixed amount / % of balance), slippage, and advanced options
5. Make sure Gas > 0, then save → manage it in **My copies**

![Smart money + Follow](../.gitbook/assets/smarket_doc.png)

![Copy settings](../.gitbook/assets/follow_doc.png)

***

## 5. Check whether copying works

| Page | Purpose |
|------|---------|
| **My copies** | Whether the rule is active and whether there's a funding alert |
| **Trade history** | Whether your orders were filled / skipped / failed |
| **Copy activity** | The trader's public actions (**not** your fills) |
| **Positions** | Your current positions; close / redeem here |

***

## Tips for beginners

- Start with a small deposit, buy a little Gas, and test with a small fixed amount for 1–2 days
- When funds or Gas run low, buys are skipped but the rule usually **does not** pause automatically; after topping up, go to **My copies** and tap **Resume buys**
- Withdrawals support **Polygon USDC** only — double-check the address before submitting
