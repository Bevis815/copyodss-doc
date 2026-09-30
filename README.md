# CopyOdds 使用文档

CopyOdds 是基于 [Polymarket](https://polymarket.com) 的**聪明钱分析 + 自动跟单**平台：发现表现较好的预测市场交易员，用托管交易账户自动镜像其成交。

本文档对应当前 App（`app.copyodds.io`）界面与流程。页面文案以英文界面为主时，文中会同时标注中文叫法。

## 四步上手

1. **登录 / 注册** — 邮箱验证码、Passkey 或 Telegram
2. **充值** — 向托管地址转入 Polygon 或 BSC 上的 USDC / USDT
3. **购买平台 Gas** — 支付自动跟单服务费点数（不是链上 MATIC）
4. **跟单** — 在「排行榜」或「聪明钱」挑交易员 → 点 **Follow（跟单）** → 选跟单模式（默认「比例」）→ 保存规则

完全不懂从哪开始？先看 [界面导航一览](getting-started/app-tour.md)。

## 开始跟单前请确认

| 项目 | 要求 |
|------|------|
| 平台 Gas | **大于 0**（否则无法开启跟单；Gas 用尽后买单会跳过） |
| USDC 余额 | 建议至少约 **$1**，用于实际买入 |
| 交易账户 | 登录后通常自动开通 |

## 主要入口（与 App 导航一致）

| 功能 | 路径 / 导航 |
|------|-------------|
| 排行榜（跟单池每日盈利） | **Leaderboard** → `/`（首页） |
| 聪明钱 | **Smart money** → `/smart-money` |
| 我的跟单 | **My copy trading** → `/copy-rules` |
| 跟单动态 | **Copy activity** → `/feed` |
| 模拟跟单 | **Simulation copy trading** → `/copy-trading/simulation` |
| 我的持仓 | **My positions** → `/executions/positions` |
| 交易记录 / 盈亏 | **Executions** → `/executions/records`、`/executions/daily-pnl` |
| 平台 Gas 商城 | **Store** → `/store` |
| 邀请返佣 | **Affiliation** → `/affiliate` |
| 充值 / 提现 | **Deposit / Withdraw** → `/wallets/deposit`、`/wallets/withdraw` |
| 个人中心（资产总览） | **Profile** → `/profile` |
| 资金流水 | **Transaction history** → `/wallets/ledger` |
| 设置与安全 | **Settings** → `/settings` |
| 设备与 Passkey | **Settings → Devices** → `/settings/devices` |
| 手机端下载 | **Mobile App** → `/mobile-app` |
| 用户指南 | **User guide** → `/help` |

## 建议阅读顺序

1. **入门指南**（是什么 → 快速开始 → 界面导航）
2. **排行榜 / 聪明钱**（挑人，并用回测先试）
3. **跟单**（怎么开、怎么管、怎么检查）
4. **钱包**（充值、Gas、提现、流水）
5. **账户与设置、安全**（保护好账户）
6. **邀请返佣**（想赚钱分享时再看）

## 文档说明

- 本文档仅作产品操作说明，**不构成投资建议**。
- 界面持续更新，若截图与你的版本略有差异，以 App 实际显示为准。

## 联系支持

请准备：注册邮箱、操作时间、错误截图，以及「交易记录」中的相关编号 / 状态 / 链上哈希。
