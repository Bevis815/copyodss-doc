# Copy Settings

What each parameter in the copy wizard means. For fields not shown in the wizard (such as some daily limits or delays), go by the current App interface; advanced limits from older docs may have been consolidated.

***

## Basic settings

| Setting | Description |
|---------|-------------|
| **Leader address** | The wallet address to copy; must be correct |
| **Name** | Display name for the rule, optional |
| **Copy mode** | Fixed amount or % of balance |
| **Amount / Ratio** | Fixed USDC per trade, or a percentage of available balance |
| **Slippage tolerance** | Acceptable deviation from the trader's fill price; no fill if exceeded |

### How to think about slippage

Slippage set **too tight**: more likely to skip or fail when prices move.  
Slippage set **too loose**: more likely to fill, but possibly at a worse price.  
The default is on the loose side to improve fill rates; adjust it to your own risk appetite.

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
