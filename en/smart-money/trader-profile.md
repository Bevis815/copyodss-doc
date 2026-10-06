# Trader Profile

The trader profile page shows a single wallet's portrait: score, funds and performance, curves, positions, fills, and the copy entry point.

**Link format:**

- English: `https://app.copyodds.io/@0xTRADER_ADDRESS`
- Chinese: `https://app.copyodds.io/zh/@0xTRADER_ADDRESS`

> Some legacy paths (e.g. containing `address`) may be blocked by ad blockers; prefer `/@0x...`.

![Trader profile](../.gitbook/assets/trader_profile_doc.png)

***

## Page layout (common sections)

1. **Trader score** — Overall score, recommended/suitable tags, risk, reasons for being listed / not listed, factor scores
2. **Funds & performance** — Snapshot of current funds, total P&L, volume, win rate, etc.
3. **P&L curve** — Historical equity / PnL trend
4. **Positions / Fills** — The trader's current positions and recent trades
5. **Copy simulation** — Copyability results under delay + slippage assumptions
6. **Real copy performance** — Copy ROI, P&L, subscriber count, etc., shown when there are enough samples
7. **Actions** — **Follow**; if simulated copying is enabled, there may also be a Simulation entry

***

## How to start copying from the profile

1. Check the address, score, and risk notes
2. Tap **Follow**
3. In the wizard, set amount / percentage, slippage, and advanced options
4. After saving, go to **My copies** and confirm the rule status is Following

See [How to Copy a Trader](../copy-trading/how-to-follow.md).

***

## Things to keep in mind

- While the score is "calculating", some factors and listing reasons may only appear in full later
- When a simulation section clearly states its assumptions, don't treat it as realized returns
- When real copy samples are insufficient, the UI may say it's relying on simulation for now
- When sharing with others, use the official profile link and remind them to check the domain **copyodds.io**
