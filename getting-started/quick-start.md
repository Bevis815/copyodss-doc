# 快速开始

从打开 App 到第一条跟单规则，按下面做即可。官方地址请使用 **copyodds.io / app.copyodds.io**。

![登录页](../.gitbook/assets/login_doc.png)

***

## 1. 登录或创建账户

1. 打开 App，进入 **Login**。
2. 输入邮箱 → **发送验证码** → 填写 6 位验证码 → 登录。
3. **新邮箱会自动创建账户**（无需再填姓名走单独注册页；若界面仍有姓名/条款，按提示完成即可）。
4. 可选：使用 **Passkey（通行密钥）** 或 **Telegram** 登录。
5. 通过邀请链接进入时，邀请码通常会自动带入。

### 注意

- 验证码一般约 5 分钟有效；发送后短时间不可重复发送
- 收不到邮件时检查垃圾箱 / 促销分类
- Passkey 需在支持的设备与浏览器上绑定（设置页可管理）

***

## 2. 开通交易账户并完成授权

1. 打开 **交易账户（Wallets）** → `/wallets`
2. 点 **开通交易账户**，阅读并勾选协议后确认
3. 在 **Agent 授权** 区块点 **立即授权**，用**注册时那个钱包**签名（钱包需切到 Polygon）
4. 确认页面显示 **Polymarket 已就绪**（否则无法跟单下单）

详见 [开通交易账户与授权](../wallet/trading-account.md)。

> 只想先看看、不打算马上交易？这一步可以晚点做，但**不完成授权就无法跟单**。

***

## 3. 充值 USDC / USDT

1. 打开 **Assets / Deposit（钱包 · 充值）** → `/wallets/deposit`
2. **选择网络**：Polygon (PoS) 或 BSC（与交易所提现网络一致）
3. **选择资产**：仅 USDC 或 USDT
4. 复制本页地址或扫码转账（**Polygon 与 BSC 地址不同，切勿混用**）
5. 等待链上确认；BSC 可能多等几分钟

![充值页](../.gitbook/assets/usdc1_doc.png)

详见 [充值](../wallet/deposit.md)、[支持的网络](../wallet/supported-networks.md)。

***

## 4. 购买平台 Gas

1. 打开 **Gas Store（Gas 商城）** → `/store`
2. 查看当前 Gas 与 USDC 余额
3. 选择套餐 → 用托管 USDC 购买
4. Gas 即时到账（不可提现）

![Gas 商城](../.gitbook/assets/store_doc.png)

费率简述：每笔跟单成交按名义金额约 **0.5%** 扣 Gas；**1 USDC ≈ 100 Gas**。详见 [平台 Gas](../wallet/gas.md)。

***

## 5. 挑选交易员并跟单

1. 打开首页 **排行榜（Leaderboard）** 或 **Smart money（聪明钱）** → `/` 或 `/smart-money`
2. 用分类、快速筛选或高级筛选挑人
3. 点 **Follow（跟单）**，或进入详情后再跟单
4. 选择**跟单模式**（默认「比例」）、滑点、高级选项
5. 确认 Gas > 0 后保存 → 在 **My copies（我的跟单）** 管理

![聪明钱 + 跟单](../.gitbook/assets/smarket_doc.png)

![跟单设置](../.gitbook/assets/follow_doc.png)

***

## 6. 确认是否跟单成功

| 页面 | 用途 |
|------|------|
| **My copies** | 规则是否在跟、是否资金提醒 |
| **Trade history（交易记录）** | 你的订单是否成交 / 跳过 / 失败 |
| **Copy activity（动态）** | 交易员公开动作（**不是**你的成交结果） |
| **Positions（持仓）** | 当前持仓，可平仓 / 赎回 |

***

## 新手建议

- 先小额充值、买少量 Gas、用较小固定金额测试 1–2 天
- 资金或 Gas 不足时：买单会跳过，规则通常**不会**自动暂停；补足后到「我的跟单」点 **Resume buys（恢复买单）**
- 提现仅支持 **Polygon USDC**，提交前务必核对地址

***

## 拿不准跟谁？三个安全做法

1. **先看排行榜**（首页）找到近期表现稳定的账户
2. **进详情页跑一次 [跟单回测](../smart-money/backtest.md)**，用保守参数看看「跳过」多不多
3. **仍不放心就先 [模拟跟单](../copy-trading/simulation.md)**，不动真钱

确认没问题再回到本页步骤 4 开正式跟单。
