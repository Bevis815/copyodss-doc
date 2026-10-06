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
| Receiving address | Must be able to receive Polygon USDC; **do not** enter the custodial address from the deposit page |
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

Every withdrawal must be confirmed with an **Authenticator (TOTP)** code.

If you haven't set up an Authenticator, the system will guide you to enable it in Settings; **you can't withdraw without it**.

Passkeys and email codes are only for login and similar scenarios and **cannot** be used to confirm withdrawals.

See [Withdrawal Security](../security/withdrawal-security.md) and [Two-Factor Authentication (2FA)](../security/2fa.md).

***

## Temporarily unable to withdraw?

Possible reasons:

- A withdrawal cooldown triggered by a new-device login or security policy
- Trading status is restricted
- Step-up verification failed / expired
- Address or amount validation failed

Check sessions and security settings in **Settings → Devices / Security**. If it still fails, contact support and mention whether you recently switched devices.

***

## Safety tips

- Before your first large withdrawal: test with a small amount first
- Withdrawals usually can't be undone once submitted — check the address character by character
- CopyOdds will never DM you to "help with a withdrawal" or ask for your verification codes
