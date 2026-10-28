# 数据溯源 · 2026-10-28 增量补丁

- 基线窗口 HN≥20 分全量: query_raw_items(source=hackernews, min_points=20, published_after=2026-10-27T00:00:00Z, published_before=2026-10-28T00:00:00Z, limit=80) = 64 条（基线正文 14 条已覆盖高分段）
- 增量窗口（22:51 快照后）hackernews 新条目: query_raw_items(source=hackernews, min_points=1, published_after=2026-10-27T22:51:30Z, published_before=2026-10-29T00:00:00Z) = NO_DATA（无入库，已按回退序列确认）
- 快照边缘新增帖: query_raw_items(source=hackernews, min_points=20, published_after=2026-10-27T22:00:00Z, published_before=2026-10-29T00:00:00Z)[id:575372] = ▲27 💬31 作者 tsxng「Reviewers rarely talk about reliability. Owners bring it up twice as often」2026-10-27 22:31 UTC 发布，基线 22:51:30 快照未收录
- id:575372 正文: fetch_url(https://www.bettascore.ai/research/reliability-reviewers-vs-owners) = 14 品类 6,900 条 YouTube 评测意见 vs 3,567 条 Reddit 车主意见；可靠性提及率 7.8% vs 17.0%（13/14 品类车主更高）；App/联网负面率 21% vs 71%；自清洁猫砂盆 39% vs 3%，扫地机 18% vs 1%；Glowforge Pro 可靠性/支持 2 正 7 负垫底，Eufy FamiLock S3 固件变砖 0 正 7 负垫底 20 款
- id:575372 评论: fetch_url(https://hn.algolia.com/api/v1/items/50266780) = 作者 tsxng 参与回应「评测者通常只拿到机器几周」；作者 anigbrowl 主张长周期可靠性应查 Consumer Reports
- 基线未收录当日最高分帖: query_raw_items(source=hackernews, min_points=20, published_after=2026-10-27T00:00:00Z, published_before=2026-10-28T00:00:00Z)[id:567818] = ▲674 💬238 WIRED「The US Government Is Hiding Secret Court Ruling About How It Spies on Americans」2026-10-27 14:06 UTC
- id:567818 正文: fetch_url(https://www.wired.com/story/the-us-government-is-hiding-a-secret-court-ruling-about-how-it-spies-on-americans/) = Wyden/Schiff 指政府逾期（180 天窗口 9/13 已过）未公开 FISA 法院对 702 搜索过滤器的裁决；Demand Progress 等 23 团体致信国会拒绝续期；11/6 为参议员设定的答复期限
- Show HN 回退（窗口-2d）: query_raw_items(source=hackernews, keyword='Show HN', min_points=1, published_after=2026-10-26T00:00:00Z, published_before=2026-10-29T00:00:00Z, limit=30) = 30 条，最新 2026-10-27 18:08，无基线外新增高价值条目
- 全源兜底（10-28 窗口）: query_raw_items(published_after=2026-10-28T00:00:00Z, published_before=2026-10-29T00:00:00Z, limit=50) = 50 条全部为 longbridge 财经快讯，hackernews 源 0 条
- 基线快照时间戳: themes/hn-daily/2026-10-28.md 数据速览 = 2026-10-27T22:51:30.292952+00:00

- Genie 4 发布详情（Gemini Omni 锚定、实时交互、研究预览范围）: fetch_url(deepmind.google/blog/genie-4...) = 实时交互世界模型+原生音频
- Genie 4 HN 评论（物体恒存性缺陷讨论）: fetch_url(news.ycombinator.com/item?id=50261319) = 696 points/421 comments
- Python JIT 移除（PEP 836 撤回、SC 要求、时间线）: fetch_url(lwn.net/SubscriberLink/1102102...) = JIT 开发终止
- Python JIT HN 评论（cogman10 vs stickfigure PEP/JEP 流程之争）: fetch_url(news.ycombinator.com/item?id=50257419) = 435 points/232 comments
- AI promised less work GitHub 贡献数据: fetch_url(oioannou.com/blog/ai-promised-less-work/) = 2026年至10/27达2102次贡献，8月427次为历史峰值
- Mythical Man-Month in the age of AI 核心论点: fetch_url(j11g.com/the-mythical-man-month-in-the-age-of-ai) = Brooks定律变形版
- Software may be getting worse 历史论证: fetch_url(bitlog.com/2026/10/27/...) = Windows时代质量地板来自物理介质发行
- Anthropic 反馈数据用于训练: fetch_url(privacy.claude.com/en/articles/7996868...) = 反馈附文本可入训练
- Roblox 爬取 145.5GB 创作者模型: fetch_url(open3dlab.com/news/roblox-downloaded-145-gb...) = User-Agent trellis2-data-sourcing/1.0，34小时26429请求
- LFM3 架构与规格: fetch_url(liquid.ai/blog/lfm3) = 1.7B骨干6模态，22T tokens，4bit约1GB
- blaze 增量 Rust 构建: fetch_url(github.com/indexable-inc/blaze) = ripgrep 508ms→56ms，live edit约20ms
- abliterated DeepSeek 多供应商路由: fetch_url(allmodels.io/llm/abliterated) = 5家推理供应商
- Ghostty 1.4.0 发布与安全通告: fetch_url(ghostty.org/docs/install/release-notes/1-4-0) = 172贡献者/2889提交/10个GHSA
- HN 条目路由与热度快照: query_raw_items(source=hackernews, published_after=2026-10-21) = 今日全量候选池

- HN 2026-10-27 UTC 窗口高分帖清单（60 条 ▲≥20）: query_raw_items(source='hackernews', published_after='2026-10-27T00:00:00Z', published_before='2026-10-28T00:00:00Z', min_points=20, limit=60) = 榜首 WIRED 秘密监控法庭裁决 [id:567818] ▲674，AI promised less work [id:565523] ▲600/💬570，Roblox 145GB [id:564951] ▲425，Python JIT 移除 [id:565365] ▲369，Genie 4 [id:570730] ▲180
- 第 3 条正文（AI 生产力复盘）: query_raw_items(window 10-27)[id:565523] = oioannou.com 亲历博客，2026 年 GitHub 贡献 2,102 次超 2021-2025 任何一年
- 第 3 条评论: fetch_url(https://news.ycombinator.com/item?id=50257325) = keiferski：80% 旧质量/1% 时间的必做任务不可拒绝；snarfy：铝→垃圾类比一行代码成本
- 第 4 条评论: fetch_url(https://news.ycombinator.com/item?id=50255298) = freefaler：好坏分化放大；joshAg：约 10 名程序员用 LLM 代码后掉 0.5-3 晋升档，主导工程师忘自家日期库规范
- 第 5 条评论: fetch_url(https://news.ycombinator.com/item?id=50257548) = i_c_b（前 AAA 开发者）：硬件约束混杂变量、成本膨胀倒逼商业模式优先设计
- 第 6 条评论: fetch_url(https://news.ycombinator.com/item?id=50259406) = dovetailed：Claude Code 会话质量问卷 Dismiss 仅记评分，点赞/点踩+文字反馈为另一通道连同对话提交；avd201：零数据留存是企业版付费项
- 第 7 条评论: fetch_url(https://news.ycombinator.com/item?id=50256985) = superdisk 指向 github.com/roblox/cube（Roblox 开源 3D 生成基础模型）；embedding-shape：text-to-3D 布线质量未达游戏引擎可用
- 第 11 条 libghostty 要点: fetch_url(https://news.ycombinator.com/item?id=50261998) = mitchellh 自述：CI 覆盖 9 平台含裸机、空终端内存 -90%、4 核 8GB 跑 10,000 活跃终端、JetBrains 1,250 万活跃用户、Neovim 核心替换 PR #39773、libghostty 1.0 + ABI 稳定数月内 [id:572035]
- 第 12 条正文（此前未能抓取，本轮补抓成功）: fetch_url(https://fishbowl.pastiche.org/2026/10/26/ai-skills) = Charles Miller 10-26 文，i++/++i folklore 类比、prompt engineering 套路将被产品吸收为默认、Steven Bradbury 跟跑策略
- 第 12 条评论: fetch_url(https://news.ycombinator.com/item?id=50255346) = joshstrange：LLM 熟练度是技能光谱；Leynos：AI 技能全是老技能（学习/表达/假设检验/委派/定义 done）
- JetBrains 终端改用 libghostty: query_raw_items(window 10-27)[id:571283] = blog.jetbrains.com 官宣，与 Ghostty 1.4.0 同日


- 第 8 条 LFM3 路由与热度: query_raw_items(keyword='LFM3', source=hackernews, window 10-27)[id:572318] = ▲40 💬12，HN 50262229 采集时已涨至 117 分/44 评论
- 第 8 条评论: fetch_url(https://news.ycombinator.com/item?id=50262229) = samstevens（Liquid AI 发布团队）：d1-2B 决策模型 1GB 统一内存可跑校准分类、100+ 标注样本+GPU 可单步微调 LFM3-Audio-2B；colingauvin：LFM2.6 标注仅约 40% 数据点可信、待 LFM3 上 LocalAI；Powdering7082 发现无系统提示时 reasoning trace 仍渗入"必须使用工具"指令，samstevens 确认大量 tool-use RL
- 第 9 条 blaze 路由与热度: query_raw_items(keyword='blaze', source=hackernews, window 10-27)[id:555701] = ▲29 💬6，HN 50254300 帖已被 [flagged]
- 第 9 条评论（fact-check）: fetch_url(https://news.ycombinator.com/item?id=50254300) = anonymous908213 指控抄袭 rustd（Claude 改名洗稿、二次投稿疑似买号，前帖 50168220）；octoberfranklin：borrow checker 0.1.0 无、main 仅覆盖约 2/3 rustc 借用错误、首提交距今 7 天、单一贡献者；wumms：25 项基准中位 19x/最小 3.7x/最大 83x（"92x"为 up-to 口径）
- 第 10 条 abliterated 路由与热度: query_raw_items(keyword='abliterated', published_after=2026-10-20)[id:557372] = ▲90 💬117，HN 50254836 采集时 93 分/118 评论
- 第 10 条评论: fetch_url(https://news.ycombinator.com/item?id=50254836) = Aurornis：abliteration 不补训练集缺失信息且会以微妙方式劣化性能，不建议默认使用；Hizonner："more brain damage"无法修复脑损伤；reedf1：拒绝常发生在 thinking 阶段（改答相似问题），abliterated 对照可暴露 sandbagging；himata4113：glm5.2→deepseek 越狱链同样可达且保留原性能
- abliterated 安全风险前置研究: query_raw_items(keyword='abliterated', published_after=2026-10-20, min_points=1)[id:494225] = 2026-10-19 ProjectDiscovery「How abliterated models can get you pwned」▲249 💬137，去护栏模型自身更易被 prompt injection 攻破


## tech_scout 交叉审查（2026-10-28）独立核验来源

- 10-27 UTC 窗口 ▲≥20 全量（独立复核）: query_raw_items(source=hackernews, min_points=20, published_after=2026-10-27T00:00:00Z, published_before=2026-10-28T00:00:00Z, limit=100) = 65 条（稿中称 64 条、reference 另一行称 60 条，三处不一致）
- 窗口第 6 高分帖（稿中未覆盖）: query_raw_items(同上窗口)[id:565303] = ▲348 💬160 IEEE Spectrum「Wikipedia's Cleanup of AI-Generated Content」2026-10-27 11:08 UTC
- Debian 治理帖（稿中未覆盖）: query_raw_items(同上窗口)[id:564826] = ▲222 💬134 debian-devel「I will no longer upload to NEW」2026-10-27 09:59 UTC
- 安全簇（稿中未覆盖）: query_raw_items(同上窗口)[id:566813] = ▲176 💬57 Wiz「No successful PHP2Shell exploits seen so far; exposure down 67%」；[id:574969] = ▲72 Tailscale SSH investigation update（19:55 UTC，快照后沿）
- 生产力簇第四候选（稿中未覆盖）: query_raw_items(同上窗口)[id:567341] = ▲131 💬69「Here Be Monsters: What Do You Still Need to Know When Agents Do the Work?」
- Show HN 兜底（独立复核）: query_raw_items(source=hackernews, keyword='Show HN', window 10-27, limit=30) = 窗口内无被漏掉的高价值 Show HN（TitleArt▲395 等属 10-26 窗口）
- "AI 生产力怀疑论三帖 ▲45"指代核实: query_raw_items(同上窗口)[id:564053] = ▲45「AI Skills are worthless in 2026」（即稿中第 12 条；同窗口另有 3 条 ▲45 帖，指代存在歧义）
- 10-20 Meta torrent 诉讼事实核验: query_raw_items(keyword='torrent OR piracy', published_after=2026-10-15)[id:500372] = 2026-10-21 solidot「Meta 被勒令公布授权通过 BT 下载盗版电子书的员工名单」（事实成立，但稿/原 reference 均未挂此溯源行）
