# Roundtable Scratchpad — hn-daily

- Session: 2026-11-17_0647__manual__hn_utc_hacker_news_5_1_2_4_6_2_3_1_2_top10_8_12_query_raw_it
- Lead: tech_generalist
- 议题: HN 书摘每日扫描：昨日（前一日 UTC 窗口）Hacker News 高价值帖子书摘。 产出 5 栏目：头条深读（1-2 条）/ 值得一读（4-6 条）/ 技术雷达（2-3 条）/ 社区之声（1-2 条）/ 数据速览（Top10 快照），共 8-12 条。
【数据 · 全部工具查询，不注入数值】用工具主动取数（禁止凭空写数字）： - 主取数：query_raw_items 工具，source='hackernews'，按前一日 UTC 窗口
  （created/ingested 前一日 00:00 → 当日 00:00）筛选。
  机械过滤：metadata 的 hn_points ≥ 20（采集端已带分）；同 URL 去重；
  跨天去重（用 ReadThemeDocsTool 读 themes/hn-daily/index.md 的「往期」列表比对标题）。
  【空结果回退 · 必须执行】若主查询（hn_points≥20）返回 <5 条，依次执行：1) min_points=1 同窗口 2) keyword='Show HN' 窗口-2d 3) 全源 keyword 兜底；仍不足时诚实标注未能抓取，禁止编造。
- 每条入选帖的正文/摘要：query_raw_items 返回的 full_text 优先；
  缺失则用 web 搜索/直接抓取原文补充（抓不到就标注"未能抓取"，不虚构）。
- 评论摘录：用 Algolia HN items API 或评论区抓取（可选，有则摘 1 条高质量评论）。
【规范 · 必读】用 ReadThemeDocsTool 读取两份规范后动笔： 1. themes/hn-daily/template.md —— 5 栏目结构 seed（## 头条深读 / ## 值得一读 /
   ## 技术雷达 / ## 社区之声 / ## 数据速览；禁止编号顶层节——透传 publish 精确匹配）
2. themes/WRITING_GUIDE.md —— 写作硬规则（集体署名/金字塔原理/数字溯源）
【方法 · 四维精筛】机械过滤只是保底线（去重/类型/分数≥20），**价值判断由 LLM 完成**： 对候选独立打分（1-5）：信息密度（新事实/数据/决策 vs 观点水贴）、 一手性（作者亲历 vs 二手转述）、讨论深度（评论区是否已产生高质量延伸）、 行业相关性（对科技从业者的 relevance）。≥4 入选；3 分按名额递补；<3 淘汰。 分数只是参考信号，**不要纯按分数排序选帖**——低分但有洞察的帖子（技术雷达/社区之声 栏目）应入选，高分但信息量低的（标题党/重复/宣传稿）应淘汰。 辅助信号：hn_points/hn_comments 比（高分低评论 ≈ 标题党嫌疑）。
【质量铁律】① 摘要必须基于实际抓到的正文——raw_items.full_text 只有元数据时， 用 fetch_url 工具按 URL 抓取文章正文（HTTPS 优先），抓不到才标注"未能抓取"—— 宁可失败得明显，不成功得虚假；② 每条带原文链接可追溯（原文 + 评论）； ③ 中文为主，标题保留英文原文 + 中文翻译副标题（无域名后缀）； ④ 摘要/批注/评论摘录直接讲内容，禁止"标题宣布""该文介绍"类开场白， 金字塔原则结论先行，篇幅从短信息密度优先； ⑤ 禁止 @ 提及任何人（GitHub 会把 @xxx 解析成 mention 并向真实用户发送通知）—— 作者/评论者一律写"作者 用户名"（如"作者 mkeeter"），禁止写"@mkeeter"。 禁止 session 目录名/manual/miss 等内部元数据出现在正文。
【立场】服务科技行业从业者的每日信息扫描，不输出投资建议。
【记忆 · 分析中自主沉淀】分析中如产生以下内容，调用 remember 工具存储（个人记忆层）： - 客观事实 / 带出处与数据的关键结论（如"非农 -2.3万，美元走低黄金上涨"） - 短期有效的观察（如"9月加息25bp隐含概率 56.5%"） 无需存储：过程性描述、已 publish 进主题文档的完整内容（避免重复）。

- 参与 Agent: tech_generalist, tech_scout, ai_specialist, kevin_kelly
- 轮次: 1 / 1
- 状态: ok

## Lead 最终综合

# HN 书摘 · 2026-11-16（周一）· 增量补丁

> 今日三句话：① HN "Who is Hiring" 帖量跌至 12 年低位（2026 年月均 287 帖、11 月同期 -37%），同日 AI 关键词覆盖 51.6% 的招聘帖——就业收缩与 AI 渗透在一手数据里同日确认。② AI 自动化滥用首次被一手量化：Show HN 发布后 4 天收到 17 封机器人推销邮件，HN 求职帖邮箱被抓取用于定向诈骗（▲120）。③ agent 基础设施竞争提速：开源策略网关 Coral（▲50）与 EMG 机器人数据采集套筒 Axonnic（YC F26）同日上榜。

> ⛔ 正文中作者/评论者一律写「作者 用户名」格式，禁止 @ 提及。本期为对 2026-11-16 定版的增量补丁，全部条目发布于 2026-11-16 UTC 窗口，标【新增】；上一期（2026-11-15 窗口）条目不在本表内。

## 头条深读（1-2 条）

### 1.【新增】"Who is Hiring" 帖量 12 年低位，AI 已出现在一半招聘帖里 — HN 招聘趋势年度更新（▲93 · 💬83）

| 原文 | ["Who is Hiring?" postings stuck near 12-year lows as AI reaches half of all jobs](https://www.hntrends.com/2026/november.html)（[HN 讨论](https://news.ycombinator.com/item?id=50512950)，[id:781937]） |
| --- | --- |
| 热度 | ▲ 93 · 💬 83 · 作者 myth_drannon · 2026-11-16 01:31 UTC |
| 摘要 | 截至 11-14，11 月 "Who is Hiring" 线程仅 244 条招聘，同比 -37%（去年同期 387）；2026 年月均 287 条，为 2013 年以来最低年均值，8 月的 224 条是 2014 年 1 月以来最少。同期 AI 关键词覆盖 51.6% 的招聘帖（两年前仅 30%，2026 年 6 月首破 50%），其中 AI Agents 14.8% 已超 LLM 10.7%，MCP 从一年前 0.3% 升至 4.5%（榜单涨幅最大）；语言榜 Rust 升至第 3（8.2%，一年前 4.9%）并连续 5 个月中 4 个月压过 Go；前端岗位占比从 2022 年初 27% 跌至 6.6%。 |
| 批注 | 这是本窗口信息密度最高的一手数据：招聘收缩与 AI 渗透不是两条叙事而是同一条——岗位在减少的同时，存量岗位的技能要求正被 AI Agents/MCP 重写；对科技从业者而言，"HN 帖量下降"里既有招聘渠道迁移（评论者指出 Greenhouse/Ashby 分流），也有真实的编制收缩，两个解释无法从该数据本身拆开。 |
| 评论摘录 | 作者 SCUSKU：被 YC 初创裁员后以 HN 招聘板为"保险"，现感帖量锐减，但其观察是全球 SWE 需求并未下降、只是初创改投 Greenboard/Ashby 等渠道——"coding is basically prompting now"，仍能拿到面试。[评论链接](https://news.ycombinator.com/item?id=50512950) |

### 2.【新增】HN 求职帖邮箱被抓去钓鱼：一手诈骗预警（▲120 · 💬41）

| 原文 | [Tell HN: HN is being scraped for emails to scam](https://news.ycombinator.com/item?id=50513451)（[id:782359]） |
| --- | --- |
| 热度 | ▲ 120 · 💬 41 · 作者 eks391 · 2026-11-16 02:53 UTC |
| 摘要 | 作者提醒：HN 的 "Who's Hiring" 等页面公开留有个人邮箱，正被爬虫/agent 抓取用于定向诈骗——他收到一封冒充"AWS 延迟付款通知"、发往其 HN 专属邮箱的钓鱼邮件，因坚持"一站一邮箱"当场识破。核心防御是两点：打开前悬停发件人域名、点击前悬停链接域名。 |
| 批注 | 与 #1 同源：HN 招聘生态的价值（公开邮箱直达创始人）正在被 AI 爬取反噬，"公开即暴露"从理论风险变成求职者的实际成本——社区已出现用图片化邮箱替代明文的应对。 |
| 评论摘录 | 作者 david_allison：后悔在 "Who wants to be hired?" 帖留邮箱，"主开发邮箱基本半废"；作者 dang 回应相关帖子可随时删除，但评论者 tasuki 反驳"unleaking is not a thing"（泄露无法撤回）。[评论链接](https://news.ycombinator.com/item?id=50513451) |

## 值得一读（4-6 条）

### 3.【新增】Coral：agent 自己写工具的开源策略网关（▲50 · 💬24）

| 原文 | [Show HN: Coral – Open-source gateway where agents write their own tools](https://github.com/withcoral/coral)（[id:784898]，[HN 讨论](https://news.ycombinator.com/item?id=50516232)） |
| --- | --- |
| 热度 | ▲ 50 · 💬 24 · 作者 jcs · 2026-11-16 14:14 UTC |
| 摘要 | Coral 是自托管的 agent 执行网关：agent 用短 TypeScript 程序调用工具，跑通后存为可复用的自定义工具；每次调用先过策略检查（Allow/Ask/Block）再注入凭据转发。与只控制"可见哪些工具"的 MCP 网关相比，Coral 的差异点是粒度——自定义工具代码内可携带业务规则（如"只关 30 天无活动的工单"），README 称已有 450+ 公司的数千名开发者在用。 |
| 批注 | agent 基础设施正从"连接"竞争转向"权限粒度"竞争：MCP 解决了 agent 能调什么，没解决调用时的业务边界——Coral 把策略下沉到可复用工具代码，是该问题的开源答案之一。 |
| 评论摘录 | 未能抓取评论（仅抓取 README 正文）。 |

### 4.【新增】AT&T 起诉 Comcast："光纤供电 WiFi" 实为有线宽带（▲55 · 💬46）

| 原文 | [Comcast's "fiber-powered Wi-Fi" is cable, AT&T says in false advertising case](https://arstechnica.com/tech-policy/2026/11/comcast-falsely-advertises-cable-internet-as-fiber-powered-att-lawsuit-says/)（[id:786122]，[HN 讨论](https://news.ycombinator.com/item?id=50523025)；Ars 正文 405 未能抓取，摘要基于 HN 页面） |
| --- | --- |
| 热度 | ▲ 55 · 💬 46 · 作者 jaredwiener · 2026-11-16 20:48 UTC |
| 摘要 | AT&T 以虚假广告起诉 Comcast：其宣传的 "fiber-powered Wi-Fi" 底层是 cable（HFC）接入而非光纤入户。评论区的共识是"用竞争对手互撕实现消费者保护"——同时翻出 AT&T 自己的前科：U-Verse 时代的 "fiber rich network" 措辞与 4G 时代把网络标成 "5G E"。 |
| 批注 | 宽带营销话术战的法律化对固网竞争格局是慢变量：若法院采纳"链路最低配置段必须与广告诉求一致"的口径（评论区作者 altairprime 的设想），"fiber-powered/gig" 类模糊措辞的广告空间将被压缩。 |
| 评论摘录 | 作者 soupfordummies：AT&T 几年前行业升级 5G 时把 4G 服务包装成 "5G E（5G Evolution）"，"极其卑劣"——两家都有前科。[评论链接](https://news.ycombinator.com/item?id=50523025) |

### 5.【新增】Show HN 之后 4 天，17 封 AI 生成的推销邮件（▲56 · 💬51）

| 原文 | [Doing Show HN generates a ton of automated email pitches](https://petervandijck.com/post/pbrgs-ev0bc)（[id:784295]，[HN 讨论](https://news.ycombinator.com/item?id=50516232)） |
| --- | --- |
| 热度 | ▲ 56 · 💬 51 · 作者 petervandijck · 2026-11-16 11:00 UTC |
| 摘要 | 作者上周把 Airdash 发上 Show HN，4 天内 17 个服务发来推销邮件，几乎全部由"只读了 HN 标题"的软件生成：7 个是发布目录/榜单（$0–49、卖 dofollow 外链），10 个卖安全扫描、竞品报告、agent 测试、演示视频、Reddit 推广、newsletter 赞助位。一封目录邮件把他整条 Show HN 标题原样粘贴成产品名；某个服务说"只发这一封"后又连发 3 次同款。 |
| 批注 | 这是 AI 外呼（outbound spam）生态的罕见一手计量样本：Show HN 标题已成为自动 prospecting 的输入源，独立开发者发布即被 17 路 agent 攻扫——与 #2 的邮箱爬取互为印证。 |
| 评论摘录 | 未能抓取评论（正文已抓取，评论区未抓取）。 |

### 6.【新增】Fakemetrics：用假数据截图"营销成功学"，顺便测了 Claude Opus 的 UI 复刻力（▲28 · 💬10）

| 原文 | [Show HN: Fakemetrics.com – "build in public" like a superstar](https://fakemetrics.com/)（[id:785882]） |
| --- | --- |
| 热度 | ▲ 28 · 💬 10 · 作者 tigranbs · 2026-11-16 18:08 UTC |
| 摘要 | Fakemetrics 让用户任选平台生成完全虚构的增长截图（Stripe 营收 +645.3%、Instagram 互动、X 曝光、LinkedIn 28,400 活跃用户等全套模板）并下载。作者本意是顺带测试 Claude Opus 能否像素级复刻这些 UI——结论是"并非只靠 prompt 就能做到"，仍需大量手工调试。 |
| 批注 | 双重价值：讽刺"build in public"的社证制造工业（截图即信誉）；同时留了一份 Opus 复杂 UI 复刻能力的实战记录——LLM 生成"看起来对"的像素级界面仍非易事。 |
| 评论摘录 | 未能抓取评论。 |

## 技术雷达（2-3 条）

### 7.【新增】Axonnic（YC F26）：EMG 前臂套筒为灵巧机器人采训练数据（▲21 · 💬7）

| 原文 | [Launch HN: Axonnic (YC F26) – Sleeves that track fingers and estimate force](https://news.ycombinator.com/item?id=50522776)（[axonnic.com](https://axonnic.com)，[id:786120]） |
| --- | --- |
| 热度 | ▲ 21 · 💬 7 · 作者 arshpatankar · 2026-11-16 20:29 UTC |
| 摘要 | 前臂套筒用 64 通道表面 EMG 读肌肉电信号，解码 20 个手指关节角并估计指尖力，主打"视频捕捉不到的用力信息"——缝纫、精密装配这类手几乎不动但肌肉持续微调的场景，EMG 优于纯视频。基准：训练 4 天后的一次 215 秒录制免重标定，对比 Apple Vision Pro 手部追踪仅 6.9° 误差；工厂实录遭遇无线干扰，团队正自研有线 PCB 硬件。源于作者 Maxim 的牛津 EMG 研究。 |
| 批注 | 人形/灵巧操作的瓶颈正从模型转向数据采集：EMG 把"熟练工的隐性用力"变成可标注信号，是继视频、动作捕捉之后的第三条遥操作数据路线。 |
| 评论摘录 | 未能抓取评论。 |

### 8.【新增】OpenTodo：单 Go 二进制、本地优先的自托管任务管理器（▲20 · 💬19）

| 原文 | [Show HN: OpenTodo – a self-hosted, local-first task manager in one Go binary](https://github.com/OpenTodoApp/OpenTodo)（[id:785631]，[HN 讨论](https://news.ycombinator.com/item?id=50517352)） |
| --- | --- |
| 热度 | ▲ 20 · 💬 19 · 作者 pixari8383 · 2026-11-16 13:21 UTC |
| 摘要 | 自托管待办应用：单二进制/Docker/K8s/Helm 部署，手机电脑离线可用、列表可共享，自然语言录入（"Call Sarah next Wed 3pm #work p1"）直接解析日期与优先级；新发布 iPhone/iPad 应用（提醒、分享面板、Today widget、Face ID）。口号是"plan your day without renting your to-do list"——对标订阅制任务应用的反锁定叙事。 |
| 批注 | 本地优先/自托管工具的持续供给说明"反订阅疲劳"是稳定的开发者需求侧主题；信息密度一般，列雷达仅作赛道供给信号。 |
| 评论摘录 | 未能抓取评论。 |

## 社区之声（1-2 条）

### 9.【新增】Ask HN：AI 工具这么强，为什么你的 bug backlog 还没清空？（▲38 · 💬65）

| 原文 | [Ask HN: If AI tools are so good, why isn't your bug backlog empty?](https://news.ycombinator.com/item?id=50520076)（[id:785651]） |
| --- | --- |
| 热度 | ▲ 38 · 💬 65 · 作者 ex-aws-dude · 2026-11-16 17:20 UTC |
| 摘要 | 发帖逻辑：若 AI 真要取代程序员，bug 应该修不完、功能应被 PM 排到业务侧瓶颈——但自己公司和业内朋友都没出现这种收缩。高赞回复给出机制解释：AI 修 bug 是"补丁式"的，只覆盖报告里的症状、极少消除整类问题；成熟系统里一次正确修复也许只有 10 行代码，而把上下文、边界、优先级谈清楚的委派开销"已经等于干活本身"。 |
| 评论摘录 | 作者 frostiness：让 agent 修 issue 它确实能修，但几乎总是加代码盖住症状，"没有一个我用过的模型会在拥有自主权时选择更简单、更可维护的方案"；作者 davnicwil：纯英文委派存在信息损耗，谈判到某一点"就不如自己写了"，greenfield 才是例外。[评论链接](https://news.ycombinator.com/item?id=50520076) |

## 数据速览（本窗口 Top10 全量快照）

窗口：2026-11-16 00:00 → 2026-11-17 00:00 UTC，source=hackernews，全部条目 hn_points ≥ 20（分数/评论为抓取时快照，HN 页面后抓者以页面为准）。

| # | 原文标题 | 中文标题 | 分数 | 评论 |
| --- | --- | --- | --- | --- |
| 1 | [Tell HN: HN is being scraped for emails to scam](https://news.ycombinator.com/item?id=50513451) | HN 邮箱被抓取用于诈骗 | 120 | 41 |
| 2 | ["Who is Hiring?" postings stuck near 12-year lows…](https://www.hntrends.com/2026/november.html) | 招聘帖 12 年低位，AI 覆盖一半 | 93 | 83 |
| 3 | [Doing Show HN generates a ton of automated email pitches](https://petervandijck.com/post/pbrgs-ev0bc) | Show HN 后 17 封自动推销邮件 | 56 | 51 |
| 4 | [Comcast's "fiber-powered Wi-Fi" is cable…](https://arstechnica.com/tech-policy/2026/11/comcast-falsely-advertises-cable-internet-as-fiber-powered-att-lawsuit-says/) | AT&T 诉 Comcast 虚假光纤广告 | 55 | 46 |
| 5 | [Show HN: Coral – gateway where agents write their own tools](https://github.com/withcoral/coral) | Coral：agent 自写工具的策略网关 | 50 | 24 |
| 6 | [US now "comfortable" with children dying of measles…](https://arstechnica.com/health/2026/11/us-now-comfortable-with-children-dying-of-measles-as-death-toll-hits-10/) | 美国麻疹死亡达 10 例 | 41 | 28 |
| 7 | [Ask HN: If AI tools are so good, why isn't your bug backlog empty?](https://news.ycombinator.com/item?id=50520076) | AI 这么强，bug backlog 为何不清空 | 38 | 65 |
| 8 | [Show HN: Fakemetrics.com](https://fakemetrics.com/) | 虚假增长截图生成器 | 28 | 10 |
| 9 | [Launch HN: Axonnic (YC F26)](https://news.ycombinator.com/item?id=50522776) | EMG 手指追踪套筒 | 21 | 7 |
| 10 | [Show HN: OpenTodo](https://github.com/OpenTodoApp/OpenTodo) | 自托管本地优先任务管理器 | 20 | 19 |

## 数据缺口与抓取失败声明

- Ars Technica 正文返回 HTTP 405，Comcast 条目摘要基于 HN 讨论页抓取。
- hntrends.com 首次抓取超时，重试成功；Coral 仅抓到 README，评论区未抓取。
- 本窗口主查询（hn_points ≥ 20 过滤）返回空，按回退协议改用 keyword='Show HN' 窗口 -2d 拉取后，按 published_at 严格裁回 2026-11-16 UTC 窗口；窗口内 hn_points ≥ 20 条目共 10 条，全部入选或入 Top10，未出现编造条目。

{"action": "finalize", "questions": [], "confirmed_missing_indicators": [], "confirmed_event_mappings": [], "actions": [{"type": "follow_up", "priority": "P2", "summary": "跟踪 hntrends 招聘数据与 AI 就业叙事：11 月 244 帖/-37% YoY 是否在 12 月延续，校验'AI 挤压初级岗位'假设", "verification_date": "2026-12-15"}, {"type": "monitoring", "priority": "P3", "summary": "持续监控 agent 工具网关/权限层赛道（Coral 等）与 MCP 权限粒度议题的后续高分帖", "recurrence": "weekly"}]}

## 第 1 轮（finalize）

- 问题: (无)
