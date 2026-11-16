# HN 书摘 · 2026-11-16（周一）

> 今日三句话：① Chase、美国银行、富国银行、U.S. Bank 与 Zelle 同日宕机，Chase 承认是本地硬件软件缺陷——叠加微软邮件（7 月补丁引入的缺陷）与联合航空故障，"系统性退化"从博客论点变成当日事实。② Qwen4-Max 发布，推理档位首次可完全关闭（none 档），848 分讨论区却在争论鹈鹕图基准是否已被训练数据污染。③ HN 招聘帖月均 287 条跌至 2013 年以来最低，同期 51.6% 的帖子提及 AI——AI 渗透与岗位收缩同向而行。

## Big Picture

Hacker News 是全球技术社区的公共议事厅，本页是对 2026-11-16 UTC 全天 73 条 ≥20 分帖子的每日书摘。当日的核心矛盾极其清晰：AI 能力供给端继续狂飙——Qwen4-Max 发布拿到 780 分、MIT 制造课把 AI agents 与 Edge AI 排进正式课表、uBlock Origin 的通用 XSS 由 GPT-5.6 Sol 主力找出；而软件基础设施消费端同日连环故障——五家大行加 Zelle、微软邮件服务、联合航空系统相继宕机，再往前推四周还有 PHP2Shell 与 5 月的 NPM 供应链劫持。社区开始用"系统性退化"描述 2026 年的软件质量，另一端则是招聘帖月均 287 条创 2013 年以来新低。我们认为，这组并置正是技术演化「形成」（Becoming）阶段的典型切面：生成与变异速度极快，而验证、运维等沉淀性能力的"遗传"落后于生成速度——本期头条、雷达与社区之声都围绕这一落差展开。本报告由三人接力完成，分工如下。

## 接力协作

### 分工

| 位置 | Agent | 负责栏目 |
| --- | --- | --- |
| 第 1 棒 | kevin_kelly | 全文初稿、Big Picture、接力协作、头条深读（1-2） |
| 第 2 棒（本轮） | tech_scout | 深化「值得一读」（3-7）与「技术雷达」（8-10），补写该两节的 tech_scout 视角；原样保留第 1 棒结论 |
| 第 3 棒 | 待接力 | 深化「社区之声」（11-12）、校验「数据速览」与全文事实溯源 |

后续 writer 只在自己的分工范围内深化，原样保留他人已写的段落与结论；如发现遗漏可补写并在上表标注。

## 头条深读

### 1. Technical issue at JPMorgan Chase triggers online banking delays for US banks（摩根大通技术故障触发美国多行网上银行延迟）

| 原文 | [Technical issue at JPMorgan Chase triggers online banking delays for US banks](https://news.ycombinator.com/item?id=50521045) |
| --- | --- |
| 摘要 | 11 月 16 日美国 Bank of America、Chase、U.S. Bank、Wells Fargo 与 Zelle 同时报宕机，Downdetector 出现集中故障报告。Chase 发言人 Joe Evangelisti 确认故障源于"本地硬件系统中的软件缺陷"，与网络攻击无关；Zelle 官方则否认自身故障。评论者 A_D_E_P_T 指出故障面（卡不可用、网点关闭、网银中断）与上月 Revolut 约 12 小时的宕机（起因为 Google Cloud 故障）高度相似。AP 正文 403 未能抓取，以上据 HN 评论区转述的声明与条目摘要。 |
| 批注 | 同日微软邮件服务故障（7 月补丁引入缺陷）与联合航空系统故障叠加，单点缺陷在高度耦合的云化与本地混合基础设施中级联放大——这是"软件系统性退化"叙事当天最硬的证据。 |
| 评论摘录 | 评论者 zenexer 引用 Chase 声明："JPMorgan Chase has experienced a temporary issue related to a software bug in an on-premise hardware system — it is not cyber-related"，并指出"看起来不是云厂商的锅"（[原文链接](https://news.ycombinator.com/item?id=50521045)） |

### 2. Qwen4-Max（通义千问 Qwen4-Max 发布）

| 原文 | [Qwen4-Max](https://news.ycombinator.com/item?id=50513215) |
| --- | --- |
| 摘要 | Qwen 发布 Qwen4-Max，推理强度首次提供 none / low / high / xhigh 四档，none 可完全关闭推理——上一代 Qwen3.8 Max 无法关闭推理，只能在 minimal 到 xhigh 五档中选择。官方博客为动态渲染页面，正文未能抓取，以上据 HN 评论区（396 条讨论）：作者 simonwillison 用其惯用的"Markdown 渲染鹈鹕图"横评各档输出，认为 4-Max 整体优于 3.8 Max，但仍偏好 3.8 的 xhigh 结果。 |
| 批注 | 可关闭推理意味着同一模型同时覆盖"快而便宜"与"慢而强"两端，推理计算量成为模型定价与路由的主轴；但评论区同时质疑鹈鹕图已被训练数据污染，社区对第三方基准的信任度在同步下降。 |
| 评论摘录 | 作者 simonwillison："Qwen4-Max has a none setting, but 3.8 Max didn't allow disabling reasoning."（[原文链接](https://news.ycombinator.com/item?id=50513215)） |

**kevin_kelly 视角：** 今天的头条组合是一次罕见的"同日对照实验"——能力端（Qwen4-Max 可关闭推理）与基础设施端（五家银行同日宕机）同时推进，暴露的不是 AI 泡沫，而是验证与运维能力的沉淀速度落后于生成速度。按 12 个必然筛子，这组信号同时命中「知化」「形成」「追踪」：方向确定，摩擦点在可靠性工程而非模型能力本身；故障潮是短期摩擦，不是长期趋势的反向证据。

## 值得一读

### 3. Amazon's Discount Illusion（亚马逊折扣幻觉：三分之一"促销"毫无优惠）

| 原文 | [Amazon's Discount Illusion: 1 in 3 "Deals" Offered No Savings – 1 in 10 Cost More](http://groundworkcollaborative.org/news/amazons-decoy-deals-groundwork-investigation-reveals-nearly-1-in-3-black-friday-and-cyber-monday-deals-advertised-by-amazon-offered-no-savings-to-shoppers-nearly-1-in-10-w) |
| --- | --- |
| 摘要 | Groundwork Collaborative 抽查 2024-2025 年黑五/网一 Amazon 官方 deals 页 350+ 商品：近 1/3 的"促销价"与促销前一个月持平或更高，近 1/10 比促销前更贵。具体案例：Hunter 女式黄雨靴促销价 $126.99，开促前 9 天售 $79.97（等贵 59%）；UGG Butte 男靴促销价 $179.98，约四周前售 $98.40（等贵 83%）。报告作者为 Breyon Williams、Elizabeth Pancotti 与 Lindsay Owens。 |
| 批注 | 发布方是消费政策倡导组织、立场并非中立，但方法可复核（逐商品比对促销前 30 天价格）；749 分 463 评论说明社区接受的是数据而非立场。"参考价"体系失效的直接后果是比价工具与价格历史插件的需求上升——信任缺口即产品机会。 |

### 4. Software is breaking down at a systemic level（软件正在系统性崩坏）

| 原文 | [Software is breaking down at a systemic level](https://www.breck-mckye.com/blog/2026/11/software-is-breaking-down-at-a-systemic-level/) |
| --- | --- |
| 摘要 | 作者把 2026 年的故障串成一条线：微软全球宕机 2 天后紧接 FAA 全美停飞、10 月 21 日 PHP2Shell（支撑全球约 70% 网站的 PHP 隐藏了十余年的内存记账缺陷被 AI 辅助利用）、eMudhra 数千张 SSL 证书私钥泄露、5 月 NPM "Shai Hulud" 供应链劫持。结论：这些故障没有共同的直接原因，却共享同一个结构——"由低质量零件构成的高复杂系统"；AI 既是诱因（研究者数小时找到复杂漏洞）也是症状，真正的断裂点在"我们建造软件的整套方式"。 |
| 批注 | HN 评论区当天就完成了一轮归因对抗：最高赞评论者 doug_durham 反驳时间线（云计算 16 年前就已成熟，问题是随算力规模放大而非质量退化），评论者 swatcoder 则给出四点结构解释——云厂商集中制造共因故障点、胖客户端迁向瘦客户端、依赖优先开发只审查表层代码、团队任期缩短失去资深 owner。争论焦点已从"是否在退化"转向"退化的机制是什么"，这本身就是叙事从博客观点变成主流议题的标志。 |

### 5. Universal XSS in uBlock Origin from website-driven element picker（uBlock Origin 元素选择器引发通用 XSS）

| 原文 | [Universal XSS in uBlock Origin from website-driven element picker](https://iter.ca/post/ubo-uxss/) |
| --- | --- |
| 摘要 | 安全研究者 Smitty van Bodegom 披露 uBlock Origin（Firefox MV2 版）一键通用 XSS：恶意网站可嵌入元素选择器的扩展 iframe，驱动其写入"受信任过滤器"，进而向任意站点注入执行任意 JavaScript。利用链分四步：从 uAssets 的 lootdest 过滤规则（no-fetch-if 钩住 fetch 后发 XHR 到 moz-extension://<UUID>/…）反钩 XHR 提取随机扩展 UUID；构造 opacity 0 的隐形 iframe 嵌入选择器；驱动其写入目标过滤器；把隐形"Create"按钮摆到用户鼠标下诱导点击。MV3 的 uBO Lite 存在同类但较轻的问题；已修复（GitHub advisory）。作者称 GPT-5.6 Sol 找出了该漏洞、Claude 编写了大部分 PoC 代码，文章文字由本人撰写。 |
| 批注 | 通用 XSS 是浏览器扩展威胁模型的最高等级（任意站点上下文执行任意 JS），而利用链的第一步竟是"广告拦截规则自己泄露扩展 UUID"——安全默认值在真实部署中被过滤规则生态抵消。AI 分工模式（AI 提假说、人验证、AI 写 PoC）与第 8 条 Lean 互为镜像：发现已自动化，验证仍靠人。 |

### 6. "Who is Hiring?" postings stuck near 12-year lows as AI reaches half of all jobs（HN 招聘帖跌至 12 年低位，AI 出现在半数岗位）

| 原文 | ["Who is Hiring?" postings stuck near 12-year lows as AI reaches half of all jobs](https://www.hntrends.com/2026/november.html) |
| --- | --- |
| 摘要 | hntrends 中断两年半后恢复更新，覆盖大量积压变化。截至 11 月 14 日当月招聘线程 244 条，同比 -37%（去年同期 387 条）；7 月以来每期落在 224-255 条区间，8 月的 224 条为 2014 年 1 月以来最少；2026 年月均 287 条，为 2013 年以来最低年均值。同时 AI 提及率 51.6%（两年前 30%，2026 年 6 月首破 50%），仅次于 Remote；AI agents（含 agentic）14.8% 已超 LLM 的 10.7%，MCP 从一年前 0.3% 升至 4.5%（榜单涨幅最大），传统 machine learning 标签从 14.8% 降至 11.5%。语言榜 Python 22.1%、TypeScript 17.6%（一年前 22.5%）、Rust 升至 8.2%（一年前 4.9%，近五个月中四个月压过 Go）。岗位结构（三月均值）：前端从 2022 年初 27% 跌至 6.6%（一年前 15.6%），Full Stack 26.2%→20.1%、Back End 23.6%→18.8%；Senior 稳定在约 30%，Staff 自 2019 年约翻两番至约 12%，Junior 仅约 3%；Remote 55.7%。新增词条包括 RAG、LangChain、Anthropic、pgvector、Bun、Deno。 |
| 批注 | 前端岗位四年跌 76% 是全榜单最陡的岗位曲线，且过去一年的跌幅集中在最近几个月——岗位收缩不是线性趋势而是正在加速。Rust 从 4.9% 到 8.2% 用一年完成对 Go 的反超，招聘数据是语言热度的领先指标（领先社区讨论约 1-2 年）。AI 提及 51.6% 与岗位总量 -37% 同向：AI 在招聘文本里渗透的不是新岗位，而是存量岗位的技能要求改写。 |

### 7. How to Make Almost Anything（MIT "如何制造（几乎）任何东西" 2026 课程站）

| 原文 | [How To Make (almost) Anything — MAS.863 2026](https://pub.cba.mit.edu/863.26/site/) |
| --- | --- |
| 摘要 | MIT 传奇制造课 MAS.863 2026 秋季课表上线：每周三 13:00-16:00 于 E14-633，主题依次为 CAD、计算机控制切割、嵌入式编程、电子设计、3D 扫描打印、数控加工、机械设计、网络与系统集成，12 月 15 日结课展示与期末考。与往年的差异在辅课表（recitation）：10 月 1 日为 AI agents、10 月 29 日为 Edge AI（课件与代码已挂出），其余 recitation 仍是版本控制、电子、EDA、调试、CAM 等传统主题。该条 ▲796 为当日全站最高分。 |
| 批注 | 两个 AI 话题被安插在"3D 扫描打印"与"输入设备"之间，说明课程把 AI 当作制造工具链的一环而非独立主题——这是"AI 嵌入物理世界"最早的课程表级信号，方向与招聘榜 AI agents 14.8% 互相印证；▲796 当日最高分也说明社区对"动手造东西"的饥渴远超对又一个模型发布的饥渴。 |

## 技术雷达

### 8. "...and the proof is checked in Lean"（"……而且证明是在 Lean 里检查过的"）

| 原文 | [...and the proof is checked in Lean](https://xenaproject.wordpress.com/2026/11/12/and-the-proof-is-checked-in-lean/) |
| --- | --- |
| 摘要 | 面对 OpenAI 上月发布的 722 篇定理汇编（约 45% 附 Lean 代码，其中 3 篇已因符号错误撤稿），Xena 项目给出判断"在 Lean 里检查过"是否可信的四问清单，第一问即最关键：Lean 语句是否对应论文中的非形式化语句。文中举例一段能完全编译的"费马大定理"定义——`∀ a b c n : ℕ, n ≥ 3 → a^n + b^n ≠ c^n`——因自然数含 0，a=b=c=0、n=3 即构成反例，是平凡假命题，但编译照样通过（只有证明会失败）；Lean 严格区分"定理语句"与"证明"，而人类习惯把两者都叫"定理"。作者同时指出：Lean 曾有 soundness 缺陷且可能再有、AI 会 reward hack，因此两端极端说法都不对；对 AI 生成的仓库，这些问题大多尚未被系统性回答——"没有理由认为测试会失败，只是还没人做"；Mathlib 之外的库（如 DeepMind Formal Conjectures 中 Hodge 猜想的形式化依赖超 1 万行代码）尚无专家级审查。 |
| 批注 | 这是"验证层滞后于生成层"最精确的技术表达：编译通过 ≠ 语句正确，社区讨论已从"AI 能否证明"转向"证明的是不是它声称的东西"——后者才是形式化验证可信度的真正瓶颈。 |

### 9. Frame – 31.5" color ePaper display（Frame：31.5 英寸全彩电子纸显示屏）

| 原文 | [Frame – 31.5" color ePaper display](https://trmnl.com/blog/introducing-frame) |
| --- | --- |
| 摘要 | TRMNL 发布第三代产品 Frame：31.5 英寸全彩 ePaper 屏、手工木框（自建木工车间）、首批约 470 台，2026 年底前发少量、主力交付在 2027 年初。差异化点：Clock Sync 按日定时刷新（相对"每 N 分钟"节奏，减少闪屏并延长续航）、microSD 完全离线模式（零个人信息回传服务器）、后置常供电 USB-C 开孔，配套自研 Lazarus 抖动与 LUT 色彩方案。创始人 2013 年曾创办 ArtSpot（纽约咖啡馆寄卖本地艺术），失败后 5 年以 +13% 利息偿还投资人，TRMNL 是同一愿景的第三次尝试。 |
| 批注 | 470 台首批量产是 creator 硬件模式而非消费电子量产，出货量本身无信号价值；信号在需求端验证——常显、低功耗、离线、零遥测的"安静屏幕"若能在 470 人处成立，下一档才是放大问题。按 S 曲线处于导入期，观察点是 2027 年 Q1 交付后的复购与二手溢价。 |

### 10. Coral – Open-source gateway where agents write their own tools（Coral：让 agent 自己写工具的开源网关）

| 原文 | [Coral – Open-source gateway where agents write their own tools](https://github.com/withcoral/coral) |
| --- | --- |
| 摘要 | Show HN 发布 Coral：自托管开源网关，口号"Execution rails for agents"，位于 agent 与其操作的系统之间。agent 不调用预定义工具，而是现场编写短 TypeScript 程序作为工具调用，能用即存为可复用自定义工具；Coral 在注入凭据前对每次 provider 调用按策略做 Allow/Ask/Block 检查。差异化论点直指 MCP 网关："多数网关只决定 agent 能看见哪些工具，是全有或全无"，而自定义工具是代码，可承载更细规则（README 举例：closeStaleTicket 只改 30 天无活动工单的一个字段）。代码库为 Rust（Cargo/crates，1,547 次提交），提供 macOS/Windows/Linux 桌面端与 Docker Compose/Kubernetes 服务端（需 OIDC、反向代理、SQLite/Postgres），provider 目录支持 GitHub/Linear 等，可自带 OpenAPI 或 MCP server；默认读操作直通、写操作需审批。README 声称"450+ 公司、数千开发者"在用，该数字暂无独立验证。 |
| 批注 | "agent 自写工具"把工具安全问题从清单治理（可见哪些工具）推到代码治理（生成的代码做什么），策略层必须跟上工具生成速度——这正是当日头条（故障）与雷达第 8 条（验证）的同构问题在 agent 基础设施上的重演。采用声明自报且 Show HN 仅 50 分 24 评论，属早期信号，按 S 曲线处于导入期的开发者体验阶段。 |

**tech_scout 视角：** 按信噪比给这三条标置信度：Lean 中高（Xena + OpenAI 722 篇汇编 + 3 篇撤稿多源交叉，方向明确），Coral 低（单一信源、采用数据自报），Frame 低（单点 creator 硬件信号）。雷达的高信噪比其实不在单条，而在第 8 条与第 5 条的交叉——同一天两条独立帖子指向同一件事：AI 产出的验证（定理语句、漏洞 PoC、agent 生成的工具代码）正在成为新瓶颈，而验证形式化本身还停在导入期。Frame、Coral 属"脉冲式热度"类别，判据是 3 个月后是否仍在榜或出现独立用户复述；届时再决定上调还是下调置信度。

**kevin_kelly 视角：** 雷达三条共同指向一个判断：AI 的下一瓶颈不是生成而是验证。Lean 那篇讲的是"AI 产出的定理要先证明语句对了才可信"，uBO 漏洞讲的是"AI 已进入漏洞发现主力但修复仍靠人裁剪"，Coral 讲的是"agent 自写工具需要网关级隔离"——匹配「知化」与「重混」的必然方向，但落地速度取决于验证层的成熟度。Frame 这类低功耗常显硬件则命中「屏读」与「使用」，属于会慢但不会错的方向；Coral 当前更接近早期变异，是否被市场选择（遗传为基础设施）尚需观察。

## 社区之声

### 11. Ask HN: If AI tools are so good, why isn't your bug backlog empty?（如果 AI 工具真这么强，为什么你的 bug 队列还没清空？）

| 原文 | [Ask HN: If AI tools are so good, why isn't your bug backlog empty?](https://news.ycombinator.com/item?id=50520076) |
| --- | --- |
| 摘要 | 提问者（作者 ex-aws-dude）质疑：若 AI 将取代程序员，bug 队列早该清空、功能需求早该被反超，但自己和业内多数同行并非如此。高赞回复分化：评论者 td521534f12 称个人项目 backlog 确已接近清空、团队瓶颈在代码评审；评论者 sockaddr 反驳"个人项目 bug 只是尚未被发现，检测瓶颈在开发者本人"；评论者 frostiness 称让 agent 修 bug 通常只针对症状补代码，很少消除整类问题；评论者 td521534f12 另指出受监管行业的人工评审短期内不会消失。 |

### 12. Tell HN: HN is being scraped for emails to scam（HN 正被爬取邮箱用于诈骗）

| 原文 | [Tell HN: HN is being scraped for emails to scam](https://news.ycombinator.com/item?id=50513451) |
| --- | --- |
| 摘要 | 作者 eks391 提醒 "Who's for Hire" 月度页的公开邮箱正被爬去发钓鱼邮件——其使用一站一邮箱，因此一眼识破了伪装成"AWS 付款延迟"的诈骗信，并建议悬停查看发件域名与链接域名。评论区补充：评论者 btrettel 改用图片形式贴一次性邮箱后信噪比大幅提升；作者 david_allison 表示后悔在招聘帖留主邮箱，dang 回应相关帖子可随时删除，评论者 tasuki 补充"已经泄露的收不回来"。 |

## 数据速览（今日 Top10 全量快照）

| # | 原文标题 | 中文标题 | 分数 | 评论 |
| --- | --- | --- | --- | --- |
| 1 | [How to Make Almost Anything](https://news.ycombinator.com/item?id=50514470) | MIT《如何制造（几乎）任何东西》2026 课程站 | 796 | 133 |
| 2 | [Qwen4-Max](https://news.ycombinator.com/item?id=50513215) | 通义千问 Qwen4-Max 发布 | 780 | 396 |
| 3 | [Amazon's Discount Illusion](http://groundworkcollaborative.org/news/amazons-decoy-deals-groundwork-investigation-reveals-nearly-1-in-3-black-friday-and-cyber-monday-deals-advertised-by-amazon-offered-no-savings-to-shoppers-nearly-1-in-10-w) | 亚马逊折扣幻觉：1/3 促销无优惠 | 749 | 463 |
| 4 | [Universal XSS in uBlock Origin](https://iter.ca/post/ubo-uxss/) | uBlock Origin 通用 XSS | 542 | 157 |
| 5 | [What the fuck is w2rt6byl5nf1opmc-a.com?](https://jack.cab/blog/siterate) | w2rt6byl5nf1opmc-a.com 是什么鬼 | 305 | 139 |
| 6 | [Outages reported at Bank of America, Chase, U.S. Bank, Wells Fargo and Zelle](https://apnews.com/article/bank-outage-chase-wells-fargo-truist-50fee2693c22f597fa6ca51a97ef2cda) | 美五大银行与 Zelle 同日宕机 | 301 | 196 |
| 7 | [The Secret ThinkPad Powerbutton Code to Bring Dead Laptops Back to Life (2007)](https://masnick.com/posts/the-secret-thinkpad-powerbutton-code-to-bring-dead-laptops-back-to-life/) | ThinkPad 秘密电源键代码救活变砖笔记本（2007） | 259 | 103 |
| 8 | [...and the proof is checked in Lean](https://xenaproject.wordpress.com/2026/11/12/and-the-proof-is-checked-in-lean/) | "证明是在 Lean 里检查过的" | 240 | 106 |
| 9 | [Tor Project Issues Rapid-Response DoS-Defense Fix](https://forum.torproject.org/t/security-release-0-4-9-17/22454) | Tor 应对持续 DDoS 发布快速修复 | 221 | 56 |
| 10 | [Soldier files whistleblower complaint over Iran strike that killed 6 U.S. troops](https://www.cnn.com/2026/11/15/politics/army-soldier-whistleblower-complaint) | 士兵就伊朗打击致 6 名美军死亡提起举报 | 207 | 69 |

---

**reference.md 追加内容（非稿件正文，待写入主题工作区）：**

```
- 美五大银行+Zelle 同日宕机（Chase 称本地硬件软件缺陷、非网络攻击）: query_raw_items(source=hackernews, published_after=2026-11-16T00:00:00Z)[id:785829] = Outages reported at Bank of America, Chase, U.S. Bank, Wells Fargo and Zelle
- HN 实时热度 670 分/531 评论及评论区转述的 Chase 声明: fetch_url(https://news.ycombinator.com/item?id=50521045) = Technical issue at JPMorgan Chase triggers online banking delays for US banks
- Qwen4-Max 发布及 none/low/high/xhigh 四档推理与 simonwillison 评论: fetch_url(https://qwen.ai/blog?id=qwen4-max) = 官方博客动态渲染正文未能抓取，据 HN 评论区（396 条讨论）[id:782050]
- 亚马逊黑五/网一 350+ 商品促销价抽查（1/3 无优惠、1/10 更贵）: fetch_url(http://groundworkcollaborative.org/news/amazons-decoy-deals-...) = Groundwork Collaborative 报告 [id:784896]
- 2026 软件系统性故障梳理（微软 2 天宕机、FAA 停飞、PHP2Shell、eMudhra、Shai Hulud）: fetch_url(https://www.breck-mckye.com/blog/2026/11/software-is-breaking-down-at-a-systemic-level/) = 博文正文 [id:785698]
- HN 评论区归因对抗（doug_durham 反驳时间线、swatcoder 四点结构解释）: fetch_url(https://news.ycombinator.com/item?id=50520866) = HN 评论页
- uBlock Origin 通用 XSS 完整利用链（lootdest fetch 钩子泄露 UUID、隐形 iframe 驱动 Create 按钮）: fetch_url(https://iter.ca/post/ubo-uxss/) = 博文正文 [id:782049]
- HN 招聘帖 11/14 为 244 条（同比 -37%）、2026 月均 287 条（2013 以来最低）、AI 提及 51.6%、AI agents 14.8%、MCP 4.5%、Rust 8.2%、前端 6.6%、Staff 约 12%: fetch_url(https://www.hntrends.com/2026/november.html) = hntrends 2026-11 统计（中断两年半后恢复更新）[id:781937]
- MIT MAS.863 2026 完整课表（周三 13:00-16:00 E14-633，recitation 10/01 AI agents、10/29 Edge AI，12/15 结课）: fetch_url(https://pub.cba.mit.edu/863.26/site/) = 课程站正文 [id:782738]
- OpenAI 定理汇编 722 篇、约 45% 附 Lean 代码、3 篇因符号错误撤稿、FLT 平凡假命题编译例与四问清单: fetch_url(https://xenaproject.wordpress.com/2026/11/12/and-the-proof-is-checked-in-lean/) = Xena 博文正文 [id:784168]
- TRMNL Frame 31.5 英寸全彩 ePaper、首批约 470 台、Clock Sync/离线模式、创始人 ArtSpot 经历: fetch_url(https://trmnl.com/blog/introducing-frame) = 产品公告正文 [id:785694]
- Coral README（Execution rails for agents、Rust 1547 commits、Allow/Ask/Block 策略、450+ 公司自报采用）: fetch_url(https://github.com/withcoral/coral) = GitHub README [id:784898]
- Ask HN bug backlog 讨论（评审瓶颈、症状式修复）: fetch_url(https://news.ycombinator.com/item?id=50520076) = HN 评论页 [id:785651]
- Tell HN 邮箱爬取诈骗讨论: fetch_url(https://news.ycombinator.com/item?id=50513451) = HN 评论页 [id:782359]
- 今日 Top10 快照（796/780/749/542/305/301/259/240/221/207 分）: query_raw_items(source=hackernews, published_after=2026-11-16T00:00:00Z, published_before=2026-11-17T00:00:00Z) = 73 条 ≥20 分条目
```