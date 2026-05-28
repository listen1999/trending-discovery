# AI 一人公司日报 | 2026-05-29

数据窗口：2026-05-28 06:00 — 2026-05-29 06:00（北京时间，过去 24 小时）
推文总量：338 条 / 活跃账号：87 位 / 深度挖掘：3 条
汇率参考：1 USD ≈ 7.1 CNY（2026-05-29 参考价）

---

## 今日头条

**Anthropic 同日抛出 Opus 4.8 + Claude Code「dynamic workflows」，把"一个人能并发驱动几百个 agent"从口号变成默认能力。** 模型价格与 Opus 4.7 持平、agentic coding 分数从 64.3% 升到 69.2%（来源：anthropic.com/news/claude-opus-4-8 与 TechCrunch 报道）；同时 Claude Code 推出 dynamic workflows research preview，一句"create a workflow"即可由 Claude 自动编排上百个并行 subagent 互审、迭代，断点可续，跑得动跨整个代码仓库的迁移、审计、重写。Cursor 同日接入 4.8 并隐藏 4.7、Factory Droid、Bearly AI 的 OpenADE 也同步跟进。**对一人公司读者的意义**：能耗大量 token 是真，但"模型 + harness"已正式取代"裸模型"成为可消费的产品形态——独立开发者从今天起开始用预算决定能交付的工程规模，而不是用人头。

---

## 今日金矿

### 金矿 1：Anthropic Opus 4.8 + Claude Code dynamic workflows

来源：@claudeai 官方 · 2026-05-28 23:30 BJT · 👍 48,716 · 转推 · @awilkinson 引用 Every 评测 161K views / 585 bookmarks · @gregisenberg 引用解读 120K views / 975 bookmarks · engagement_rate 0.0036–0.0081（同期中位数约 0.0015–0.0020，属 Top 5%）

**核心数据（已验证）**
- 模型版本：Claude Opus 4.8，2026-05-28 北美时间发布（交叉验证自 anthropic.com、TechCrunch、9to5Mac、MacRumors）
- 定价：与 Opus 4.7 一致，未上调（来源：Anthropic 官方）
- 基准提升：Agentic coding 64.3% → 69.2%、Multidisciplinary reasoning with tools 54.7% → 57.9%（来源：Anthropic 官方）
- Every（@danshipper、@awilkinson）实测：Senior Engineer bench 63 分，比 GPT-5.5 的 62 高 1 分，比 4.7 高 30 分（据 every.to/vibe-check/opus-4-8-vibecheck 推文摘录，[未经独立复现]）
- dynamic workflows：研究预览，Anthropic 自宣示例为 Bun 用 Rust 重写——75 万行 Rust 代码、通过 99.8% 原测试、11 天合并（据宝玉@dotey 转译，[未经独立核实数字]）
- Token 消耗预警：Anthropic 自己强调显著高于普通 Claude Code 会话，Enterprise 套餐默认关闭、需管理员手动开启（据 @dotey 整理）
- Fast mode（同模型快 2.5 倍、价格便宜约 3 倍）在 /fast 开关下可用；API 需联系客户经理（据 @dotey）

**商业模式拆解**
- Claude Code 已从"按 session 计费的代码助理"转向"按 workflow 计费的工程外包平台"——同一个用户，token 用量曲线被强行抬升
- Anthropic 同日传出新一轮融资规模消息（@packyM 提到 $65B 量级，[未经验证]），与产品端"鼓励多耗 token"的节奏完全同步
- Cursor 接入即隐藏 4.7、保留 4.6，说明厂商把 4.8 当成默认模型推；Codex / Droid 同时跟进，证明竞争对手没有冷启动期

**复制路径**

档位 B（独立开发者）
- 今天就把 Claude Code 升级到含 dynamic workflows 的最新版（Max / Team 套餐默认开启），第一个 workflow 不要选大迁移，先选"为现有项目补全单元测试"或"批量重命名 API"这类容易验证的小活，观察 token 烧得多快
- 把 4.8 + dynamic workflows 当作"用钱买并发"：估算自己单条工程任务的 token 上限（如 $50/任务），加进定价模型，再决定要不要把任务规模从单文件提到模块级
- 同时保留 Codex / Cursor 通道（@arvidkahl 验证："Claude Code 主写 + Codex 作 reviewer，月费 $20，/codex:review 每个 feature 跑一次"），让 review 留在另一家以避免一家独大

档位 C（工具集成者 / vibe coder）
- dynamic workflows 触发关键词是 "create a workflow" 或菜单里的 ultracode，今天先在测试仓库跑一遍"建一个 dev → staging → prod 的部署 workflow"感受一下中断续跑、对抗 agent 互审的行为
- 国内可访问性：claude.ai 在国内属于"需要工具"档；但 4.8 也接入 Cursor（claude.com / cursor.com 在国内同样需要工具），价格按官方计费

**国内可用**：需要工具（claude.ai / claude.com 均不直连）；Cursor、Factory Droid 同样需翻墙登录

**踩坑预警**
- "并发 + 对抗 review"会显著放大 token 账单。Anthropic 自己提醒先用小任务试水。某条用户反馈：开 4.8 后曾出现回答自相矛盾，自报模型身份混乱（@Cydiar404 实测："一会回答是千问，一会回答是 DeepSeek"），4.8 还在抖动期
- 在 medium reasoning 下写作 AI 味偏重，Every 推荐使用 high / xhigh 档（据 @awilkinson）
- 国内付款渠道：Anthropic 不直接收人民币卡，需要海外信用卡 / 海外 Apple ID 充值，或走 Cursor 包月

**官方链接**：https://www.anthropic.com/news/claude-opus-4-8 ｜ Every 评测：https://every.to/vibe-check/opus-4-8-vibecheck

**深度综述（350 字）**

这条信号最值得在意的不是分数表，而是 Anthropic 把"harness 决定上限"这件事公开承认了。@awilkinson 原话："a model is only as good as its harness, and Codex is still a far superior harness to the Claude Desktop app"——这是来自一个"我们花一周深度测了"的人。结论很清楚：4.8 把模型层重新拉到 SOTA，但 Anthropic 的桌面壳还在追 OpenAI 的 Codex。所以这次新闻的真正主角是 dynamic workflows——一个对 harness 形态的押注，让 Claude Code 自己变成"框架 + 编排器"，把和 Codex 的体验差强行抹平。趋势定位上，这是"vibe coding"这条线从"我边写边问 AI"过渡到"我下班前发个 workflow，明早来看结果"的关键一步，与上周 @_catwu 在 Anthropic 内部把 cowork 推向团队场景的节奏完全衔接。对一人公司的意外点：单个工程任务的"边际成本上限"被人为放大——以前一个 bug 修不动就放弃，现在你可以丢 $200 的 token 让 50 个 agent 在夜里轮番啃。风险则是对 Anthropic 的依赖度被进一步绑死：4.8 + dynamic workflows + cowork 共同构成的工作流，一旦换厂就要重写所有 .md / Skills / 调度脚本，迁移成本远高于换 GPT-5.5。

---

### 金矿 2：歸藏（@op7418）把 PPT Skill + 小红书图文 Skill 推向"商用授权"

来源：@op7418 · 2026-05-28 19:55 BJT · 👍 123 · 👁 10,348 · 收藏 80 · engagement_rate 0.0077（同期中位数约 0.0015，Top 15%）；前置作品贴 0.0118 / 收藏 405

**核心数据（已验证）**
- 推文原文："藏师傅的 PPT Skills 和小红书图文排版 Skill，已经通过这几天的发酵证明了巨大的商业价值。如果有哪些 Agent 或者 AI 平台需要商用授权、集成到自己产品里的，可以联系藏师傅"
- 配套小红书 Skill 数据（据作者前一条推文与 GitHub op7418/guizang-social-card-skill 验证）：
  - 2 套主题 / 28 个版式 / 9 套配色 / 8 大小红书内容类别
  - 输出形态：单文件 HTML → PNG（Editorial × Swiss 视觉系统）
  - 触发词：用户在 Claude Code 中说"帮我做一套小红书图文"
  - 仓库类型：开源，安装路径 `~/.claude/skills/guizang-social-card-skill`
- 同作者 PPT Skill（op7418/guizang-ppt-skill）也已开源，定位为 editorial magazine / Swiss layouts 的演示文档生成器
- 据公开仓库 op7418/NanoBanana-PPT-Skills 等姊妹项目，作者已围绕 Claude Skill 构建多条产品线
- 收入 / 授权报价：未公开，[未经验证]

**商业模式拆解**
- 个人作者做 Skill → 在 Twitter 发酵积累需求 → 再以"商用授权 + 集成调优"卖给 Agent / AI 平台。本质是 IP 授权 + 定制服务的组合，不是 SaaS
- 上游成本：1 个作者维护多套 Skill；变量成本几乎为 0
- 下游对象：从"个人 Claude Code 用户"上升到"任何带 Agent 能力的 AI 产品的 B 端集成方"
- 关键护城河：Editorial + Swiss 美学规范 + 小红书平台具体版式（避 AI 标）这套"领域审美 + 平台经验"

**复制路径**

档位 A（内容创作者）
- 今天就把 guizang-social-card-skill 安装到 Claude Code（开源，免费），跑 3 张图测试效果。若公众号 / 小红书图文是你日常产出，这条 Skill 直接砍掉排版人/外包美编环节
- 给自己的内容垂类（如读书、AI、亲子）做"私有 Skill"——在 Skill prompt 里固化你常用的色卡、字体、引用块格式，作为你个人风格的复用资产

档位 C（工具集成者）
- 如果你在做面向中文创作者的 AI 产品，这就是个"借力 + 付费授权"机会：先用开源版评估调用稳定性，再视用户付费规模决定要不要拿商业授权，把 Skill 嵌进自己产品的内容生成模块
- 自己复刻一套"细分平台版式 Skill"（如视频号封面、知乎专栏、即刻图文）也是可行的复制路径，但门槛在视觉品味，不在 prompt 工程

**国内可用**：Claude Code 主体需翻墙登录；guizang-social-card-skill 仓库在 GitHub，国内可直接 clone

**踩坑预警**
- "Skill 经济"目前没有标准计价机制。作者在 Twitter 发酵后议价能力高于上架商店；中国独立开发者照搬这个"在 Twitter 谈授权"模式时，需要准备好海外收款（Wise / Stripe Atlas）
- 开源版与商用授权版的功能差异未公开。如果你打算把它嵌入自己付费产品，建议先和作者沟通版权边界，避免后续合规纠纷

**官方链接**：https://github.com/op7418/guizang-social-card-skill ｜ https://github.com/op7418/guizang-ppt-skill

**深度综述（330 字）**

这是 Claude Skills 自 2025 年底正式开放以来，第一次出现"个人作者直接把 Skill 当 IP 卖授权"的可观察案例，趋势定位属"早期信号、第一次可见的商业化模板"。常规假设是 Skill 像 GitHub 仓库一样靠 star / 影响力变现，歸藏给出的反例是——他绕开了应用商店、绕开了订阅，直接定位 B 端集成。这对中文创作者最反直觉的部分是：你长期以为"美学 + 平台 know-how"很难标价，但这一刻它能被打包成一个可机器消费的格式，价格谈判权回到作者手里。对国内一人公司的启示有两个：第一，垂直平台 + 视觉风格这两条护城河比"通用提示词"更稀缺；第二，海外 Agent 平台正缺少中文场景的内容能力，是真实的需求。风险也很明确：Skill 的依赖是 Claude Code / Codex 的 Skill 协议，一旦 Anthropic 修改协议或自带类似官方组件，这条赛道的议价权会迅速向平台回流；同时商用授权报价目前完全不透明，对买方议价能力极弱，中国创作者需要警惕"开口报价过低"的陷阱。

---

### 金矿 3：PaywallPro 开源 Top 500 iOS 订阅 App 付费墙数据集

来源：@lxfater（铁锤人）转发 @AI_Jasonyu · 2026-05-28 18:20 BJT · 👍 209 · 👁 59,722 · 收藏 344 · engagement_rate 0.0058（同期中位数约 0.0015，Top 15%）

**核心数据（已验证）**
- 项目：paywallpro/paywall-gallery（经 GitHub 验证：303 stars、69 forks、10 次 commit）
- 数据规模：500 个 iOS 付费订阅 App，每周新增 50 个（据作者推文与仓库 README）
- 字段：付费墙截图、Onboarding 预览、定价模型、付费墙模式、估算 MRR / ARPU / RPD、评分、版本号、offer 详情（周期、价格）、截图数量、Onboarding 流程数量
- 输出形态：机器可读的 Markdown 文件，含完整截图链接
- 许可：可用于"学习、研究、评论、内部产品参考"（需署名），禁止整包搬运、再售卖、用于构建直接竞争的商业产品；截图版权仍归各 App 开发商

**商业模式拆解**
- 开源版是"漏斗"：拿走头部 500 个 App 的标准数据，让独立开发者把它当付费墙设计的免费 reference
- 隐含商业化路径：完整数据集（不止 500）、API 化、按行业切片大概率会变成 PaywallPro 的付费 SKU——但作者本贴未明确披露价格，[未经验证]
- 估算 MRR / ARPU / RPD 来源未公开方法论，[未经验证]，使用时建议作为"相对值参考"而非"绝对值依据"

**复制路径**

档位 B（独立开发者）
- 今天 30 分钟可做：git clone 仓库，扫一遍你产品所在的赛道（健康、效率、AI 工具…）前 20 个 App 的付费墙截图，标注他们的（a）首屏 hook，（b）价格锚定（年付 vs 月付折扣比例），（c）软付费墙 vs 硬付费墙边界
- 本周可做：把仓库的 5 个最像你产品的 App 的 Onboarding 流程截屏并排列对比，逐步骤问自己"如果删掉这步会怎么样"，对照修订自己的 Onboarding——iOS 付费墙优化的最大杠杆点通常在 Onboarding 末段
- 与现有工具链配合：把 Markdown 数据导入 Notion / Obsidian，配合 Claude Code 的项目级搜索做 prompt，比如"列出所有把年付折扣压在 60% 以下的健康类 App，统计他们的首屏文案模式"

档位 D（服务变现者）
- 给 iOS App 团队做付费墙优化咨询，这套数据是免费弹药库。但避免直接二次售卖——许可明确禁止
- 输出物可以是"按你产品所在赛道的付费墙竞品分析 + 改写建议"，单次服务定价参照欧美 ASO 咨询行情（[未经验证]，建议先看 Reddit r/AppDevelopers 实价）

**国内可用**：GitHub 直接访问；iOS 海外开发者账号 + Apple ID 走 App Store Connect 流程

**踩坑预警**
- "估算 MRR" 字段方法论不公开，与真实订阅收入可能差异较大。把它作为相对排序信号，不要在商业计划里直接引用绝对值
- 仓库 commit 频率较低（10 次 commit），数据新鲜度需要自查时间戳
- 跨境收款仍是最大门槛，与付费墙优化无关——一人公司搭出海订阅 App，先把 Stripe Atlas / 香港公司这层走通再优化数据

**官方链接**：https://github.com/paywallpro/paywall-gallery

**深度综述（300 字）**

这条信号在过去半年是反复出现的——"独立开发者最缺的不是设计能力而是看见好设计的机会"。Paywall Gallery 把"我去逛 25 个竞品 App 的付费墙"这件事从一天压缩到 15 分钟，价值是真实的。趋势定位属于"中期验证"：自从 2024–2025 年 vibe coding 让产品端 MVP 接近零成本之后，独立开发者真正缺的是"付费墙 + Onboarding"这个高 ROI 节点的批量经验，开放数据集是把这个 know-how 显性化的合理产物。反直觉之处：作者主动公开 MRR 估算字段，说明 PaywallPro 的真实生意可能不在数据本身，而在数据的连续性 + 行业切片——你今天看到的是 500 个公开样本，下季度对手会看到 1500 个动态样本。一人公司复制这个模式的窗口期还在：选一个"出海创作者最饥渴的视觉资产 + 数据组合"的垂类（如 LinkedIn 帖、TikTok 直播间 UI、Shopify 落地页），同样可以做出"免费 500 + 商业付费数据"的开源 → 商业漏斗，但前提是你能持续供数。

---

## 快讯区

**收入信号**
- Pat Walls 转发某 $60K MRR SaaS 创始人案例：上线 2 个月、靠 2,000 次客户电话拉出留存与定价（"if he didn't do this, the product would not have made any money"）— @thepatwalls · 2026-05-29 05:16 · 👁 685 · [未经验证，作者也声明 "allegedly, I will have to verify this"]
- Pat Walls 自我案例：员工年薪 5 年 $54K → $115K → 离职做 Starter Story，8 年收入 0 → $1.6M → 卖掉公司 — @thepatwalls / @starter_story · 2026-05-29 04:00 · 👁 54,210 · 收藏 178 · 数据来自 Pat Walls 自述
- TanStarter（@indie_maker_fox）声明模板月销售额"首次超过 ShipFast"，未公开具体数字 — @indie_maker_fox · 2026-05-28 14:10 · 👁 6,159 · [未经验证]
- Indie Fox 简介自述："产品出海 2 年收入破 10 万美刀"（约合 ¥71 万）— 据 author_bio
- Tony Dinh（@tdinh_me）简介自述："TypingMind $137K/m"（约合 ¥97 万 / 月） + 其余产品 $5K / $518 / $50 — 据 author_bio
- @levelsio 简介自述：6 款产品月营收合计约 $242K/m（约合 ¥172 万 / 月）— 据 author_bio
- Marc Lou 简介自述：6 款产品月营收合计约 $70K/m（约合 ¥49.7 万 / 月）— 据 author_bio

**产品发布**
- Claude Opus 4.8 + Claude Code dynamic workflows research preview · 2026-05-28 — @claudeai 官方
- Cursor 上线 Opus 4.8，默认隐藏 4.7、保留 4.6 — @cursor_ai · 2026-05-29 02:30
- Factory Droid 接入 Opus 4.8 含 fast mode — @bentossell / @FactoryAI · 2026-05-29 01:44
- Netlify AI Gateway 实操演示更新（内置访问 AI 模型，无需自建 key 管理）— @thisiskp_ · 2026-05-28 07:20
- @Shpigford 发布 granite.co 上 Product Hunt（产品方向未在推文具体披露）— 2026-05-28 18:22
- 锐哥 MOGE.AI（@NewRay888）上 Product Hunt，定位"AI 工具发现 + Agent Skills 精选"，月流量自述 400K+ — 2026-05-28
- II-Commons-Skills：Intelligent-Internet 开源的"让 Agent 能从 arxiv / PubMed 拉知识"的 Skill 仓库 — @virushuo 转推 · 2026-05-29 00:31

**工具更新**
- Anthropic Claude Design 与 Claude AI 网页、Claude Code 共享额度（之前是独立额度）— @dotey · 2026-05-28 06:53 · 👁 30,871 · 收藏 119
- 推特上线自动翻译，全量推文按读者语言自动翻译（"巴别塔倒塌了？"）— @xiaohu / @op7418 / @turingou 多人确认 · 2026-05-28
- X Premium / Premium+ 接入 Hermes Agent + Grok CLI，xAI 可在本地命令行调 Grok-4.20 — @runes_leo · 2026-05-28
- @indie_maker_fox 切换主工作流到 Superconductor（支持多 coding agent + worktree） — 2026-05-28 11:20

**值得关注的观点**
- 宝玉（@dotey）整理的多 agent 写 plan 工作流：把需求同时丢给 Codex / Claude Code / Cursor 开 Plan 模式，挑最优方案再让另两个借鉴；复杂 Plan 切 phase 写 Markdown 文档，便宜模型负责执行，最后用 GPT-5.5 做 review — 👍 390 · 👁 39,755 · 收藏 413 · engagement_rate 0.0104
- Arvid Kahl（@arvidkahl）：Claude Code 主写 + Codex 作 reviewer（codex-plugin-cc 插件，$20/月），每个 feature 跑 /codex:review — engagement_rate 0.0111
- Ole Lehmann（@itsolelehmann）拆解 Anthropic 内部 marketing ops 周报工作流：周日夜定时任务 → 抓上周纪要 + Slack + 数仓 → 3 个自建 Skill（prep / proofread / action-items）→ 周一直接给主管 → 每周用"这周学到什么"反哺 Skill。强调 proofread Skill 禁止 hallucination："no source = no number" — engagement_rate 0.0122
- Nicolas Cole（@Nicolascole77）把 102 个 viral writing 模板打包成 5 个 Claude Skills，评论 "social" 免费送 — 👍 290 · 收藏 390 · engagement_rate 0.0116
- @asmartbear（Jason Cohen，2 家独角兽创始人）反 mid-market 创业定式："小公司没钱 / 大公司锁死，中间是机会"——他的长文质疑这是"两头之恶兼具" — 链接到 longform.asmartbear.com/mid-market
- @asmartbear："我之所以知道做软件比理解客户 + 拿到注意力 + 卖出去容易 100 倍——因为我认识 100 个能做软件的工程师，对应只有 1 个能让 100 个人付费的创始人"
- @oran_ge（Orange AI）总结当前 AI 反思声音四点：1) model + harness 才是产品 2) 完全自动化是自欺欺人 3) 慢工出细活是新奢侈品 4) AI 的 ROI 有时不如人 — 👍 184 · 收藏 97
- @SimonHoiberg 公开自托管 SaaS 栈：Hetzner + Kubernetes + Docker + WireGuard + NextJS / Postgres / pgvector / Redis / MinIO / Grafana / Prometheus，自述跑出 7 位数 SaaS — 收藏 146

**教训与反思**
- Cydiar404 实测 Opus 4.8 偶发"一会回答是千问、一会回答是 DeepSeek"，4.8 早期身份识别有抖动
- @gefei55（哥飞）案例：oreateai 用 AI 批量低质量页面冲流量，2 个月后流量已下跌，证明 Google 自净机制起效——批量生成不等于低质量批量生成
- @lidangzzz：对普通中国人合规接触美股的两条路——支付宝定投 S&P500 / 纳 100 基金，或在富途/老虎/长桥持有 Nvidia/OpenAI/Anthropic 现金股至 100 岁报税 — 👁 18,456 · 收藏 39（金融建议，不构成实操推荐）

**传播力素材**
- 原文："The newsletter is the business. The content is the product. Your life is the marketing." — @Jayyanginspires · 👁 279 · engagement_rate 0.0072
  改写方向：适合公众号"AI 时代个人品牌方法论"选题——把这三句拆成三段论的标题图，对照举一个真实独立开发者案例（如 @Nicolascole77、@dvassallo）
  点评：这条话击中的是创作者对"个人品牌 + 产品 + 生意"三角关系长期模糊的焦虑，用同位语把三件事压成一句格言。盲区在于它默认"newsletter 是合理生意"——对中国创作者来说 newsletter 不是渠道（公众号 / 视频号才是），照搬这句话会误导你低估渠道差异。
- 原文："Most AI companies are actually just UX companies with a very expensive API bill." — @Prathkum · 👁 17,438
  改写方向：适合视频号短视频——念这一句 + 拉 3 个 AI 工具的对比截图（同样 API、不同界面）
  点评：金句的反直觉力来自"砍掉技术神秘感"，提醒创业者别把"用 OpenAI"当核心竞争力。但盲区是它低估了今天 UI 之外的 RAG / context 工程 / 数据飞轮——把"UX"这一个词扛起所有差异化太省事
- 原文："The unit of work you can hand off jumps from a file to an entire codebase." — @gregisenberg（描述 dynamic workflows）· 👁 120,365 · 收藏 975
  改写方向：适合小红书图文——封面写"AI 编程的'最小单位'又变大了一档"，正文 3 张图分别解释 file → module → codebase
  点评：把 dynamic workflows 翻成"工作交付单位的跃迁"是非常精准的命名，独立开发者用这一框架去解释为什么自己今天能"一人公司化"会更有说服力。但要注意 token 账单是这种跃迁的隐性成本，传播时不能只讲爽点不讲账
- 原文："Hiring for slope > y-intercept is more true than ever" — @stephsmithio · 👁 3,052
  改写方向：适合 LinkedIn / 即刻——"招人看斜率比看起点更重要"，配一个学习曲线对比图
  点评：原本是面对企业招聘者的判断，搬到一人公司语境就是"挑合伙人 / 合作者要看成长速度而非现有 title"。但盲区在小团队短期内根本没时间等斜率兑现，需补一句"如果只能等三个月，那 y-intercept 也别低"

---

## 延伸资源库

### 播客 / 视频 / 访谈
- Every「Vibe Check: Opus 4.8—Anthropic Should've Rounded Up to 5」by @danshipper / @awilkinson · 评测文章 + 视频 · 链接：https://every.to/vibe-check/opus-4-8-vibecheck
- @TrungTPhan × @benthompson Stratechery 节目（讨论生成式广告革命、Meta、Google Search、Apple、AppLovin）· 2026-05-29 03:09 · 链接见 stratechery.com
- Silk Podcast EP 1：@JackButcher × @JustinGilanyi · 主题"Don't touch the art" · silkarthouse.com/podcast/work-luck-play-jack-butcher
- 本期未涉及高优先级中文播客新单集

### 图书 / 课程
- 本期无新书 / 课程信号

### 链接汇总（已 web_fetch / web_search 验证）
- 工具类：
  - https://www.anthropic.com/news/claude-opus-4-8 （Anthropic 官方）
  - https://github.com/paywallpro/paywall-gallery （303★，已 fetch）
  - https://github.com/op7418/guizang-social-card-skill （小红书图文 Skill，已 search 确认）
  - https://github.com/op7418/guizang-ppt-skill （PPT Skill，已 search 确认）
  - https://github.com/Intelligent-Internet/II-Commons-Skills （知识检索 Skill）
  - https://github.com/openai/codex-plugin-cc （Codex 作为 Claude Code 的 review 插件，@arvidkahl 推荐）
  - https://docs.tanstarter.dev/zh/docs/mkimage （MkImage 接入 TanStarter 的文档）
- 报道类：
  - https://techcrunch.com/2026/05/28/anthropic-releases-opus-4-8-with-new-dynamic-workflow-tool/
  - https://9to5mac.com/2026/05/28/anthropic-upgrades-claude-with-new-opus-4-8-model-heres-whats-new/
  - https://www.macrumors.com/2026/05/28/anthropic-claude-opus-4-8/
  - https://longform.asmartbear.com/mid-market/ （Jason Cohen 反 mid-market 创业长文）
  - https://www.notboring.co/p/thank-god-for-data-centers （Packy McCormick）

---

## 行动建议（按档位分组）

档位 A（内容创作者）
- 今天 30 分钟内：在 Claude Code 装 op7418/guizang-social-card-skill，跑 3 张你公众号 / 小红书近期选题的图文，对比你现有排版的时间成本
- 本周可做：把自己最常用的 3 套视觉风格写进私有 Skill（色卡、字号、引用块格式），形成可复用资产

档位 B（独立开发者）
- 今天 30 分钟内：克隆 paywallpro/paywall-gallery，把你产品赛道前 20 个 App 的"首屏 hook、年付折扣、Onboarding 末段"三件事手抄到文档
- 今天 30 分钟内：把 Claude Code 升级到含 dynamic workflows 版本，先跑一个低风险任务（如"为模块 X 补单测"），观察 token 消耗速度
- 本周可做：建立"主写 Claude Code + 审查 Codex"双通道（codex-plugin-cc，$20/月），每次新功能跑一次 /codex:review

档位 C（工具集成者 / vibe coder）
- 今天 30 分钟内：用 dynamic workflows 触发关键词 "create a workflow" 试一个真实场景的端到端任务（如"从 GitHub issue 到 PR"），把你预算上限设成单任务 $20，强制中断观察行为
- 本周可做：评估是否把 op7418 / II-Commons / Nicolas Cole 的 Skills 接入自己工作流，按"先 fork 再用"原则减少协议变动风险

档位 D（服务变现者）
- 本周可做：以 paywallpro/paywall-gallery 为弹药，给已有 1 个 iOS App 客户做"付费墙 + Onboarding 对标分析"作为内部 demo，验证报价空间

---

## 避坑指南

- **dynamic workflows 的"试一下没事"**：Anthropic 自己警告 token 消耗显著放大、Enterprise 默认关闭——独立开发者别用月费套餐随手挂大型 workflow 跑过夜，先估单任务 token 上限再开。
- **Opus 4.8 早期身份识别抖动**：@Cydiar404 实测出现"一会回答是千问、一会是 DeepSeek"，证明 4.8 在中文场景的对话连贯性还在抖动。重要场景先做小批量验证再切换。
- **AI 批量生成 SEO 站的自净期到了**：@gefei55 案例（oreateai）显示 2 个月内流量已下跌；不要被"批量页面+短期流量"骗，长期稳定流量仍依赖单页质量。
- **本土化金额建议不可凭空给**：本期多名作者自报月营收（@levelsio、@tdinh_me、@indie_maker_fox、Marc Lou），均为 author_bio 自述、非招股书或第三方核实数据；任何"我也能做到 $X/月"的复制路径都需要看清楚作者用了几年和什么渠道才到这个数。

---

## 本期情报评估

**信息密度**：高密度
原因：Opus 4.8 + dynamic workflows 同日落地，配套 Cursor / Factory 等 harness 同步跟进，单一事件带动了 PPT/小红书 Skill 商用授权、Anthropic 内部 workflow 拆解、多 agent 写 plan 工作流等多条联动信号。

**趋势信号**：
"模型 + harness + Skill"三件套正从分散叙事压成同一条工作流——独立开发者今天起讨论的不再是"用什么模型"，而是"配什么 harness、装什么 Skill、烧多少 token"。

**横向对比**（多个收入数据点 / 同主题信号）：
- 单产品深耕路径：Tony Dinh TypingMind $137K/m（约 ¥97 万）
- 产品矩阵路径：@levelsio 6 产品 $242K/m（约 ¥172 万）、Marc Lou 6 产品 $70K/m（约 ¥49.7 万）
- 内容 + 工具变现路径：Pat Walls Starter Story 8 年从 $0 到 $1.6M 再卖掉
- 模板分销路径：@indie_maker_fox 自述 2 年破 $100K，TanStarter 模板月销首次超过 ShipFast（数字未公开）
共同点：所有公开自述收入的作者都长期、公开建设个人品牌（author_bio 即广告位），收入数据本身就是用户获取渠道的一部分；脱离个人品牌只靠产品的路径在本期信号中未出现。

**当日强信号数 vs 噪音比**：
约 3 条强信号（Opus 4.8 / Skill 商用化 / PaywallPro）+ 多条中等信号（Anthropic 内部 workflow、TanStarter 收入声明、PPT/小红书 Skill 影响力等），整体噪音占比中等——欧洲空调、阿根廷罗马教皇等高 view 推文均被识别为娱乐 / 段子型噪音，未进入主体分析。

**本期信源**：
@claudeai @awilkinson @gregisenberg @_catwu @dotey @op7418 @lxfater @indie_maker_fox @thepatwalls @tdinh_me @levelsio @marclou @itsolelehmann @arvidkahl @Nicolascole77 @asmartbear @oran_ge @SimonHoiberg @Cydiar404 @gefei55 @lidangzzz @Jayyanginspires @Prathkum @stephsmithio @runes_leo @TrungTPhan @packyM @bentossell @cursor_ai @virushuo @FinanceYF5（共 31 位）
