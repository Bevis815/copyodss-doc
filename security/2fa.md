# 2FA

CopyOdds 登录默认是**邮箱验证码**（无传统密码）。建议再开启下面的第二因素，提升登录与提现安全。

![设置安全](../.gitbook/assets/settings_security_doc.png)

_建议截图：Settings → Security — Authenticator、Passkeys、Devices、提现二次验证说明_

***

## 可用方式

| 方式 | 用途 |
|------|------|
| **邮箱 OTP** | 登录、绑定验证、提现兜底 |
| **Authenticator（TOTP）** | 推荐用于提现确认；Google / Microsoft Authenticator、1Password 等 |
| **Passkey** | 面容 / 指纹 / 屏幕锁；可用于登录与提现确认 |
| **Telegram** | 可选登录 / 绑定方式（以设置页为准） |
| **设备管理** | 查看并移除设备；新设备可能影响提现 |

***

## 建议开启顺序

1. 绑定并验证邮箱
2. 开启 **Authenticator**
3. 在常用设备添加 **Passkey**
4. 熟悉 **Devices** 列表，不认识的设备及时移除

***

## Authenticator（TOTP）

1. 打开 **Settings → Security**
2. 按指引用 Authenticator App 扫码 / 录入密钥
3. 输入 6 位动态码完成开启

开启后，提现会**优先**要求 Authenticator 验证码。

***

## Passkey（通行密钥）

1. 在支持的浏览器 / 系统中打开设置
2. 添加 Passkey，按系统提示完成生物识别或屏幕锁
3. 登录页可选择 Passkey 快速登录
4. 未开 Authenticator 时，提现可能优先使用 Passkey

注意：不同浏览器、WebView、系统版本支持程度不同；失败时可回退邮箱验证码。

***

## 设备与会话

- 在 `/settings/devices` 查看登录设备
- 新设备或新环境登录后，**提现可能被临时锁定**一段时间（安全冷却）
- 不要在公用电脑勾选长期信任未知扩展或保存验证码到不安全位置

***

## 丢失验证器怎么办？

若仍能登录邮箱：

1. 使用邮箱验证码登录
2. 在设置中重新绑定 Authenticator / Passkey
3. 检查设备列表并移除丢失设备

若邮箱也无法访问：联系支持并准备身份核验材料（以客服流程为准）。
