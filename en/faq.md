# FAQ

When something goes wrong, check this page first. If you still can't solve it, please have ready: your registered email, the time of the action, error screenshots, and the transaction hash or trade history ID.

---

## Account & login

### Do new users need to sign up separately?

In most cases, entering a **new email** on the login page and completing the code creates an account automatically. If the screen still asks for a name / terms, just follow the prompts.

### Not receiving the verification code?

Check your spam folder and the email spelling; resend after the countdown ends. Company email servers sometimes block it — try a personal email you use often.

### What if Passkey fails?

Log in with an email code instead; make sure your browser is supported and you're not using an incompatible embedded WebView, then re-add the Passkey in Settings.

---

## Account setup & authorization

### Do I need to apply for a trading account?

**No.** It's usually opened automatically after login, so you can deposit right away. In the rare case it shows "not yet opened", tap to open it and accept the agreement. See [Trading Account & Wallet Page Status](wallet/trading-account.md).

### The wallet page shows "Agent authorization" — do I have to pay gas?

No. Signing is free and the platform covers on-chain fees. You just need the wallet you registered with, switched to **Polygon (chain ID 137)**.

### Is "Polymarket trading authorization incomplete" a problem?

Just tap **Re-authorize Polymarket**. It's an issue in the authorization step and **does not affect funds you've already deposited**.

### Why are there two numbers, "on-chain balance" and "available balance"?

On-chain balance is the native USDC that has actually arrived; available balance is the portion processed and ready for copying. They may differ for a few minutes right after a deposit — that's normal.

---

## Deposits & balance

### Why hasn't my balance updated after depositing?

Check that: the network is **Polygon or BSC (matching the page)**, the asset is **USDC/USDT**, the address exactly matches this page, and the transaction is confirmed on-chain. BSC may be slower. Refresh your balance after confirmation; if it still hasn't arrived, provide the transaction hash.

### Can I deposit USDT?

Yes, but it must be USDT on the network selected on the page, sent only to this page's address. Don't force a withdrawal from the wrong network.

### What happens if the destination wallet has no MATIC?

The withdrawal will succeed, but **you won't be able to move that USDC on-chain afterward**. Keep a little MATIC (POL) in the receiving address.

### The withdrawal says "channel busy" — what should I do?

Wait a few minutes or hours as prompted and try again. **Your funds are safe**, and you don't need to resubmit.

### Right after arriving, it says "automatically converting to tradable balance"?

That's normal. Native USDC that arrives on-chain needs to be processed into tradable balance automatically — wait a few minutes and refresh.

### Can I confirm a withdrawal with a Passkey or email code?

**No.** Withdrawals currently only accept **Authenticator codes**; Passkeys and email codes are only for login and similar scenarios.

### Does turning off Authenticator require a code?

Yes. For security, turning it off also requires a 6-digit code. If you're switching devices, it's easier to just re-bind on the new device.

### Why is the withdrawable amount less than my balance?

Positions and open orders tie up funds. Go by **Max withdrawable**.

### Are the Polygon and BSC addresses the same?

**No.** Never mix them up. See [Supported Networks](wallet/supported-networks.md).

---

## Gas & copying

### What's the difference between Platform Gas and MATIC / BNB?

Platform Gas is a CopyOdds service-fee credit bought with USDC in the Gas Store. MATIC / BNB are on-chain native tokens used for network fees — **they're not the same thing**.

### Why can't I add or resume a copy rule?

The most common reason is **Gas = 0**. Buy Gas, then enable / resume.

### How much USDC do I need to start copying?

Enabling a rule usually only requires Gas > 0. But each actual buy needs about **$1** or more of available USDC.

### I bought Gas / deposited funds — why still no copy buys?

When funds are insufficient, buys are skipped but the rule isn't necessarily paused. After topping up, go to **My copies** and tap **Resume buys**. Also check Trade history for slippage failures, direction mismatches, or hitting the no-adding-to-positions limit.

---

## Copy execution

### Why were some trades not copied?

Common reasons: direction settings, amount too small, no-adding-to-positions limit, slippage, insufficient USDC/Gas, no shares to sell, insufficient liquidity. Open Trade history to see the specific status.

### Copy activity shows the trader bought — why didn't I?

Copy activity ≠ your fills. Check Trade history.

### The trader sold — why didn't I?

You must hold shares in that market. If you never bought or have already sold out, a skipped sell is normal.

### What's the difference between pausing and deleting?

A paused rule can be resumed; a deleted rule must be recreated. Neither one automatically closes your positions.

---

## Withdrawals & security

### Why do withdrawals need step-up verification?

To protect your funds and prevent assets from being moved out directly if a session is hijacked. Verification methods are used in this order: **Authenticator** first if bound; then **Passkey**; and if neither is available, it falls back to **email verification**.

### Can a Passkey be used to withdraw?

No. A Passkey is a shortcut for **login**; withdrawals only accept Authenticator codes.

### Can't withdraw after logging in on a new phone?

A new-device cooldown may have been triggered, or the Authenticator isn't set up in the new environment yet. Try again later and check device management and your TOTP binding; contact support if it keeps failing.

### Will the official team ever ask for my seed phrase?

**Never.** See [Anti-Phishing](security/anti-phishing.md).

---

## Smart money

### Does the leaderboard guarantee profits?

**No.** Metrics are based on public data and models and include simulation assumptions; past performance ≠ future returns.

### How do I open a trader's profile?

`https://app.copyodds.io/@0xADDRESS` (add `/zh` for the Chinese UI).

### Are "Copy fit / backtest P&L" my real returns?

No. They're mostly simulations assuming delay + slippage; your actual results are in Trade history.

---

## Copy modes

### What copy modes are there, and which should I pick?

**Ratio** (default), **By balance %**, and **Fixed amount**. If it's your first time, just use the default **Ratio**: you buy a percentage of whatever the trader buys, which makes it hardest for one of their big bets to blow up your account. See [The Three Copy Modes](copy-trading/copy-modes.md).

### What does "Ratio" mean?

If the trader buys $5,000 in one trade and your ratio is 10%, you buy $500. The ratio range is 0.1%–100%.

### What is the "Leader order size range" in Ratio mode for?

It filters out tiny dust orders and oversized orders. Orders below the lower bound are skipped; orders above the upper bound are still copied, but the amount is calculated as "upper bound × ratio", so one big bet from the trader doesn't get amplified.

### Can I just use the "Suggested ratio" the page gives me?

Yes. It's calculated as "your available balance ÷ (range upper bound × the trader's approximate trades per day)", designed so that **you'll use about that many trades' worth over a day**. Lower it manually if you want to be more conservative.

### Why was my trade skipped with "Outside size band"?

The trader's order was too small (below the range's lower bound). It's a dust order filtered out on purpose, not a bug.

### What happens if the calculated amount is under $1?

As long as your balance is enough, the system automatically **tops it up to $1** (the exchange minimum buy) and places the order instead of skipping it.

### Is the default slippage 30% or 15%?

The default in copy settings is **15%**, adjustable from 1% to 100%.

### Why are the parameters pre-filled when I copy from a trader profile?

The system uses the "copy simulation" results to pre-fill slippage and max copy buys for you; the page will say "Pre-filled from copy simulation".

---

## New features

### What's the difference between Leaderboard and Smart money?

Leaderboard shows the **daily profit ranking of copy pool accounts** (home page); Smart money shows the **score and profile of individual trader addresses**. To pick traders, use the Leaderboard to find a direction first, then refine with Smart money's filters.

### Are "Copy activity" and "Trade history" the same thing?

No. Copy activity shows **what the trader did**; Trade history shows **the results of your copy attempts**. Comparing the two is the easiest way to spot problems.

### Does simulation copy trading use my real money?

**No.** Simulation copy trading runs in a separate virtual account and doesn't need Gas either.

### Why can't I sell my position?

It may be "pending settlement" (the market has ended and is waiting to settle), or there may be no buy orders in that market at the moment. If you won, a **Redeem** button will appear.

### Is "Transaction history" on the wallet page the same as the trade history menu?

No. **Executions** in the menu is your **copy trade history**; **Transaction history (`/wallets/ledger`)** in the wallet is your **fund movement and Gas spending ledger**.

### Will removing a device in device management affect my copies?

It won't delete your copy rules, but the old device's login sessions are invalidated immediately and it will need to log in again.

### Is the commission on the affiliate page always 10%?

No. Your commission rate depends on your **tier** (from L1 at 10% up to the top tier). L1 is activated automatically after you make a purchase, then you upgrade automatically based on your number of direct referrals; the top tier must be purchased.

### Do I have to download the App on my phone?

No. The web version is fully featured; for a more app-like experience, use your browser's "Add to Home Screen". See [Using CopyOdds on Mobile](getting-started/mobile-app.md).

---

## Risk notice

- Market prices fluctuate and copy trading can lose money
- Automated copying may diverge from the trader due to slippage, delay, and liquidity
- Wrong chain, wrong address, or wrong token may result in funds not arriving or being unrecoverable
- Insufficient Gas / USDC causes buys to be skipped
- Leaderboard and simulation results are for reference only and are not a promise of returns

New users should run through the whole flow with a small amount first: Deposit → Buy Gas → Copy → Check Trade history → Then try a small withdrawal.
