# Copy Activity

**Copy activity** tells you two things: **what the trader just did**, and **whether you copied it**.

Entry: **Copy activity** → `/feed` (usually reached from **My copies** or the menu)

***

## What's on the page

1. **Top: wallets I'm copying** — Lists the addresses you've enabled copying for; tap one to see only that one
2. **Three tabs**

| Tab | Content |
|-----|---------|
| **Activity** | The trader's public buys / sells |
| **My orders** | The result of each order the system placed for you |
| **My positions** | Your current positions and P&L |

3. **Filters**: All / Successful / Buys / Sells / Copying
4. Every entry shows a time (**just now**, **a few minutes ago**); pull down on mobile to refresh

***

## Reading copy statuses

| Status | Meaning | What to do |
|--------|---------|------------|
| **Copying** | Trying to place the order | Wait a moment |
| **Copied** | Successfully copied | Nothing |
| **Skipped** | Not copied this time | Check the failure reason |
| **Failed** | The order was rejected or errored | Check the reason — possibly balance / slippage / Gas |
| **Not copied** | This entry isn't within your copy scope | Nothing |

Tap any entry to see **trade details**: market, direction, address, volume, copy rule, copy wallet, status, time, and on-chain transaction hash.

***

## Common skip reasons

- Direction mismatch (you set Buy only / Sell only)
- Amount too small (below the exchange minimum buy of about $1)
- Reached "Max open copy buys" (default 1, i.e. no adding to positions)
- Slippage too large
- **Insufficient Gas** or **insufficient USDC**
- The trader sold but you don't hold the matching position
- No one was taking orders in that market at the time

***

## Tips

- Use **Activity** to watch others and **Trade history** to check yourself — comparing the two is the easiest way to spot problems
- If there are lots of skips, check Gas and balance first, then consider adjusting slippage or lowering the amount
- When sharing an entry with support, include the **record ID** or **transaction hash**
