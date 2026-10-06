# The Three Copy Modes (Beginners Start Here)

The first thing to choose in copy settings is the **copy mode**. There are currently three:

| Mode | One-line summary | Best for |
|------|------------------|----------|
| **Ratio** (new, default) | You buy a **fixed percentage** of whatever the trader buys | Most people, especially when the trader's order sizes vary a lot |
| **By balance %** | Each trade uses a **percentage of your own balance** | People who want position size to scale with their balance automatically |
| **Fixed amount** | Every trade buys **the same amount** | Traders whose order sizes are fairly consistent |

> **New users default to Ratio mode.** It's the most recommended mode right now and is covered in the most detail below.

***

## Why was Ratio mode added?

Fixed amount has a common problem: the trader buys $30 one time and $3,000 the next, but you always copy $10 — so you completely miss their rhythm, either copying too little to matter or blindly copying too much.

Ratio mode changes this to: **however much they place, you place a proportional amount**.

| Trader's fill | Your Fixed amount mode | Your Ratio mode (10%) |
|---------------|------------------------|-----------------------|
| $50 | Copy $10 | Copy $5 |
| $500 | Copy $10 | Copy $50 |
| $5,000 | Copy $10 | Copy $500 |

The benefit is that it **naturally tracks the trader's position sizing**, without one occasional big bet from them blowing up your account.

***

## Ratio mode in detail

### Three things to set

| Setting | Where | Description |
|---------|-------|-------------|
| **Copy ratio** | Slider below the mode | 0.1%–100%. Trader's fill × this ratio = your order amount |
| **Leader order size range** | Second slider below the mode | Only copies the trader's "normal-sized" orders, filtering out dust and oversized orders |
| **Slippage tolerance** | Below the mode | 1%–100%, default **15%** |

### 1. Copy ratio

This is the "how much to copy" ratio. The settings page shows a preview line:

> Leader 100, you set 10%, so yours is 10.

The page usually also shows a **Suggested ratio** next to "about N trades/day". It's calculated like this:

> **Suggested ratio ≈ your available balance ÷ (range upper bound × trader's approximate trades per day)**

Example: you have $1,000 available, the trader buys about 5 times a day, and the range upper bound is $800.
Suggested ratio ≈ 1000 ÷ (800 × 5) = 25%. In other words, **you'll use about 5 trades' worth over a day**, and one big order won't wipe out your balance at once.

If you don't want the suggested value, just drag the slider to set your own, from 0.1% to 100%.

> Tip: once you drag the slider, the system stops overriding your choice automatically; the suggestion is only recalculated when you refresh or pick a trader again.

### 2. Leader order size range

This range is derived from **the trader's largest historical single fill**, and defaults to the middle portion (about 5%–95%). It filters out two kinds of orders:

| Situation | Handling | Why |
|-----------|----------|-----|
| Trader buys **too little** (below the lower bound) | **Skipped**, not copied | These "dust orders" aren't worth copying and would just cost Gas |
| Trader buys **within the range** | Copied normally at your ratio | This is the trader's regular activity |
| Trader buys **too much** (above the upper bound) | **Still copied**, but the amount is calculated as "upper bound × your ratio" | Prevents one occasional big bet from putting all your money in |

The page has ready-made presets:

| Preset | Meaning | Best for |
|--------|---------|----------|
| **All 0–100%** | No filtering at all | Traders whose order sizes are very regular |
| **Balanced 1–99%** | Copies almost everything, filtering only extremes | **Default, best for beginners** |
| **Core 20–80%** | Only copies the main middle portion | More conservative, copying only core activity |

**Official example**: range $200–$800, ratio 10%, the trader buys $5,000 → you copy only $80.

> Tip: right after choosing a trader, if there's no historical fill data for them yet, the page will say "No cache yet; copying at the default ratio for now, actual amounts will be capped by your balance" — this is normal.

### 3. Slippage tolerance

- Meaning: the maximum allowed deviation in fill price
- Default **15%**, adjustable from 1% to 100%
- **Tighter**: more likely to skip or fail when prices move
- **Looser**: more likely to fill, but possibly at a worse price

> When you start copying from a trader profile, the system uses the "copy simulation" results to pre-fill slippage and max copy buys; the page will say "Pre-filled from copy simulation".

***

## How a single copy trade is actually calculated

Suppose you set: ratio **10%**, range **$200–$800**, balance $1,000.

| Step | Description |
|------|-------------|
| 1. Look at the trader's fill | They bought $5,000 |
| 2. Check whether it's within the range | Above the $800 upper bound, so it's **not skipped**, but calculated from the upper bound |
| 3. Calculate the amount | Take the **smaller** of "trader's fill × 10%" and "upper bound × 10%" = $80 |
| 4. Check your balance | Continue if balance ≥ $1; if not enough, order with what your balance actually allows |
| 5. Top up to the minimum | If the result is under $1, it's **topped up to $1** (the exchange minimum buy) as long as your balance allows |
| 6. Deduct Gas | After the fill, about 0.5% is deducted in Platform Gas |

Now a case within the range: the trader buys $500 → 500 × 10% = $50, copied normally at $50.

***

## When trades get skipped

| Message in the App | In plain words | What to do |
|--------------------|----------------|------------|
| **Outside size band** | The trader's order was too small — a dust order | Nothing; this is by design |
| **Insufficient funds** | Your available balance is below $1 | Deposit, or lower the ratio |
| **Your size < $1** | Too small even after topping up | Raise the ratio or lower the range upper bound |
| **Price ≥ $0.85** | The trader bought an outcome that's already priced as "nearly certain" | Nothing |
| **Already open (no add-on)** | You've already copied into this market | Keep the default "no adding" or change the setting |
| **Slippage too high** | The price moved away | Consider loosening slippage |
| **Low Gas** | You've run out of Platform Gas | Top up in the [Gas Store](../wallet/gas.md) |

> Note: the **"under $1 is topped up to $1"** rule applies in all three modes (Ratio, Fixed amount, By balance %). So orders under $1 aren't skipped — they're topped up and copied (as long as your balance allows).

***

## The other two modes

### By balance %

- Each trade uses a **percentage of your own available USDC balance**; e.g. at 5% with a $1,000 balance, each trade buys $50
- As your balance grows, each trade grows automatically; as it shrinks, trades shrink
- Results under $1 are also topped up to $1

**Best for**: people who want position size to scale with their balance without constantly adjusting amounts by hand.

### Fixed amount

- Every trade buys **the same amount**, e.g. $25 each time
- Minimum $1
- Special rule for small orders: when the amount is under $1, if it's **≥ 5 shares** the order uses your set amount; if **under 5 shares**, it's adjusted to $1 automatically

**Best for**: traders whose order sizes are fairly consistent (e.g. around $200 per trade over the long run), when you want precise control over each trade's cost.

***

## Which one should I pick?

| Your situation | Recommendation |
|----------------|----------------|
| First time, not sure what to choose | **Ratio** (default) |
| The trader's order sizes vary a lot | **Ratio** |
| You want precise control over each trade's amount | **Fixed amount** |
| You want position size to scale with your balance | **By balance %** |

***

## FAQ

**What's the most I can be charged per trade in Ratio mode?**

There's no separate per-trade cap — your ratio × the trader's fill is the amount, but it's limited by both the "range upper bound" and "your balance". To be more conservative, lower the ratio and the range upper bound.

**I'm nervous about using the suggested ratio directly.**

You can use it directly; the system already accounts for "about how many trades per day". To play it safer, start a small rule with a lower ratio, watch for a day or two whether there are many skips, then increase gradually.

**Does Ratio mode conflict with "no adding to positions"?**

No. The default "max 1 copy buy" (no adding) means **the same market** is bought only once; the ratio controls **how much this one trade buys**. To add to positions, raise "Max open copy buys" in advanced settings — **the maximum is All (unlimited)**.

**Is the default slippage in settings 30% or 15%?**

It's now **15%**, adjustable from 1% to 100%.

**Is there an official "Ratio guide" in the App too?**

Yes. Tap **Ratio guide** in the top-right of Ratio mode (or on the settings page) to open it. That's the platform's own detailed version; this page is the full explanation for beginners.

***

## Related pages

- Walk through it step by step: [How to Copy a Trader](how-to-follow.md)
- What each parameter means: [Copy Settings](settings.md)
- How to manage after enabling: [Managing Copies](managing.md)
- Try it without spending money first: [Simulation Copy Trading](simulation.md)
