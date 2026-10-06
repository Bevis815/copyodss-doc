# 教程视频清单与接入任务

> 本文件是**给智能体/开发同事执行的工作单**，不是终端用户文档。
> 终端用户看的教程说明在 `getting-started/`、`wallet/`、`copy-trading/` 等目录里。

---

## 一、这是什么

CopyOdds 官方 Telegram 频道 `@CopyOddsApp` 上发布的一批**操作教学视频**，覆盖 4 个主题 × 多种语言。视频同时也是 App 内「观看教程」(`/guide-video`) 的素材来源。

**频道地址：** https://t.me/CopyOddsApp

---

## 二、原始链接清单（逐字保留）

```
https://t.me/CopyOddsApp/2    id 的充值视频
https://t.me/CopyOddsApp/3    ko 的充值视频
https://t.me/CopyOddsApp/4    ru 的充值视频
https://t.me/CopyOddsApp/5    en 的充值视频
https://t.me/CopyOddsApp/6    fr 的充值视频
https://t.me/CopyOddsApp/7    fr 的参数说明视频
https://t.me/CopyOddsApp/8    fr 的聪明钱说明视频
https://t.me/CopyOddsApp/9    fr 的提现视频
https://t.me/CopyOddsApp/10   id 的参数说明视频
https://t.me/CopyOddsApp/11   id 的聪明钱说明视频
https://t.me/CopyOddsApp/12   id 的提现说明视频
https://t.me/CopyOddsApp/13   ko 的参数说明
https://t.me/CopyOddsApp/14   ko 的聪明钱说明
https://t.me/CopyOddsApp/15   ko 的提现说明
https://t.me/CopyOddsApp/16   ru 的参数说明
https://t.me/CopyOddsApp/17   ru 的聪明钱说明
https://t.me/CopyOddsApp/18   ru 的提现说明
```

---

## 三、规范化对照表

| # | 链接 | 语言 | 主题 | 对应 App 页面 |
|---|------|------|------|-------------|
| 2 | https://t.me/AITrading_io/5308 | id | 充值 | 交易账户 / Deposit |
| 3 | https://t.me/AITrading_io/5312 | ko | 充值 | 交易账户 / Deposit |
| 4 | https://t.me/AITrading_io/5316 | ru | 充值 | 交易账户 / Deposit |
| 5 | https://t.me/AITrading_io/5319 | en | 充值 | 交易账户 / Deposit |
| 6 | https://t.me/AITrading_io/5303| fr | 充值 | 交易账户 / Deposit |
| 7 | https://t.me/AITrading_io/5302 | fr | 参数说明 | 我的跟单 / 跟单设置 |
| 8 | https://t.me/AITrading_io/5304 | fr | 聪明钱说明 | 聪明钱榜单 |
| 9 | https://t.me/AITrading_io/5306 | fr | 提现说明 | 提现 |
| 10 | https://t.me/AITrading_io/5307 | id | 参数说明 | 我的跟单 / 跟单设置 |
| 11 | https://t.me/AITrading_io/5309 | id | 聪明钱说明 | 聪明钱榜单 |
| 12 | https://t.me/AITrading_io/5310 | id | 提现说明 | 提现 |
| 13 | https://t.me/AITrading_io/5311 | ko | 参数说明 | 我的跟单 / 跟单设置 |
| 14 | https://t.me/AITrading_io/5313 | ko | 聪明钱说明 | 聪明钱榜单 |
| 15 | https://t.me/AITrading_io/5314 | ko | 提现说明 | 提现 |
| 16 | https://t.me/AITrading_io/5315| ru | 参数说明 | 我的跟单 / 跟单设置 |
| 17 | https://t.me/AITrading_io/5317 | ru | 聪明钱说明 | 聪明钱榜单 |
| 18 | https://t.me/AITrading_io/5318 | ru | 提现说明 | 提现 |
| 19 | https://t.me/AITrading_io/5321 en | 参数说明 | 我的跟单 / 跟单设置 |
| 20 | https://t.me/AITrading_io/5320 | en | 聪明钱说明 | 聪明钱榜单 |
| 21 | https://t.me/AITrading_io/5322 | en | 提现说明 | 提现 |

### 主题 → 代码里的 topic 标识

| 主题 | topic 标识 | CDN 文件名主干 |
|------|-----------|--------------|
| 充值 | `deposit` | `desposit`（**历史拼写错误，勿改**） |
| 参数说明 | `copy-rules` | `use` |
| 聪明钱说明 | `smart-money` | `smart` |
| 提现 | `withdraw` | `withdraw` |

---

## 四、覆盖情况与缺口

| 语言 | 充值 | 参数说明 | 聪明钱 | 提现 | 合计 |
|------|-----|---------|-------|-----|------|
| fr | ✅ #6 | ✅ #7 | ✅ #8 | ✅ #9 | 4 |
| id | ✅ #2 | ✅ #10 | ✅ #11 | ✅ #12 | 4 |
| ko | ✅ #3 | ✅ #13 | ✅ #14 | ✅ #15 | 4 |
| ru | ✅ #4 | ✅ #16 | ✅ #17 | ✅ #18 | 4 |
| **en** | ✅ #5 | ❌ | ❌ | ❌ | 1 |
| **zh-TW** | ❌ | ❌ | ❌ | ❌ | 0 |

**必须先确认的 3 件事：**

1. **zh-TW（繁体中文）一个都没有。** 这是 App 的默认兜底语言，缺中文视频影响最大——需向运营确认是否另有中文视频（推测在 #1 之前或之后的编号）。
2. **en 只有充值一支**，缺参数说明 / 聪明钱 / 提现。
3. **编号 #1 内容未知**，本次清单从 #2 开始。需打开频道确认 #1 是什么（很可能是 zh-TW 充值视频）。

---

## 五、交给智能体的任务

### 任务 A：把清单结构化并落库

1. 打开 https://t.me/CopyOddsApp 逐条核对 #1–#18，**确认每条的语言与主题**，补全上表。
2. 输出一份机器可读清单，建议格式（存为仓库内 `tutorial-videos.json` 或同等形式）：

```json
{
  "channel": "https://t.me/CopyOddsApp",
  "videos": [
    {
      "messageId": 2,
      "url": "https://t.me/CopyOddsApp/2",
      "locale": "id",
      "topic": "deposit",
      "verified": true,
      "note": ""
    }
  ]
}
```

3. `locale` 取值必须与 App 一致：`en` / `zh-TW` / `id` / `fr` / `ru` / `es` / `ko` / `hi`。
4. `topic` 取值必须是：`deposit` / `copy-rules` / `smart-money` / `withdraw`。

### 任务 B：接入 App 内「观看教程」

App 现有实现（供定位参考）：

- 页面：`froend/src/pages/GuideVideoPage.tsx`
- 取址逻辑：`froend/src/lib/guide-videos.ts`
- 现有视频源：`https://copyodds-media-1442243915.cos.ap-singapore.myqcloud.com/videos/{主干}[-{语言}].mp4`
- 已有本地化视频的语言：`fr` / `id` / `ru` / `ko`，其余语言回落到无后缀的默认文件

请完成：

1. 从 Telegram 频道**下载视频原始文件**，按现有命名规范上传 CDN：
   `desposit-fr.mp4` / `use-fr.mp4` / `smart-fr.mp4` / `withdraw-fr.mp4`（其余语言同理，**deposit 主干保持 `desposit` 拼写**）。
2. 补齐缺失组合，特别是 **en** 的 `use` / `smart` / `withdraw`。
3. 若 zh-TW 视频确认存在，zh-TW 属于「无后缀默认文件」那一份，需要**替换默认文件**而不是新增 `-zh-TW` 后缀文件；替换前先确认线上默认文件当前是哪一版。
4. 每个页面入口确认可用：
   - 充值页「观看教程」 → `/guide-video?topic=deposit&view=video`
   - 提现页「观看教程」 → `/guide-video?topic=withdraw&view=video`
   - 我的跟单页顶部入口 → `/guide-video?topic=copy-rules&view=video`
   - 聪明钱页 → `/guide-video?topic=smart-money&view=video`

### 任务 C：把视频入口写进用户文档

在以下页面的合适位置加入「观看教程」入口，**按语言给出对应链接**：

| 文档页面 | 挂哪个视频 |
|---------|-----------|
| `getting-started/quick-start.md` | 充值视频 |
| `wallet/deposit.md` | 充值视频 |
| `wallet/withdraw.md` | 提现视频 |
| `copy-trading/copy-modes.md` | 参数说明视频 |
| `copy-trading/settings.md` | 参数说明视频 |
| `smart-money/leaderboard.md` | 聪明钱说明视频 |

写法要求：

- 用统一的说明句式，例如「看不懂文字？观看「充值教程视频」（按你的语言给出链接）」
- **缺视频的语言不要留空链接**，改为提示「暂无该语言教程」或直接不展示该入口
- 不要改动现有正文的技术口径

---

## 六、验收标准

- [ ] #1–#18 全部核对完成，表格无空格、无猜测项
- [ ] `tutorial-videos.json` 可被程序读取，locale / topic 取值合法
- [ ] CDN 上 4 个主题 × 各有视频的语言，文件均存在且可播放
- [ ] App 内 4 个「观看教程」入口在对应语言下都能播到正确的视频，不出现默认文件串台
- [ ] 6 个用户文档页面的教程入口已添加，缺语言的处理符合约定
- [ ] Markdown 内部链接无死链

---

## 七、待运营确认

1. zh-TW 视频是否已录制？在哪个编号？
2. en 的参数说明 / 聪明钱 / 提现视频是否已录制？
3. 视频是否允许下载后二次分发到自家 CDN？是否有水印/授权限制？
4. es / hi 两种语言是否在计划内？（当前 App 支持 8 种语言，这两种尚无视频）
