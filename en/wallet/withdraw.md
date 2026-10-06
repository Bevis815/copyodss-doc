# Withdraw

Withdraw freely available **USDC** from your trading account to an external wallet. Entry: **Wallets → Withdraw** → `/wallets/withdraw`.

![Withdraw page](../.gitbook/assets/usdc2_doc.png)

![Withdrawal step-up verification](../.gitbook/assets/withdraw_stepup_doc.png)

***

## Withdrawal rules

| Item | Description |
|------|-------------|
| Network | **Polygon (PoS) only** |
| Asset | **USDC** |
| Receiving address | Must be able to receive Polygon USDC; **do not** enter the custodial address from the deposit page, and it can't be **your current deposit address itself** |
| Destination wallet | Should hold a little **MATIC (POL)**; you'll need it to pay gas when moving this USDC on-chain later |
| Step-up verification | Required for every withdrawal (see below) |

***

## Steps

1. Open the withdraw page and check **Max withdrawable** (may be less than your total balance)
2. Enter a Polygon receiving address and amount
3. Double-check the network, address, and amount
4. Tap continue and complete **withdrawal step-up verification**
5. After submitting, track the status in your statements / records

***

## Why is "Max withdrawable" less than my balance?

The following funds usually can't be withdrawn immediately:

- Funds tied up in open positions
- Funds frozen in unfilled orders
- Other margin / funds locked by the system

Go by the **Max withdrawable** figure on the page, not your total balance.

***

## Withdrawal step-up verification

Every withdrawal must be confirmed with a 6-digit **Authenticator (TOTP)** code — **currently this is the only supported method**.

If you haven't set one up, the system will guide you to enable it in Settings; **you can't withdraw without it**.

**Passkeys and email codes cannot be used to confirm withdrawals** (they're only for login and similar scenarios).

See [Withdrawal Security](../security/withdrawal-security.md) and [Two-Factor Authentication (2FA)](../security/2fa.md).

***

## Temporarily unable to withdraw?

| Message | Meaning | What to do |
|---------|---------|------------|
| **Withdrawal channel busy** | Many withdrawal requests today | Wait a few minutes or hours as prompted; **your funds are safe and you don't need to resubmit** |
| **New device / new network cooldown** | You just switched devices or your IP changed | Try again after the cooldown ends |
| **Unfilled orders exist** | You still have open orders | Cancel them or wait for them to fill |
| **Positions still open** | Your custodial address still holds market positions | Close them or wait for settlement |
| **Previous withdrawal in progress** | Still being confirmed on-chain | Wait for it to finish before sending the next one |
| **Address is your deposit address** | You can't withdraw back to your deposit address | Use your own receiving address instead |

Check sessions and security settings in **Settings → Devices / Security**. If it still fails, contact support and mention whether you recently switched devices.

***

## Safety tips

- Before your first large withdrawal: test with a small amount first
- Withdrawals usually can't be undone once submitted — check the address character by character
- CopyOdds will never DM you to "help with a withdrawal" or ask for your verification codes

***

## Where to see withdrawal records

**Transaction history** → `/wallets/ledger` shows each withdrawal's status and "balance after", with a link to the block explorer. See [Transaction History](ledger.md).
