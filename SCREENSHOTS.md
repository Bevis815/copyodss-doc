# 截图准备清单

把 PNG 放到 `.gitbook/assets/`，文件名建议与下表一致，便于直接替换文档中的引用。

**拍摄建议：** 桌面宽度约 1280–1440；关键步骤用英文界面拍一版即可（与 App 默认文案一致）；可另附中文界面。打码邮箱、地址中间段、二维码可保留完整（文档需要对照）。

---

## P0 — 必须（上线文档优先）

| 文件名 | 拍什么 | 要点 |
|--------|--------|------|
| `login_doc.png` | 登录页 | 邮箱 + 验证码；能看到 Passkey / Telegram 入口更佳 |
| `usdc1_doc.png` | 充值页 | **网络下拉可见 Polygon / BSC**；地址或二维码；「校验充值地址」按钮 |
| `store_doc.png` | Gas 商城 | Gas 余额、USDC 余额、套餐卡片、0.5% 说明文案 |
| `smarket_doc.png` | 聪明钱榜单 | 搜索、分类/筛选、至少 3 张交易员卡片、Follow 按钮 |
| `follow_doc.png` | 跟单向导 | 金额/比例步骤 + 滑点；或高级设置（方向、最多跟买笔数） |
| `my_copies_doc.png` | 我的跟单 | 顶部汇总 + 至少一条 Following / Funding alert 规则 + 操作菜单 |
| `change_doc.png` | 交易记录 | 今日/累计盈亏 + 含「已成交 / 跳过」等状态的列表 |

## P1 — 重要

| 文件名 | 拍什么 | 要点 |
|--------|--------|------|
| `usdc2_doc.png` | 提现页 | Polygon-only 提示、最大可提、地址与金额表单 |
| `withdraw_stepup_doc.png` | 提现二次验证弹窗 | 能看出 Authenticator / Passkey / 邮箱选项 |
| `trader_profile_doc.png` | 交易员详情 | 评分卡、核心指标、Follow |
| `settings_security_doc.png` | 设置 → 安全 | Authenticator、Passkeys、Devices、提现二次验证 |
| `feed_doc.png` | 动态页 | 带单公开成交 + Copied / Skipped 等状态 |
| `positions_doc.png` | 持仓页 | 持仓卡片与平仓入口（可选写入 managing 文） |

## P2 — 加分

| 文件名 | 拍什么 | 要点 |
|--------|--------|------|
| `wallet_security_doc.png` | `/wallets/security` | 独立钱包 / 私钥隔离 / 提现保护 |
| `verify_deposit_doc.png` | 校验充值地址成功弹窗 | Telegram bot 或邮箱指引 |
| `deposit_network_select_doc.png` | 选择充值网络底部弹层 | Polygon vs BSC 对比文案 |
| `gas_empty_resume_doc.png` | 我的跟单资金提醒 | Funding alert + Resume buys |
| `daily_pnl_doc.png` | 每日盈亏 | 曲线或日列表 |

---

## 旧图处理

`.gitbook/assets/` 里已有部分旧截图（`login_doc.png`、`usdc1_doc.png` 等）。**充值相关旧图若仍只显示 Polygon、或文案写「勿用 BSC」，请重拍替换**——当前产品已支持 BSC 充值。

登录旧图若仍是「名/姓注册表单」，建议换成当前「邮箱验证码自动开户 + Passkey/Telegram」界面。

---

## 文档内引用关系（便于你对照）

| 截图 | 出现在 |
|------|--------|
| login | Quick Start |
| usdc1 / store / smarket / follow | Quick Start、Deposit、GAS、Leaderboard、Follow |
| my_copies / feed / change | Managing、How Copy Trading Works |
| usdc2 / withdraw_stepup | Withdraw、Withdrawal Security |
| trader_profile | Trader Profile |
| settings_security | 2FA |
| wallet_security / verify_deposit | Wallet Security、Anti-Phishing |
