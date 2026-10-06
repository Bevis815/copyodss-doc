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

## Deposits & balance

### Why hasn't my balance updated after depositing?

Check that: the network is **Polygon or BSC (matching the page)**, the asset is **USDC/USDT**, the address exactly matches this page, and the transaction is confirmed on-chain. BSC may be slower. Refresh your balance after confirmation; if it still hasn't arrived, provide the transaction hash.

### Can I deposit USDT?

Yes, but it must be USDT on the network selected on the page, sent only to this page's address. Don't force a withdrawal from the wrong network.

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

To protect your funds and prevent assets from being moved out directly if a session is hijacked. Withdrawals currently only support **Authenticator** codes; if you haven't set one up, enable it in Settings first.

### Can I withdraw with a Passkey or email code?

**No.** Passkeys / email codes are for login and similar scenarios; withdrawals require an Authenticator.

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

## Risk notice

- Market prices fluctuate and copy trading can lose money
- Automated copying may diverge from the trader due to slippage, delay, and liquidity
- Wrong chain, wrong address, or wrong token may result in funds not arriving or being unrecoverable
- Insufficient Gas / USDC causes buys to be skipped

New users should run through the whole flow with a small amount first: Deposit → Buy Gas → Copy → Check Trade history → Then try a small withdrawal.
