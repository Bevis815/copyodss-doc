# Simulation Copy Trading

**Simulation copy trading** runs your copy strategy with a "virtual wallet" — **no real money involved**, purely for testing parameters and seeing results. It's ideal for beginners who aren't ready to put real money in yet.

Entry: **Simulation copy trading** → `/copy-trading/simulation`

> Simulation copy trading is being rolled out gradually. If you don't see this menu, it hasn't been enabled for you yet.

***

## How it differs from live copying

| | Simulation | Live copying |
|--|------------|--------------|
| Money | Virtual balance | Your custodial USDC |
| Gas | Not needed | Needed (about 0.5% service fee per trade) |
| Can you lose money? | Not for real | Yes |
| Purpose | Test parameters, see long-term performance | Real returns |

***

## Get started in three steps

### 1. Create a virtual account

Tap **Create virtual account** and fill in:

| Field | Description |
|-------|-------------|
| Account name | Something to tell them apart, e.g. "Test-A" |
| Starting balance | Simulated principal |
| Duration (days) | After it expires, no new positions are opened; existing positions can still be closed or settled |

### 2. Add addresses to copy

Add trader addresses under **Copy addresses**; you can name the strategy and add notes.

### 3. Configure the strategy

| Setting | Description |
|---------|-------------|
| Copy method | Ratio / Fixed amount |
| Direction | Buy and sell / Buy only / Sell only |
| Min / Max per trade | Amount range for each trade |
| Per-market cap | The most to put into a single market |
| Daily cap | The most to put in per day |
| Max slippage | No fill if exceeded |
| Execution delay | Simulates "reacting a bit slower" |
| Market cooldown | Minimum interval between two copies in the same market |
| Pause after consecutive failures | Pause after this many failures in a row (default 10) |

Tap **Start simulation copy** to run it.

***

## Viewing results: five tabs

| Tab | Content |
|-----|---------|
| **Copy addresses** | The addresses you added, strategy settings, and status |
| **Positions** | Simulated positions; you can simulate closing them manually |
| **Executions** | Shares, fees, and status for each simulated fill |
| **Performance** | Equity curve, total P&L, win rate, max drawdown, slippage cost, fee cost, etc. |
| **Ledger** | Details of every fund movement |

### Statuses

| Account status | Meaning |
|----------------|---------|
| Active | Running normally |
| Paused | You paused it; can be resumed |
| Expired | No new positions; existing equity can still be handled |
| Archived | Put away; can't be archived while it holds positions |

### Note on closing positions

Closing manually requires a **market price from within the last 15 minutes** to get a quote; if the price is stale or missing, you'll be prompted to refresh the quote. Before confirming, you'll see the estimated fill price, slippage, fees, estimated proceeds, and estimated P&L.

***

## In one sentence

The real value of simulation copy trading is this: **before spending real money, you get to see what "frequent copying + high slippage + small principal" actually leads to.**
