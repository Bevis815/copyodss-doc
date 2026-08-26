# Withdrawal Security

提现会把资金转到外部地址，因此每次提现都需要 **step-up（二次验证）**。当前仅支持 **Authenticator（TOTP）**。

![提现二次验证](../.gitbook/assets/withdraw_stepup_doc.png)

***

## 验证方式

- **唯一方式：Authenticator 动态验证码**（Google / Microsoft Authenticator、1Password 等）
- 未绑定 Authenticator 时，提现流程会要求先前往设置开启
- **Passkey、邮箱验证码不能用于提现**（仍可用于登录等）

可在设置中查看「提现二次验证」说明。

***

## 提现时怎么做

1. 确认已绑定 Authenticator
2. 在提现页填好 Polygon 地址与金额并核对
3. 进入二次验证弹窗，输入 6 位动态码
4. 验证通过后再提交提现

验证码错误或过期时，重新输入当前码即可。

***

## 额外保护

| 机制 | 说明 |
|------|------|
| 最大可提 | 持仓与挂单占用不可提 |
| 新设备 / 安全冷却 | 新设备或风险变更后可能暂时无法提现 |
| 交易状态限制 | 账户若被限制交易，提现也可能受影响 |
| 地址核对 | 填错外部地址通常无法追回 |

***

## 安全提示

- 不要向自称客服的人提供 Authenticator 验证码
- 不要把提现地址改成「对方提供的中间地址」
- 官方邮件域名相关提示见 [Anti-Phishing](anti-phishing.md)
- 大额前提：小额试提 → 确认到账 → 再提大额
