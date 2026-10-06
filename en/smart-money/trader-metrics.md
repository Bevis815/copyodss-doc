# Understanding Trader Metrics

Numbers on the leaderboard and profile pages aren't always calculated the same way. Below are the fields you'll see most often. **All metrics are for reference only and do not guarantee future performance.**

***

## Overall score and tier

| Concept | Description |
|---------|-------------|
| **Overall score / Trader score** | Result of a multi-factor model; higher usually means better overall performance |
| **Leaderboard rank** | The default overall ranking may combine multiple ranks and is **not** simply sorted by overall score |
| **Tier (S–D)** | A quality tier label for the address (e.g. S = top smart money → D = caution / high risk) |
| **Risk** | Risk level hints such as Low / Medium / High |

### Score factors (common)

| Factor | Meaning (simplified) |
|--------|----------------------|
| Edge | Prediction / pricing advantage |
| Profitability | Ability to make money |
| Copyability | Whether they're easy to keep up with under delay and slippage assumptions |
| Drawdown health | Whether drawdowns are under control |
| Consistency | Whether performance is sustained and stable |
| Style penalty | Traits like gambling concentration may lower the score |

The scoring window is mostly a recent sample, not the account's full history since creation.

***

## Common list / card metrics

| Metric | How to read it |
|--------|----------------|
| **Total P&L** | P&L under the stated methodology; note whether it's a recent window or the official PnL service |
| **7-day P&L** | Short-term performance; less meaningful when volatile |
| **Win rate** | Share of closed samples called correctly; high win rate ≠ guaranteed profit |
| **Drawdown / DD** | Drop from the peak; lower is usually better |
| **Copy fit** | Simulated copyability: High / Medium / Low |
| **Profit factor** | Ratio-type metric of total profits vs. total losses |
| **Stability / Activity** | Related to return volatility and trading frequency |
| **7-day trades / Volume** | Whether they're still actively trading |
| **Avg. closed return** | Average return-type metric across closed samples |

Columns marked as "simulated" (backtest P&L, copy loss, slippage, etc.) are simulations **assuming delayed fills**, **not** real copy results of platform users.

***

## Profile snapshot (common fields)

| Field | Description |
|-------|-------------|
| Current funds | Reference for the trader's capital size |
| Total P&L / Unrealized P&L | Realized and open-position floating P&L |
| Total volume | Reference for trading activity |
| Total return / Avg. profit margin | Return-type ratios |
| Wins / Losses | Sample structure |
| Profit factor | Profit quality |
| Largest win / Largest loss (drawdown) | Tail risk |
| Recent activity | Whether they're still trading |

***

## "Real copy performance" vs. "Copy simulation"

| Type | Meaning |
|------|---------|
| **Copy simulation** | The system backtests "what would happen if you copied" with delay + slippage assumptions |
| **Real copy performance** | Samples from users actually copying this address on the platform (ROI, copy P&L, subscribers, etc.); may be hidden when samples are insufficient |

**Neither** guarantees your results after copying.

***

## Reading tips

1. Look at score, drawdown, and copyability before total P&L
2. With too few samples, win rate and ROI are easily distorted
3. For market-maker / extremely concentrated-bet addresses, good-looking metrics don't mean they're suitable to copy
4. Ultimately, judge copy results by your own **Trade history**
