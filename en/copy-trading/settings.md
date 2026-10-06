# Copy Settings

What each parameter in the copy wizard means. For fields not shown in the wizard (such as some daily limits or delays), go by the current App interface; advanced limits from older docs may have been consolidated.

***

## Basic settings

| Setting | Description |
|---------|-------------|
| **Leader address** | The wallet address to copy; must be correct |
| **Name** | Display name for the rule, optional |
| **Copy mode** | Pick one: **Ratio** (default) / **By balance %** / **Fixed amount** |
| **Copy ratio** | Ratio mode only: leader's fill × ratio = your order amount |
| **Slippage tolerance** | Acceptable deviation from the trader's fill price; default **15%**, adjustable from 1% to 100% |

### How to think about slippage

Slippage set **too tight**: more likely to skip or fail when prices move.  
Slippage set **too loose**: more likely to fill, but possibly at a worse price.  
The 15% default is meant to improve fill rates; adjust it to your own risk appetite. Ratio mode also has two extra parameters, "Leader order size range" and "Copy ratio" — see [The Three Copy Modes](copy-modes.md).

***

## Ratio mode parameters

| Setting | Description |
|---------|-------------|
| **Copy ratio** | 0.1%–100%; the page shows a suggested value with "about N trades/day" |
| **Leader order size range** | Derived from the leader's largest historical fill; below the lower bound is skipped, above the upper bound is calculated as "upper bound × ratio" |

For the full explanation and examples, see [The Three Copy Modes](copy-modes.md).

***

## Advanced settings

| Setting | Description |
|---------|-------------|
| **Direction · Both sides** | Copy both buys and sells |
| **Direction · Buy only** | Copy buys only |
| **Direction · Sell only** | Copy sells only |
| **Max open copy buys** | Max number of concurrent copy buys under the same rule; **default 1 = no adding to positions**; the maximum shows **All = unlimited** |

### Why no adding to positions by default?

Positions in a single prediction market can stack up quickly. The default of 1 helps limit single-market risk; raise it once you've confirmed the strategy suits you.

***

## Platform default behavior (good to know)

- **Copy delay**: currently the product usually tries immediately (no extra artificial delay)
- **Pause after consecutive failures**: the platform may briefly pause buys after repeated failures (exact thresholds may vary); after fixing the issue you can resume in **My copies**

***

## Funding-related "soft limits"

These aren't necessarily settings, but they act like limits:

| Situation | Effect |
|-----------|--------|
| Gas = 0 | Buys are skipped; buy Gas and tap **Resume buys** |
| Insufficient USDC | Buys are skipped; deposit more or lower the amount / percentage |
| Below about $1 | Buys may not meet the exchange's minimum notional |

***

## Changing settings

1. Open **My copies**
2. Find the rule → **Edit**
3. After saving, only future fills are affected

If Simulation is enabled in your environment, it may expose more limit-type parameters; for live copying, the wizard fields are what count.

***

## Fields on the Quick copy page

Besides starting a copy from a trader profile, you can also paste an address directly on the **Quick copy** page (`/copier`):

| Field | Description |
|-------|-------------|
| **Copy ratio** | Follows as a percentage of your available balance; 100% uses the full balance, 5% is a light position |
| **Per-trade cap (USDC)** | The most you'll put into any single trade |
| **Total cap (USDC)** | The most you'll put into all copies combined |
| **Auto-copy toggle** | When on, the system uses your custodial wallet to copy this user's orders automatically |

Setting the same address again **overwrites** the previous rule; after making changes, check once in **My copies**.
