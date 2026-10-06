# Platform Gas

**Platform Gas** is a **service-fee credit** inside your CopyOdds account, used to pay fees on automated copy fills.

> **Platform Gas ≠ on-chain gas.** It is not MATIC, POL, or BNB, and not the gas you use in a wallet to pay network fees.

Entry: **Gas Store** → `/store`.

![Gas Store](../.gitbook/assets/store_doc.png)

***

## Why do you need Gas?

Each copy fill (buy or sell) deducts service-fee credits based on the fill's notional amount. Without Gas:

- **You can't create or resume copy rules**
- Under existing rules, **buys are usually skipped**
- If you still hold positions, **sells may still be copied** (rules often stay running)

***

## Fees (current product terms)

| Item | Description |
|------|-------------|
| Fee | About **0.5%** of the notional amount per copy fill, deducted in Gas |
| Conversion | About **1 USDC = 100 Gas** |
| Example | A $100 fill consumes about **50 Gas** |
| Payment source | Packages are paid from your custodial **available USDC balance** |
| Withdrawable? | **No** — cannot be withdrawn or transferred |

See the store page for current packages and any bonuses (such as referral tier boosts).

***

## How to buy

1. Open Gas Store and make sure you have enough USDC
2. Read the fee description
3. Pick a package → confirm payment
4. Gas is credited instantly
5. If buys were previously skipped due to insufficient Gas: go to **My copies** and tap **Resume buys**

***

## Gas vs. USDC

| | USDC | Platform Gas |
|--|------|--------------|
| Purpose | Copy principal | Copy service fee |
| How to get it | On-chain deposit | Buy with USDC in the store |
| Can it be withdrawn on-chain? | Yes (see Withdraw) | No |

***

## FAQ

**Do I need to do anything after buying Gas?**  
We recommend going to **My copies** and tapping **Resume buys** to clear any funding alert.

**Will my rules stop when Gas runs out?**  
Usually the whole rule isn't paused — buys are skipped, and sells may still be copied if you hold positions.
