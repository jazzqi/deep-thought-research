# 数据来源溯源 · 2026-10-28 期（覆盖 2026-10-27 UTC 窗口）

- 当日 HN 高分帖全量（hn_points≥20，60 条）: query_raw_items(source=hackernews, min_points=20, published_after=2026-10-27T00:00Z, published_before=2026-10-28T00:00Z) = 60 条候选
- 头条1 AI promised less work: query_raw_items(source=hackernews)[id:565523] = ▲600/💬570，作者 oorestisime；正文经 fetch_url(https://oioannou.com/blog/ai-promised-less-work/) 抓取（GitHub 贡献数据 2020:2711 / 2021:1839 / 2022:1498 / 2023:1189；Principal 月均114 vs Full Stack 月均173；2025-12 月贡献50为入职以来最低）
- 头条1 评论: fetch_url(https://hn.algolia.com/api/v1/items/50257325) = 作者 bunderbunder 评论 id 50259535（agentic coding 破坏优先级能力）
- 头条2 Roblox 抓取 145GB: query_raw_items[id:564951] = ▲425/💬243；正文 fetch_url(open3dlab.com 公告) = 爬虫 UA trellis2-data-sourcing/1.0、AWS 单节点、34 小时 26,429 请求、读取 18,926 项目页、下载 1,027 文件/712 项目/145.5GB，其中成人内容 712 项目中 345 个（62.6GB）、423 个项目仅限非商用许可、违反 robots.txt 与 ToS
- Genie 4: query_raw_items[id:570730] = ▲180/💬87；正文 fetch_url(deepmind.google/blog/genie-4) = 原生多模态世界模型，Gemini Omni 锚定真实感，实时交互+原生音频，向 Google AI Ultra 订阅者与 Gemini API 早期伙伴推出研究预览
- Genie 4 评论: fetch_url(hn.algolia.com/api/v1/items/50261319) = 作者 causal 评论 id 50261480（游戏业整合 LLM 仍有灾难性边缘情况）
- Mythical Man-Month in the age of AI: query_raw_items[id:561816] = ▲418/💬296；正文 fetch_url(j11g.com) = Brooks 定律在 agent 时代的变异版："Adding agents to a project with unclear requirements gets you the wrong answer faster"
- FISA 702 秘密裁决: query_raw_items[id:567818] = ▲674/💬238；正文 fetch_url(wired.com) = Wyden/Schiff 指政府非法扣留 FISC 裁决，180 天公开窗口 9 月 13 日已过，要求 11 月 6 日前答复
- Wikipedia AI 清理: query_raw_items[id:565303] = ▲348/💬160；IEEE Spectrum 正文未能抓取（会员墙），摘要基于标题与项目页信息
- Apple M6: query_raw_items[id:565753](MBP,▲155/💬181) + [id:566811](iMac,▲275/💬326)；正文 fetch_url(apple.com newsroom) = M6 12核CPU/12核GPU，图形较 M5 快30%、AI 工作负载快25%，较 M1 最高 13x AI 性能，24 小时续航，Wi-Fi 7/蓝牙6
- Claude 反馈数据: query_raw_items[id:567817] = ▲207/💬91；正文 fetch_url(privacy.claude.com) = 商用产品默认不训练；显式点 thumbs 反馈则整段对话最多存 5 年、去标识化后可用于训练
- Python JIT 移除: query_raw_items[id:565365] = ▲369/💬194；正文 fetch_url(lwn.net) = 2024 年随 3.13 加入的实验性 JIT 走向移除，PEP 836（"JIT Go Brrr"）经数月讨论后被维护者撤回
- Debian NEW 队列 LLM 审查: query_raw_items[id:564826] = ▲222/💬134；正文 fetch_url(lists.debian.org) = 作者 josch 宣布不再向 NEW 上传，抗议 DFSG 团队未经公告将全部上传交 LLM 审查
- Abliterated DeepSeek: query_raw_items[id:557372] = ▲90/💬117；正文 fetch_url(allmodels.io) = 5 家推理提供商提供去拒绝（abliterated）DeepSeek V4.1 Flash 权重修改版
- AI Skills 无价值: query_raw_items[id:564053] = ▲45/💬22；正文 fetch_url(fishbowl.pastiche.org) = 作者 Charles Miller，"几周能会、几月就过期的技能没有时刻之外的价值"
- 软件变差但曾经更糟: query_raw_items[id:565305] = ▲255/💬233（Top10 快照引用，未深读）
- Trump 将禁止 "artificial intelligence" 用语: query_raw_items[id:574340] = ▲55/💬55（thehill.com 正文抓取 403 失败，仅快照）
- 跨期去重: 比对 themes/hn-daily/index.md 往期列表与 2026-10-27.md 全文，上一期覆盖 10-26 窗口（Anthropic S-1/GPT-6.1 Terra/微软买断等），本期 12 条与往期无标题重叠

- Genie 4 发布（世界模型，research preview 向 AI Ultra/API 早期伙伴）: query_raw_items(source=hackernews, published_after=2026-10-20)[id:570730] = DeepMind Genie 4 世界模型发布帖
- Genie 4 正文能力细节（原生多模态/Gemini Omni 锚定/实时语言改写场景）: fetch_url(https://deepmind.google/blog/genie-4-a-new-generation-of-world-simulation/) = 官方博客正文
- Genie 4 HN 604 分/374 评论（抓取时 2026-10-27 22:xx UTC）与物体恒存质疑评论: fetch_url(https://news.ycombinator.com/item?id=50261319) = HN 评论页
- AI promised less work 个人 GitHub 纵向数据（2026 年 2,102 次贡献/8月427次/零贡献工作日18天）: fetch_url(https://oioannou.com/blog/ai-promised-less-work/) = 正文
- AI promised less work HN 609 分/598 评论与评论摘录: fetch_url(https://news.ycombinator.com/item?id=50257325) = HN 评论页
- Anthropic 六家药企合作名单与 CAR-T 受体10倍数据: fetch_url(https://www.anthropic.com/research/early-progress-drug-development) = 官方研究正文 [id:575106]
- Amazon 裁撤 Nova 模型/Abbeel 领衔前沿方向/关闭旧金山80人AGI办公室: fetch_url(https://futurism.com/artificial-intelligence/amazon-ai-division-failure-nova) = 正文 [id:572514]
- Python 实验性 JIT 移除（PEP 836 撤回/2024 年 3.13 合入）: fetch_url(https://lwn.net/SubscriberLink/1102102/0c00e4d550f25f8c/) = LWN 正文 [id:565365]
- Anthropic 反馈数据政策（点赞反馈存5年可训练/默认商业产品不训练）: fetch_url(https://privacy.claude.com/en/articles/7996868-is-my-data-used-for-model-training) = 隐私中心正文 [id:567817]
- 特朗普禁用 AI 一词改称 SI（Truth Social/9月行政令）: fetch_url(https://thehill.com/homenews/administration/6175633-trump-bans-artificial-intelligence-term/) = The Hill 正文 [id:574340]
- Liquid AI LFM3 规格（22T token/六款2B模型/35%参数优势/4-bit 1GB/256K）: fetch_url(https://www.liquid.ai/blog/lfm3) = 官方博客正文 [id:572318]
- Survival LLM 规格（93万Wikipedia条目/按内存选型/22题盲测21对）: fetch_url(https://www.brangus.io/survival-llm) = 官方站点正文 [id:574968]
- abliterated DeepSeek 5 家推理商路由: fetch_url(https://allmodels.io/llm/abliterated) = AllModels 正文 [id:557372]
- Mythical Man-Month in the Age of AI 正文与 Brooks 定律 2026 版: fetch_url(https://j11g.com/the-mythical-man-month-in-the-age-of-ai) = 正文 [id:561816]
- MMM 评论摘录（AI 放大团队两极）: fetch_url(https://news.ycombinator.com/item?id=50255298) = HN 评论页
- AI Skills are worthless 正文与评论摘录: fetch_url(https://fishbowl.pastiche.org/2026/10/26/ai-skills) + fetch_url(https://news.ycombinator.com/item?id=50255346) [id:564053]

- Genie 4 HN 元数据（10-27 窗口当日最高分技术帖）: query_raw_items(source='hackernews',keyword='AI OR LLM OR model OR agent OR Genie OR open weights',min_points=20,published_after='2026-10-27T00:00:00Z',published_before='2026-10-28T00:00:00Z')[id:570730] = ▲180/💬87，Points 108/# Comments 43，deepmind.google Genie 4 博客
- AI promised less work HN 元数据: query_raw_items(...同上窗口)[id:565523] = ▲600/💬570，oioannou.com 博客，10-27 11:08 发布
- Wikipedia's Cleanup of AI-Generated Content HN 元数据: query_raw_items(...同上窗口)[id:565303] = ▲348/💬160，spectrum.ieee.org，10-27 11:08 发布；HN 评论页抓取时 421 points/189 comments: fetch_url(https://news.ycombinator.com/item?id=50257326) = 评论 Natsu"pre-LLM archives are the new low-background steel"
- Roblox 145GB 抓取事件 HN 元数据: query_raw_items(...同上窗口)[id:564951] = ▲425/💬243，open3dlab.com 公告；HN 评论页抓取时 448 points/266 comments: fetch_url(https://news.ycombinator.com/item?id=50256985) = 评论 xnickb/superdisk 指向 Roblox Cube
- Roblox 爬虫细节（145.5GB/712 项目/1,027 文件/423 项目仅非商业许可/trellis2-data-sourcing/1.0）: fetch_url(https://open3dlab.com/news/roblox-downloaded-145-gb-of-models-from-our-sites/) = Open3DLab 10-26 公告全文
- Amazon 砍 Nova HN 元数据: query_raw_items(...同上窗口)[id:572514] = ▲35/💬13，futurism.com（转引 Bloomberg）
- Liquid AI LFM3 HN 元数据: query_raw_items(...同上窗口)[id:572318] = ▲40/💬12，liquid.ai/blog/lfm3
- Survival LLM HN 元数据: query_raw_items(...同上窗口)[id:574968] = ▲50/💬29，brangus.io
- abliterated DeepSeek 路由 HN 元数据: query_raw_items(...同上窗口)[id:557372] = ▲90/💬117，allmodels.io/llm/abliterated
- CFSG Lean 形式化 HN 元数据: query_raw_items(...同上窗口)[id:571655] = ▲49/💬17，cfsg.axiommath.ai；规模数据（43.1M 行 Lean/2.05M 声明/715 篇文献）: fetch_url(https://cfsg.axiommath.ai/) = 项目页面
- Alphabet 估值: query_longbridge_by_route('fundamental/valuation/pe',{'symbol':'GOOGL.US'}) = PE current 17.45 / median 27.84 / high 30.45 / low 17.45（2026-10-27 查询）
- Amazon 估值: query_longbridge_by_route('fundamental/valuation/pe',{'symbol':'AMZN.US'}) = PE current 21.2 / median 29.3 / high 32.55 / low 21.2（2026-10-27 查询）
- Anthropic S-1（Big Picture 引用）: query_raw_items(source='hackernews',keyword='Anthropic S-1',published_after='2026-10-26T00:00:00Z')[id:546052] = ▲1673/💬1627，10-26 当日最热，Anthropic 提交 S-1 启动 IPO

- GOOGL/AMZN/MSFT/NVDA 实时报价: market_quote(symbols=['GOOGL.US','AMZN.US','MSFT.US','NVDA.US']) = GOOGL 320.58(+1.19%) / AMZN 253.10(+1.61%) / MSFT 531.33(-0.24%) / NVDA 217.94(+0.90%)（2026-10-27/28 查询）
- Alphabet 一致预期: query_longbridge_by_route('fundamental/consensus',{'symbol':'GOOGL.US'}) = Q4 2026E 营收 1427.2亿美元、EPS 3.34美元；Q1 2027E 营收 1378.8亿美元、EPS 3.42美元；Q2 2026 实际营收 1198.0亿美元 Beat、normalized EPS 2.85 Miss
- Amazon 一致预期: query_longbridge_by_route('fundamental/consensus',{'symbol':'AMZN.US'}) = Q3 2026E 营收 2022.4亿美元、EPS 1.96美元；Q4 2026E 营收 2443.1亿美元、EPS 2.45美元；Q2 2026 实际营收 2006.1亿美元 Beat
- 微软大规模买断（约 1/4 员工）: query_raw_items(source=hackernews, min_points=40)[id:550474] = ▲1032/💬1076，Seattle Times, 2026-10-26
- 美国宏观日历: query_calendar_events(country='US', importance='high', days=10, lookback_days=7) = 10-29 Q3 GDP 年化季环比初值（前值2.2/预期3.0）、11-6 10月非农（前值2.9万/失业率4.2%）、10-28 苹果发布会（首款触控 MacBook）、10-23 UMich 消费者信心 48.0（前值46.3）、10-22 初请 19.4万（预期20.0万）
- news/company 查询: query_longbridge_by_route('news/company',{'symbol':'GOOGL.US'}) = 429002 rate limit，本期公司新闻改用 HN raw_items 与既有抓取

## 审查人 tech_scout 独立核验（2026-10-27 22:48 UTC）

- 10-27 窗口当日 HN 高分帖独立复核（min_points=30，AI/LLM/agent 关键词）: query_raw_items(source='hackernews', keyword='AI OR LLM OR model OR agent OR open weights OR Show HN', min_points=30, published_after='2026-10-27T00:00:00Z', published_before='2026-10-28T12:00:00Z') = 确认稿件 14 条全部在库且可溯源
- Genie 4 HN 元数据独立复核: query_raw_items(keyword='Genie OR world model', published_after='2026-10-27T00:00:00Z')[id:570730] = ▲180/💬87（Points 108/# Comments 43，DB 快照），与稿件"604 分/374 评论"及 reference 双口径并存，需统一快照时间
- Stanford Daily Anthropic 盗版书籍训练（稿件未覆盖，审查发现）: query_raw_items(...同窗口)[id:570274] = ▲88/💬37，stanforddaily.com 10-27 15:28
- Cloudflare GLM-5.3 KV 缓存跨请求泄露（10-26 22:41 发布，窗口边界疑似两期均漏）: query_raw_items(...同窗口)[id:555119] = ▲176/💬71，blog.cloudflare.com
- 当日其余 AI infra/生态候选（未达雷达门槛，供参考）: query_raw_items(...同窗口) = Tailscale SSH 调查更新 [id:574969] ▲72/💬24；JetBrains IDE 换用 libghostty [id:571283] ▲24/💬5；Raspberry Pi Zero 3W 设备树曝光 [id:575146] ▲30/💬5；Intel 收购 Classiq 量子平台 [id:555014] ▲23（10-26 窗口）
- 10-26 窗口高分 AI infra 帖（疑似上期覆盖范围，供 Lead 核对去重）: query_raw_items(...同窗口) = Microsoft Type Server Protocol [id:554006] ▲264/💬174；Sebastian Raschka reasoning models 课程 [id:554007→id:550473] ▲812/💬107


- 勘误: 上行 Raschka 课程条目 id 以 [id:550473] 为准（审查人笔误，无 554007）
