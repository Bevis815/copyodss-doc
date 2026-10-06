# Withdrawal Security

Withdrawals move funds to an external address, so every withdrawal requires **step-up verification**. Currently only **Authenticator (TOTP)** is supported.

![Withdrawal step-up verification](../.gitbook/assets/withdraw_stepup_doc.png)

***

## Verification method

- **The only method: an Authenticator code** (Google / Microsoft Authenticator, 1Password, etc.)
- If no Authenticator is bound, the withdrawal flow will ask you to enable one in Settings first
- **Passkeys and email codes cannot be used for withdrawals** (they still work for login, etc.)

You can find the "Withdrawal step-up verification" description in Settings.

***

## What to do when withdrawing

1. Make sure an Authenticator is bound
2. Fill in the Polygon address and amount on the withdraw page and double-check them
3. In the step-up verification dialog, enter the 6-digit code
4. Submit the withdrawal after verification passes

If the code is wrong or expired, just enter the current code again.

***

## Extra protection

| Mechanism | Description |
|-----------|-------------|
| Max withdrawable | Funds tied up in positions and orders can't be withdrawn |
| New device / security cooldown | Withdrawals may be temporarily unavailable after a new device or risk-related change |
| Trading restrictions | If the account's trading is restricted, withdrawals may also be affected |
| Address check | Funds sent to a wrong external address usually can't be recovered |

***

## Safety tips

- Never give your Authenticator code to anyone claiming to be support
- Never change the withdrawal address to an "intermediate address" someone gives you
- For official email domain guidance, see [Anti-Phishing](anti-phishing.md)
- Before a large withdrawal: test with a small amount → confirm it arrives → then withdraw more
