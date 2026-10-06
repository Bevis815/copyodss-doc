# Supported Networks

Deposits and withdrawals support **different networks**. Always choose exactly as the page shows to avoid funds not arriving.

***

## Overview

| Action | Supported networks | Assets | Address type |
|--------|--------------------|--------|--------------|
| **Deposit** | **Polygon (PoS)**, **BSC** (when enabled) | USDC / USDT | Different address per network |
| **Withdraw** | **Polygon (PoS) only** | **USDC** | Your own receiving address |

Examples of networks not supported for deposits: **Ethereum mainnet, Arbitrum, Optimism**, etc. (unless the product explicitly adds them in the future).

***

## Polygon (PoS)

| Item | Description |
|------|-------------|
| Deposit | Supported; the address shown is your custodial wallet address (Custodial address) |
| Assets | USDC, USDT |
| Withdraw | The **only** withdrawal network; withdraw USDC to an address that can receive Polygon USDC |

Most users prefer Polygon: the path is more direct and matches the withdrawal network.

***

## BSC

| Item | Description |
|------|-------------|
| Deposit | Supported (when bridging / the product network is enabled) |
| Assets | USDC, USDT |
| Address | **Bridge address**, different from the Polygon address |
| Withdraw | Withdrawing from CopyOdds to BSC is **not supported** |

When withdrawing from an exchange via BSC, switch the deposit page to BSC first, then copy the address. Arrival may take a few extra minutes.

***

## Common mistakes

| Mistake | Consequence |
|---------|-------------|
| Withdrawing on BSC but copying the Polygon address | May not be credited / hard to recover |
| Withdrawing on Polygon but copying the BSC address | Same as above |
| Sending Ethereum USDC | Usually not credited automatically |
| Entering the deposit page address as the withdrawal address | Funds may go back to the custodial side and cause confusion; withdrawals should go to **your own** external address |
| Expecting to withdraw to BSC | Withdrawals currently support Polygon USDC only |

***

## Rules of thumb

1. **Pick the network first, then copy the address**
2. **Deposit on Polygon, withdraw on Polygon — simplest**
3. **BSC is deposit-only; you can't withdraw to BSC from this App**
4. **Only use the address from the official page + the Verify deposit address feature**
