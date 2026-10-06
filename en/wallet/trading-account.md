# Trading Account & Wallet Page Status

Your CopyOdds **trading account is usually opened automatically after login** — no separate application needed. It's your **custodial trading wallet**: the USDC / USDT you deposit lives here and is used for copy trading.

Entry: **Wallets** → `/wallets` (the **Deposit** menu item opens this page)

***

## What you'll normally see

| Section | Content |
|---------|---------|
| On-chain deposit address | Your deposit address (**different per network**); copy it or save the QR code |
| Available balance | The portion you can use for copying right away |
| On-chain balance | Native USDC that has actually arrived on the blockchain |
| Platform Gas | Used to pay copy trading service fees |
| Withdraw | Enter a Polygon receiving address and amount |
| Transaction history | Deposits, withdrawals, and Gas spending |

If you see all of this, everything is working and you can deposit right away.

***

## Why the two balances differ

| Term | Meaning |
|------|---------|
| **On-chain balance** | Native USDC that has actually arrived on the blockchain |
| **Tradable balance** | The portion the platform has processed and that can be used for copying |

If, right after a deposit, you see "xx native USDC on-chain, automatically converting to tradable balance", that's **the normal flow** — wait a few minutes and refresh.

***

## Statuses you may occasionally see

Not everyone will see these; if you do, handle them as described below.

### "CopyOdds trading account not yet opened"

In rare cases the account isn't opened automatically (e.g. something went wrong during setup). Tap **Open trading account**, read and check the agreement, then confirm.

Agreement summary:

| Clause | Content |
|--------|---------|
| Service | The platform creates a custodial trading wallet for you, used for deposits, copying, orders, and withdrawals |
| Custody & authorization | Assets are held by the platform and you don't hold the private key directly; you authorize the platform to perform the necessary signing and trade execution |
| Withdrawal protection | You may be required to enable **Authenticator (TOTP)** step-up verification before withdrawing |
| Funds & networks | Only send supported assets to the address and network shown on the page; **choosing the wrong network or asset may make funds unrecoverable** |
| Risk notice | Copy trading is **high risk and you may lose your entire investment**; slippage, liquidity, and delay all affect results |
| Eligibility & compliance | You must be at least 18; it may not be used for money laundering, fraud, or other illegal purposes |

> The agreement may be updated; the full terms are in the in-app dialog and the User Terms of Service.

### An "Agent authorization" section appears

Some accounts see an extra **Agent authorization** section on the wallet page. It lets you **authorize with a single signature**, after which the platform places orders for you and **covers on-chain gas** (you don't need your own MATIC).

If you see this section, just follow the prompts:

| Requirement | Description |
|-------------|-------------|
| Sign with **the wallet you registered with** | Choosing the wrong account in your wallet shows "Current wallet is not the registered wallet" |
| Switch your wallet to **Polygon (chain ID 137)** | Otherwise you'll see "Please switch your wallet to Polygon and try again" |
| Complete the signature in one go | Closing the extension or changing the content midway causes failure; refresh and start over |
| Watch the expiry | After it expires, copying pauses — tap **Renew**; you can also **Revoke** it (you'll need to re-authorize after revoking) |

Common errors: wrong wallet / wrong chain / authorization request expired / signed content doesn't match verification (usually extension interference — refresh and try again).

### "Polymarket trading authorization incomplete"

Tap **Re-authorize Polymarket**. This message indicates an issue in the authorization step and **does not affect funds you've already deposited**.

> In rare cases where automatic authorization fails, the page offers a "Manually paste Polymarket API credentials (advanced)" option for troubleshooting. Regular users don't need to touch it.

***

## FAQ

**Is there a fee for the trading account?**  
Opening it is free. Platform Gas of about 0.5% is only deducted when copy trades fill.

**Where is my private key?**  
Not with you. CopyOdds uses a custodial wallet with private keys stored in isolation by the platform; you control your funds through login + withdrawal step-up verification.

**Why can I see the on-chain address but not move funds out myself?**  
That's the custodial design: the address belongs to the platform and is used to receive your deposits. To move funds out, you must go through the **withdrawal** flow and complete step-up verification.

**When do the two balances differ?**  
Usually only for the few minutes **right after a deposit while it's being converted automatically**. If they stay different for a long time, refresh; if it's still off, contact support with the transaction hash.
