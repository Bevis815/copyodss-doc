# Deposit

Deposit USDC / USDT into your CopyOdds **trading account** to use as copy principal. Entry: **Wallets → Deposit** → `/wallets/deposit`.

![Deposit page](../.gitbook/assets/usdc1_doc.png)

***

## Deposit in four steps

1. **Pick network** — Polygon (PoS) or BSC, matching the network you withdraw from on your exchange  
2. **Pick asset** — **USDC** or **USDT** only  
3. **Send** — Copy or scan **the address shown on this page**  
4. **Wait** — Your balance updates after on-chain confirmation; BSC may take a few extra minutes

The page also has a **Deposit steps** section with the same four steps, plus a **Watch tutorial** video link (`/guide-video`). We recommend watching it before your first deposit.

### Three handy tips

| Action | Description |
|--------|-------------|
| **Save the QR code** | Tap **Save image** to store the address QR code on your phone; scanning is less error-prone than typing |
| **Copy after picking the network** | After switching to BSC you **must copy the address again** — the two chains use different addresses |
| **Only use the address currently shown on this page** | Don't use old addresses from chat history or sent by others |

***

## Important rules

| Rule | Description |
|------|-------------|
| Supported networks | **Polygon (PoS)** (recommended) and **BSC**; the page shows tags such as "Recommended / Fast / Low fees" |
| Address depends on network | The Polygon custodial address and the BSC bridge address are **different** — never mix them up |
| USDC / USDT only | Other tokens usually can't be credited |
| Don't use the wrong chain | Don't use unsupported networks such as Ethereum / Arbitrum |
| Verify the address | Tap **Verify deposit address**, and the system will send the address to you via the **official Telegram bot** or your **linked email** to check |
| Prefer USDC | USDT on Polygon is often shown as "USDT (PoS)"; don't deposit BNB or other tokens |

### How to use Verify deposit address

1. Tap **Verify deposit address**
2. The page will prompt you to start the official Telegram bot (`@botname`) or check your linked email
3. When you receive the address, **check it character by character** against the page
4. Only proceed if it matches exactly

### Your balance has two numbers

| Term | Meaning |
|------|---------|
| **On-chain balance** | Native USDC that has actually arrived on the blockchain |
| **Tradable balance** | The portion the platform has processed and that can be used for copying |

If, right after a deposit, you see "xx native USDC on-chain, automatically converting to tradable balance", that's the normal flow — wait a few minutes and refresh.

***

## Details

1. Log in and confirm your trading account is active
2. On the deposit page, pick the network first, then copy the address
3. When withdrawing from your exchange or wallet: carefully check the network, token, and amount
4. Return to CopyOdds and pull to refresh your balance if needed
5. Before your first large deposit: deposit a small amount → confirm it arrives → then deposit more

***

## Deposit slow or missing?

Check in this order:

1. Does the withdrawal network match the one selected on this page (Polygon vs. BSC)?
2. Is the token USDC / USDT?
3. Is the receiving address **exactly the same** as on this page?
4. Is the on-chain transaction confirmed? (Look up the hash on the corresponding block explorer)
5. Did you send it to a withdrawal destination or another platform's address by mistake?

Still missing: contact support with the **transaction hash, network, amount, time, and registered email**.

***

## What's next after depositing?

- To start copying: first make sure **Polymarket is ready**, then **buy Platform Gas** (see [Platform Gas](gas.md))
- Copy buys need available USDC (at least about $1 recommended)

***

## Where to check after it arrives

Open **Transaction history** → `/wallets/ledger` to see the deposit's network, asset, status, and balance after the transaction. See [Transaction History](ledger.md).
