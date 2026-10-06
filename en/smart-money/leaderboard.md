# Smart Money Leaderboard

The Smart Money leaderboard helps you find Polymarket traders worth copying. Entry: **Smart money** → `/smart-money` (the App home page goes here by default).

![Smart Money leaderboard](../.gitbook/assets/smarket_doc.png)

***

## What you can do here

1. **Browse the leaderboard** — View P&L, score, win rate, last 7 days, and more as cards or a table
2. **Search addresses** — Look up a trader by wallet address
3. **Filter** — Categories, quick presets, and advanced filters (tier, style, metric ranges, copyability, etc.)
4. **Ranking period** — Overall / Weekly / Monthly (the default is usually the overall ranking, which is not simply sorted by overall score)
5. **Copy** — Tap **Follow** to open copy settings, or open the profile first and decide there

***

## How leaderboard data is calculated (must read)

- P&L curves, last-7-day / total profit, etc. usually come from Polymarket's official PnL data
- Win rate, profit factor, etc. are mostly based on **closed markets**
- Scores and backtest metrics are based on **recent-window fills** (about 30 days / up to about 4,000 trades), **not the lifetime ledger**
- The **displayed leaderboard** usually only includes addresses whose overall score meets a threshold (e.g. ≥ 40); addresses that score low repeatedly may drop off
- "Copy fit / backtest P&L / slippage" and similar are mostly **simulations assuming delay + slippage**, not the real P&L of users copying on the platform

> The leaderboard **is not investment advice**. Past performance does not guarantee future returns.

***

## Common filters

### Example categories

All, Politics, Sports, Esports, Crypto, Culture, Weather, Economy, Tech, Finance, Mentions, and more.

### Example quick filters

| Preset | Rough purpose |
|--------|---------------|
| Featured | Platform-featured traders, leaning toward copyable |
| Steady | Relatively conservative style |
| High copyability | Easier to keep up with in simulation |
| Recently active | More frequent trading in the recent window |
| All copyable | Addresses available for copying |
| High win rate / High return / Low drawdown | Narrow down by the corresponding metric |
| Long-term stable | Candidates with better consistency |

### Advanced filters (common options)

- Copyable addresses only / Featured only (excluding market makers)
- Tier (S–D), trading style
- Metric ranges (e.g. trades in the last 7 days, win rate)
- Exclude specific risk tags
- Copyability: High / Medium / Low

***

## Trading style tags (for reference)

| Tag | Meaning (simplified) |
|-----|----------------------|
| Information edge | Tends to position early / information-driven |
| Arbitrage | Spread / arbitrage patterns |
| Gambler | High-volatility betting patterns; copy with extra caution |
| Market maker | High-frequency market making; usually unsuitable for regular copying |
| Mixed | General mixed style |

***

## Suggestions

1. Start with presets like Featured / High copyability / Steady to narrow the field
2. Open the profile to review score factors, drawdown, and risk notes
3. Follow with a small amount to test, then adjust gradually
4. When sharing a trader, use the profile link format: `https://app.copyodds.io/@0xADDRESS` (add `/zh` for the Chinese UI)
