# Transaction History

**Transaction history** records every fund movement in and out of your account, plus Gas spending — think of it as a bank statement.

Entry: **Transaction history** → `/wallets/ledger` (usually reachable from the deposit / withdraw pages)

***

## Table fields

| Field | Meaning |
|-------|---------|
| **Network / Asset** | e.g. Polygon (PoS) + USDC, BSC + USDT, Platform + Gas |
| **Type (In / Out)** | Incoming or outgoing |
| **Status** | Received, Completed, Posted |
| **Balance after** | How much is left in the account after this entry |
| **View on-chain** | Open this transaction in a block explorer |

Three kinds of records:

| Type | Description |
|------|-------------|
| **Deposit** | USDC / USDT transferred in from an external wallet |
| **Withdrawal** | Sent to your own address |
| **Gas spending** | Service-fee credits deducted for each copy fill |

***

## When the numbers don't add up

| Symptom | What to check |
|---------|---------------|
| Deposit not showing | Was the network correct, is the asset USDC/USDT, does the address exactly match the page for that network, is it confirmed on-chain (BSC is slower)? |
| Withdrawal stuck "Processing" | You need to complete withdrawal step-up verification first; there may be a cooldown after a new device or risk-related change |
| More Gas deducted than expected | Every buy and sell is charged about 0.5% of the fill amount; compare against the example in [Platform Gas](gas.md) |
| Balance doesn't match positions | Positions and open orders tie up funds; go by **Max withdrawable** |

If you can't find it, send support the **time, amount, and status** from the ledger along with the on-chain hash.
