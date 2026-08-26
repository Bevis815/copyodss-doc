# CopyOdds 使用文档

CopyOdds 是基于 [Polymarket](https://polymarket.com) 的**聪明钱分析 + 自动跟单**平台：发现表现较好的预测市场交易员，用托管交易账户自动镜像其成交。

本文档对应当前 App（`app.copyodds.io`）界面与流程。页面文案以英文界面为主时，文中会同时标注中文导航名。

## 四步上手

1. **登录 / 注册** — 邮箱验证码、Passkey 或 Telegram
2. **充值** — 向托管地址转入 Polygon 或 BSC 上的 USDC / USDT
3. **购买平台 Gas** — 支付自动跟单服务费点数（不是链上 MATIC）
4. **跟单** — 在「聪明钱」挑选交易员 → 点 **Follow（跟单）** → 保存规则

## 开始跟单前请确认

| 项目 | 要求 |
|------|------|
| 平台 Gas | **大于 0**（否则无法开启跟单；Gas 用尽后买单会跳过） |
| USDC 余额 | 建议至少约 **$1**，用于实际买入 |
| 交易账户 | 登录后通常自动开通 |

## 主要入口（与 App 导航一致）

| 功能 | 路径 / 导航 |
|------|-------------|
| 聪明钱排行榜 | **Smart money** → `/smart-money`（首页即此） |
| 我的跟单 | **My copies** → `/copy-rules` |
| 交易账户 / 充值提现 | **Assets / Deposit** → `/wallets/deposit` |
| Gas 商城 | **Gas Store** → `/store` |
| 持仓 / 交易记录 | **Positions** / **Trade history** |
| 用户指南 | **Getting started** → `/help` |
| 设置与安全 | **Settings** |

## 文档说明

- 左侧目录按产品模块划分，建议按 **Getting Started → Wallet → Smart Money → Copy Trading** 阅读。
- 文中 `![...]` 处为建议截图占位；截图清单见文末「需要准备的截图」。
- 本文档仅作产品操作说明，**不构成投资建议**。

## 联系支持

请准备：注册邮箱、操作时间、错误截图，以及「交易记录」中的相关编号 / 状态。

---

## 需要准备的截图（总览）

按优先级准备即可；文件建议放到 `.gitbook/assets/`，命名示例见各页。

| 优先级 | 截图 | 用于页面 |
|--------|------|----------|
| P0 | 登录页（邮箱 + Passkey / Telegram） | Quick Start |
| P0 | 充值页：网络选择（Polygon / BSC）+ 地址 / 二维码 | Deposit |
| P0 | Gas 商城：套餐列表 + 余额 | GAS |
| P0 | 聪明钱排行榜（卡片列表 + 筛选） | Leaderboard |
| P0 | 跟单向导（金额 / 比例 + 滑点） | How to Follow / Settings |
| P0 | 我的跟单列表（状态 + 操作菜单） | Managing |
| P1 | 交易员详情 / 评分卡 | Trader Profile |
| P1 | 提现页 + 二次验证弹窗 | Withdraw / Withdrawal Security |
| P1 | 交易记录 / 持仓 | How Copy Trading Works / FAQ |
| P1 | 设置 → 安全（Authenticator / Passkey / 设备） | 2FA |
| P2 | 动态页（Copy activity） | Managing |
| P2 | 资产安全保障页 | Wallet Security |
| P2 | 「校验充值地址」成功提示 | Anti-Phishing |
