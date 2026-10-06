# How CopyOdds Works

From "a trader gets a fill" to "your account tries to copy it", the whole flow looks like this:

```text
Smart money trader gets a fill on Polymarket
        ↓
CopyOdds detects the public fill
        ↓
Matches your copy rule for that address
        ↓
Calculates order size per the rule (fixed amount or % of your balance)
        ↓
Tries to place the order within slippage (consumes Platform Gas)
        ↓
Result is written to Trade history; holdings show up in Positions
```

## 1. Discovering traders

- The system continuously scores and screens public Polymarket wallets
- The **displayed leaderboard** usually requires the overall score to meet a threshold (e.g. ≥ 40); low-scoring addresses may drop off
- In **Smart money** you can browse, search, or analyze unlisted addresses (if the feature is available, a daily limit may apply)

## 2. Funds and fees are separate

| In-account resource | Purpose |
|---------------------|---------|
| **USDC (etc.)** | Copy principal: used when buying, returned when selling |
| **Platform Gas** | Service-fee credits: about 0.5% of the notional amount is deducted per copy fill |

When Gas is 0: you **can't create / resume copy rules**. Existing rules usually keep running, but **buys are skipped**; sells may still be copied if you hold positions.

## 3. How copy rules take effect

You save one rule per leader address (saving again for the same address overwrites it):

- **Copy mode** (pick one; default **Ratio**):
  - **Ratio**: each of the leader's fills × your ratio = your order amount
  - **By balance %**: each trade uses a percentage of your own available USDC
  - **Fixed amount**: every trade buys the same amount
  - See [The Three Copy Modes](../copy-trading/copy-modes.md)
- **Direction**: Both / Buy only / Sell only
- **Slippage**: no fill if the price moves too far (default 15%)
- **Copy ratio / Size range** (Ratio mode only): controls "how much to copy" and "which order sizes to copy"
- **Max open copy buys**: default 1 (no adding to positions); can be raised, and the maximum is **All (unlimited)**

After detecting a leader fill, the system tries to place an order using these rules. It **does not guarantee** every trade will be copied.

## 4. How to tell whether a trade was copied

| Where to look | What it tells you |
|---------------|-------------------|
| Copy activity | What the trader did |
| Trade history | Your copy attempt results (filled / skipped / failed) |
| Positions | What you currently hold |
| My copies | Rule status: Following / Manually paused / Funding alert |

## 5. Deposit and withdrawal networks differ (important)

- **Deposit**: Polygon (PoS) and BSC (when enabled), assets USDC / USDT
- **Withdraw**: **Polygon (PoS) USDC** only
- The two deposit networks use **different addresses** — never mix them up

See [Supported Networks](../wallet/supported-networks.md).

## 6. Security model in brief

CopyOdds uses a **custodial trading account**: one wallet per user, with isolated private keys. Withdrawals require **Authenticator (TOTP)** step-up verification. See [Security](../security/wallet-security.md).
