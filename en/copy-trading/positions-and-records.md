# My Positions & Trade History

After you start copying, all your positions and the result of every order are on these two pages. **As a beginner, these two pages are all you need to know.**

| Page | Entry | What it answers |
|------|-------|-----------------|
| **My positions** | My positions → `/executions/positions` | What do I hold now, and am I up or down? |
| **Trade history** | Executions → `/executions/records` | The result of every copy attempt |
| **Profit/Loss** | Executions → Profit/Loss → `/executions/daily-pnl` | How much have I made over this period? |

***

## My positions

### What you'll see

| Field | Meaning |
|-------|---------|
| **Market / Outcome** | Which event and which outcome (Yes / No) you bought |
| **Avg. price / Current price** | Your entry cost and the current market price |
| **Cost / Value / P&L** | How much you spent, what it's worth now, and whether you're up |
| **Copy sources** | Which copy rules built up this position |
| **Status** | Open / Pending settlement / Settled / Archived |

### What you can do

| Action | Description |
|--------|-------------|
| **Buy more** | Buy a bit more yourself by entering a USD amount |
| **Close** | Sell at market to lock in P&L; the price moves with the market |
| **Bulk close** | Close up to a certain number of positions at once |
| **Redeem** | The market has ended and you won — convert the position to USDC |
| **View details** | See the buy time, settlement method, and full timeline |

### What the statuses mean

| Status | Description |
|--------|-------------|
| **Open** | The market hasn't ended; you can sell |
| **Pending settlement** | Can't sell for now; if you won, Redeem will appear; if you lost, it closes automatically |
| **Settled** | Converted to USDC and returned to your balance |
| **Archived** | Tiny or illiquid positions that can't be sold for now; doesn't affect anything else |

***

## Trade history (copy history)

Each row is one attempt the system made on your behalf:

| Status | Meaning |
|--------|---------|
| **Filled** | Copied successfully |
| **In progress** | Still processing |
| **Skipped** | No order placed (see the failure reason) |
| **Failed** | The order was rejected or errored |

You can filter by **Filled / Settled / Unsuccessful**. Tap any row to see: copy rule, order ID, buy price and shares, how it was closed (sold / redeemed / expired), cost, proceeds, P&L, full timeline, and on-chain hash.

***

## Profit/Loss page

- The top shows a **cumulative P&L curve**, switchable between 1 day / 1 week / 1 month, etc.
- The bottom shows a **period breakdown**, including today, yesterday, and each day's account P&L change
- The curve matches Polymarket's account P&L methodology; if official data is temporarily unavailable, the page will note that it's using platform ledger data instead

> The business day's start time is as shown on the page (e.g. starting at 08:00), so keep this in mind when looking at data across days.

***

## Common beginner questions

**Why doesn't my positions' P&L match my balance?**  
Position P&L is "estimated at the current market price", and the unrealized part changes with the price; your balance only reflects it once you sell or redeem.

**Why did my sell fail?**  
Common reasons: no buy orders in the market at the time, shares tied up in open orders, or the remaining position is below the minimum sell size. Try again later.

**I won — why don't I see the money?**  
It takes a little time to be credited after the market settles; you can tap **Redeem** to redeem manually. While it shows "Pending settlement", you can't act on it yet.
