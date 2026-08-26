# Managing Copy Traders

在 **My copies（我的跟单）** → `/copy-rules` 管理全部跟单规则。

![我的跟单](../.gitbook/assets/my_copies_doc.png)

***

## 页面顶部汇总（常见）

| 字段 | 含义 |
|------|------|
| Realized（已实现） | 已平仓实现的盈亏 |
| Position（持仓） | 当前持仓市值类汇总 |
| Unrealized（未实现） | 浮动盈亏 |
| Win Rate | 胜场 / 负场相关统计 |

未创建任何规则时，页面可能显示新手引导：登录 → 充值 → 买 Gas → 开始跟单。

***

## 规则状态

| 状态 | 含义 | 你要做什么 |
|------|------|------------|
| **Following** | 正常跟单中 | 日常观察交易记录即可 |
| **Manually paused** | 你主动暂停 | 需要时 Resume |
| **Funding alert** | 资金 / Gas 等问题导致买单受影响 | 充值或买 Gas 后点 **Resume buys** |

> 资金不足时规则**常常仍保持开启**，只是买单被跳过——这是刻意设计，方便你在补仓后继续跟卖已有持仓。

***

## 单条规则可做的操作

| 操作 | 说明 |
|------|------|
| Pause / Resume | 暂停或恢复整条规则 |
| Resume buys | 清除资金提醒后继续跟买 |
| Edit | 修改金额、比例、滑点等 |
| Delete | 删除规则（历史记录通常仍保留） |
| Positions / Activity / Detail | 跳到持仓、动态或详情 |

也支持批量暂停 / 恢复 / 删除（以界面为准）。

***

## 停止 vs 删除

| | 停止（Pause） | 删除（Delete） |
|--|---------------|----------------|
| 之后还能不能快速恢复 | 可以 Resume | 需重新创建规则 |
| 历史交易记录 | 保留 | 通常仍保留 |
| 已有持仓 | **不会**自动卖出 | **不会**自动卖出 |

持仓请到 **Positions** 自行平仓或等待结算赎回。

***

## 相关页面

| 页面 | 路径 | 用途 |
|------|------|------|
| Copy activity | `/feed` | 看 leader 公开成交与跟单状态标签 |
| Trade history | `/executions/records` | 你的成交结果 |
| Positions | `/executions/positions` | 持仓与平仓 |
| Daily P&L | `/executions/daily-pnl` | 每日已实现盈亏 |

![动态页](../.gitbook/assets/feed_doc.png)

动态上的状态标签用于理解「这笔公开成交有没有尝试跟」，**最终以交易记录为准**。
