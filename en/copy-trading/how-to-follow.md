# How to Copy a Trader

Add a smart money address to automated copying and save the rule.

![Copy wizard](../.gitbook/assets/follow_doc.png)

***

## Pre-flight checklist

| Condition | Notes |
|-----------|-------|
| Logged in with an active trading account | Usually opened automatically after login |
| Platform Gas > 0 | **Required**; otherwise you can't enable / resume |
| Available USDC balance | About $1 or more recommended; otherwise buys are likely skipped |

***

## Entry points

Any of the following:

1. Tap **Follow** on the **Smart money** list or a profile page
2. **Quick copy / New copy** in **My copies**
3. Open `/copier` (Quick copy) directly and paste an address
4. Open a profile link `https://app.copyodds.io/@0x...` and tap Follow

***

## Steps

1. Confirm the **Leader address** (0x…); bringing it over from the leaderboard avoids typos
2. Optional: name the rule (Name this copy trade)
3. Choose a **Copy mode** — pick one of three:
   - **Ratio** — **The default mode**; copies a fixed percentage of each of the leader's fills (leader buys $500 at a 10% ratio → you buy $50)
   - **By balance %** — A percentage of **your available USDC** (1%–100%)
   - **Fixed amount** — Buys the same amount every time (minimum $1)
4. Set **Slippage tolerance** — default **15%**, adjustable from 1% to 100%

   > For how the three modes differ, how the ratio is calculated, and where the suggested values come from, see [The Three Copy Modes](copy-modes.md)
5. Optionally open **Advanced settings**:
   - **Direction**: Both / Buy only / Sell only
   - **Max open copy buys**: default **1** (no adding to positions); the maximum is **All (unlimited)**
6. Save (**Copy trade / Save**)
7. Go to **My copies** and confirm the status is **Following**

***

## Fixed amount vs. % of balance

| Mode | Behavior | Best for |
|------|----------|----------|
| Fixed amount | Whether the trader buys $50 or $500, you copy with your set amount | Controlling per-trade risk |
| % of balance | Copies buys with a % of your available balance at that moment | Scaling automatically with your capital |

If the amount calculated from the percentage is below the minimum order size, the system may raise it to the minimum before trying.

***

## Notes

- Each leader address usually has only one active set of settings; saving again overwrites it
- Changing a rule only affects future copies and doesn't rewrite past fills
- Stopping / deleting a rule **does not** automatically sell your positions
- Test with a small amount first, and only scale up after Trade history looks normal

***

## Where to look after copying

| What you want to see | Where to go |
|----------------------|-------------|
| What the trader just did, and whether I copied it | [Copy Activity](copy-activity.md) |
| What I currently hold | [My Positions & Trade History](positions-and-records.md) |
| Rule status, pause / resume | [Managing Copies](managing.md) |
