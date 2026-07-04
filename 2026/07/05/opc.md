# AI 一人公司日报 | 2026-07-05

> **数据窗口：** 2026-07-04 06:00 → 2026-07-05 06:00（北京时间）
> **今日背景：** 美国独立宣言 250 周年 + 世界杯淘汰赛，时间线噪音极大。@TrungTPhan 等娱乐/体育账号全部内容已过滤。本期有效信号：0 A级 · 4 B级 · 多条 C级，属中间信号日。

---

## 今日头条

### baoyu-design Skill 借助 Fable 5 突破 PPTX 动画壁垒

@dotey 发布重要更新：baoyu-design（GitHub 1,190 stars，已验证）正式支持 PPT 动画导出。此前 Opus 4.8 多次尝试均失败，原因是 PptxGenJS 不直接支持 PPTX 动画节点。Fable 5 对 PPTX XML 格式了如指掌，迭代数轮即实现突破。

工作流：Claude Code / Cursor 本地运行 → 生成 HTML 幻灯片 → PptxGenJS 导出 PPTX（含动画） → 在 KeyNote/PowerPoint 中播放。常用动画已可用，细节仍有少量偏差。中国用户可直接访问，无需额外工具。

---

## 今日金矿

### 金矿 1 ⭐ B级 · Claude Skill · 工具

**baoyu-design 新增 PPT 动画支持（Fable 5 驱动）**

| 字段 | 数据 |
|------|------|
| 来源 | @dotey |
| 推文发布时间 | 2026-07-04 |
| 互动数据 | views 43,829 · bookmarks 312 · ER 0.71% |
| GitHub | github.com/jimliu/baoyu-design（1,190 stars，经 web_search 验证） |
| 中国可用性 | 直接访问（本地运行，无外部 API 依赖） |

**核心要点：**
- Fable 5 理解 PPTX XML 动画节点（`<p:animClkTbl>` 等），Opus 4.8 此前无此能力
- 导出流程：HTML → PptxGenJS → PPTX，Playwright 无头 Chromium 完成渲染
- 常用动画（淡入淡出、擦除、飞入）已可用；复杂动画细节有偏差
- 适合高频制作演示材料的独立开发者、咨询顾问、内容创作者

**适用读者：** C类（vibe coder / 工具整合）、A类（内容创作者减少 PPT 制作时间）

---

### 金矿 2 ⭐ B级 · Claude Skill · 中文工具

**Fenng Chinese Tech Doc Style Skill 更新，近 400 Stars**

| 字段 | 数据 |
|------|------|
| 来源 | @Fenng（知名中文技术人，丁香园创始人） |
| 推文发布时间 | 2026-07-04 |
| 互动数据 | views 9,795 · bookmarks 122 · ER 1.25% |
| GitHub | 见原推链接，近 400 stars |
| 中国可用性 | 直接访问 |

**核心要点：**
- 面向**中文技术文档、产品文案、界面文案**的写作 Skill，为一人公司节省大量文案校对时间
- ER 1.25% 为本窗口非节日内容前三，说明中文独立开发者对此有强烈需求
- 与 baoyu-design、op7418 演示视频 Skill 共同构成中文开发者"AI 生产力 Skill 套件"雏形

**适用读者：** A类（内容创作）、B类（独立开发产品文案）、C类（工具整合）

---

### 金矿 3 ⭐ B级 · SaaS 样板 · 工具

**TanStarter CLI v1.0 正式发布：5 分钟全自动部署新网站**

| 字段 | 数据 |
|------|------|
| 来源 | @indie_maker_fox |
| 推文发布时间 | 2026-07-04 |
| 互动数据 | views 3,777 · bookmarks 37 · ER 0.98% |
| 文档 | docs.tanstarter.dev/docs/cli |
| 源码 | github.com/mkfasthq/tanstarter-cli |
| 中国可用性 | 直接访问（需要 Cloudflare 账号） |

**核心要点：**
- 输入项目名 + 域名 → 自动完成：GitHub 仓库初始化、Cloudflare 资源配置、环境变量写入、域名上线
- 底层技术栈：TanStack Start + Cloudflare Workers + Base UI（从 Radix UI 迁移）+ shadcn/ui
- 本窗口该链接被分享 2 次，@indie_maker_fox 也是本窗口被转推最多的账号之一（3 次）

**适用读者：** B类（indie dev 快速搭建 SaaS）、C类（vibe coder 降低部署门槛）

---

### 金矿 4 ⭐ B级（弱） · SaaS 收购 · 商业化参考

**acquire.com 在售：M365/Google Workspace 迁移 SaaS（$30K/月利润，94% 毛利率）**

| 字段 | 数据 |
|------|------|
| 来源 | @agazdecki（acquire.com CEO） |
| 推文发布时间 | 2026-07-05 04:13 |
| 互动数据 | views 1,926 · bookmarks 7 · ER 0.36% |
| 月利润 | $30,000（≈ ¥217,800/月，按汇率 7.26） |
| 毛利率 | 94% |
| TTM 营收 | $33K（业务存续时间短，近期才开始规模化） |
| Listing | app.acquire.com（经 web_search 未找到 listing 补充信息） |
| 中国可用性 | 需要工具（acquire.com 国内访问不稳定） |

**核心要点：**
- 企业 IT 迁移属刚需，客户付费意愿强；94% 毛利率表明几乎无运营成本
- TTM 仅 $33K 说明是早期业务，但上月利润 $30K 意味着正在快速规模化
- 收购估值参考：数字业务通常 2–4× 年利润 → 估算 $720K–$1.44M（≈ ¥522 万–¥1,045 万）
- 对一人公司读者的价值：**赛道参考**，企业 M365/Google Workspace 迁移可用 AI 高度自动化

**注意：** 本条目 engagement 极低（7 bookmarks），信号来自 @agazdecki 官方账号，数据可信但未经独立验证。

**适用读者：** D类（服务变现）、B类（寻找可复制商业模式）

---

## 快讯区

**本窗口 C 级信号速览**

- **Marc Lou TrustMRR bot traffic** [@marclou] — "TrustMRR 过去两周：105,821 人类用户 vs 366,410 机器人，3.4× 流量来自 AI（ChatGPT / Claude）和爬虫。" DataFast 已内置 bot traffic 追踪，支持识别 ChatGPT/Claude 抓取、Googlebot 索引、训练数据爬取及 404 信号。（views 22,393 · bookmarks 66 · ER 0.29%）→ **一人公司 SEO 策略必须纳入 AI 流量考量**

- **Sonnet 5 网页设计 18 分钟教程** [@FinanceYF5] — "有开发者专门录了一条 18 分钟教程，讲怎么用 Claude Code 配 Sonnet 5 搭出拿奖级别的网站。"（views 7,115 · bookmarks 78 · ER 1.10%）→ 链接见原推，C/B 类读者收藏

- **Fable 5 疯狂用例 Top 10** [@FinanceYF5] — 整理了 10 个用 Fable 5 实现的极端案例，包括有人靠此赚钱。（views 25,024 · bookmarks 114 · ER 0.46%）→ 模型能力快速参考

- **演示视频 Skill 需求调研** [@op7418] — "有人需要这种可以做演示视频的 Skill 吗？"附演示视频链接。（views 45,762 · bookmarks 326 · ER 0.71%）→ 326 bookmarks 说明需求强烈，Skill 尚未正式发布，持续关注 @op7418

- **lxfater：放弃写程序，直面技能标品化** [@lxfater] — X Article，JS 限制无法读取全文。摘要：GPT5.3 后意识到技术壁垒被模型更新快速抹平，标品化导致低价化，于是转向新技能方向。（views 10,536 · bookmarks 137 · ER 1.30%）→ 高 ER，建议直接阅读原文

- **Polymarket V2 Builder 归因 bug** [@runes_leo] — 将自建交易系统迁至 Polymarket V2 后，发现所有订单的 builder 归因字段为空，volume 全部归平台。根因：V2 订单结构中 `builderCode` 字段若不填，SDK 默认全零，无报错无警告，链上照样成交。（views 7,757 · bookmarks 58 · ER 0.75%）→ **参与 Polymarket Builder Program 的开发者必读，迁 V2 前检查 builderCode**

- **FinanceYF5：AI 交易机器人价值 28.9 万美元** [@FinanceYF5] — 列举了一个用 AI 构建的交易机器人估值案例（$289,000）。（views 3,607 · bookmarks 9 · ER 0.25%）→ 数据未经独立验证，存疑，谨慎参考

- **lxfater：将工作交给 AI** [@lxfater] — "这篇文章标题可以改为：如何将工作交给 AI。很多人没认真研究过自己的工作，所以无法交给 AI。你不交，懂门道的人会交，冷兵器对热兵器。"（views 7,741 · bookmarks 21 · ER 0.27%）

---

## 传播力素材

> 以下内容 engagement_rate 高，但属传播/情感共鸣类，**非直接行动信号**。适合内容创作者（A类）参考选题方向。

| 排名 | 账号 | 摘要 | ER | Bookmarks | 备注 |
|------|------|------|-----|-----------|------|
| 1 | @thedankoe | X Article | **2.84%** | 7,906 | 内容为 X Article，JS 限制无法读取全文；书签量极高，强烈建议直接阅读 |
| 2 | @aaditsh / @trq212 | X Article | 0.79% | **14,612** | 本窗口最高书签量；内容为 X Article，JS 限制无法读取全文 |
| 3 | @blakeaburge | "Treat your hobbies like a small business — have more hobbies, fewer opinions" | 1.22% | 1,389 | 副业/爱好产品化的心理框架 |
| 4 | @Jayyanginspires | "People who realize they can just do things have a certain aura." | 1.11% | 366 | 本窗口被转推 4 次，执行力与自我授权叙事 |
| 5 | @Jayyanginspires | "How can I increase my surface area for luck?" | 1.40% | 202 | 扩大机遇接触面 |
| 6 | @lxfater | X Article（编程/技能标品化） | 1.30% | 137 | 见快讯区；值得深读 |

---

## 延伸资源库

| 资源 | 来源账号 | 类型 | 中国可用性 |
|------|---------|------|-----------|
| github.com/jimliu/baoyu-design | @dotey | 开源 Skill | 直接访问 |
| docs.tanstarter.dev/docs/cli | @indie_maker_fox | 官方文档 | 直接访问 |
| github.com/mkfasthq/tanstarter-cli | @indie_maker_fox | 开源工具 | 直接访问 |
| @Fenng Chinese Tech Doc Style | @Fenng | 开源 Skill | 直接访问 |
| DataFast bot traffic tracker | @marclou | SaaS 工具 | 需要工具 |
| @thedankoe X Article | — | 深度内容 | 需直接访问 X |
| @aaditsh / @trq212 X Article | — | 深度内容（最高 BK） | 需直接访问 X |
| @lxfater X Article | @lxfater | 深度内容 | 需直接访问 X |

---

## 行动建议

**本周可立即执行：**

1. **测试 baoyu-design PPT 动画**（C/A 类读者）：如果你已有 Claude Code 或 Cursor + Playwright 环境，clone github.com/jimliu/baoyu-design 直接测试。首选场景：客户提案、产品演示、内容课程课件。

2. **安装 Fenng Chinese Tech Doc Style Skill**（A/B/C 类读者）：中文产品文案和技术文档是一人公司的高频工作，该 Skill 近 400 stars 说明已有验证，直接使用可节省大量文案打磨时间。

3. **检查你的 Polymarket Builder 配置**（B 类读者，仅参与 Builder Program 者）：迁移至 V2 的交易系统必须显式设置 `builderCode`，否则所有 volume 归平台，你的激励收益清零。

4. **阅读 @thedankoe 和 @aaditsh X Article**（全类读者）：本窗口书签量最高的两篇文章（7,906 + 14,612），受 JS 限制需直接在 X 上打开阅读。

5. **关注 @op7418 演示视频 Skill**（A/C 类读者）：326 bookmarks 的需求验证极强，Skill 尚未正式发布，上线后立即是高价值工具。

---

## 避坑指南

- **节日噪音陷阱（7月4日）**：美国独立250周年 + 世界杯期间，@TrungTPhan 等娱乐账号的高 engagement 帖子（World Cup 战报、爱国内容）已全部过滤，不予引用。
- **acquire.com 数据解读注意**：$30K 月利润 + $33K TTM 营收意味着该业务处于极早期（近一个月才规模化），收购估值参考意义 > 直接投资意义，请区分。
- **@FinanceYF5 AI 交易机器人估值未验证**：宣称价值 $289K 的案例无第三方数据支撑，勿直接参考。
- **TanStarter CLI Cloudflare 限制**：国内访问 Cloudflare Workers 部署的服务可能存在不稳定，建议测试时使用代理环境。

---

## 本期情报评估

| 指标 | 数值 |
|------|------|
| 数据窗口 | 2026-07-04 06:00 → 2026-07-05 06:00（北京时间） |
| 总推文数 | 219（原创 120 · 引用 48 · 转推 46 · 回复 5） |
| 活跃用户数 | 74 |
| 语言分布 | 英文 148 · 中文 59 |
| A 级信号 | 0 |
| B 级信号 | 4（baoyu-design · Fenng Skill · TanStarter CLI · acquire.com SaaS） |
| C 级信号 | 7 |
| 过滤噪音 | 大量（节日 / 世界杯 / 爱国内容） |
| 信号密度评级 | **中低**（中间信号日） |
| 特殊背景 | 美国国庆 250 周年 + 世界杯淘汰赛，噪音比远高于正常工作日 |
| 最高书签 | @aaditsh / @trq212 X Article — 14,612 |
| 最高 ER | @thedankoe X Article — 2.84% |

---

*本报告由自动化流水线生成，数据来源为 Twitter/X 列表爬虫，时间窗口内共处理 219 条推文。*
