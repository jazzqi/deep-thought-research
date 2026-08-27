# reference.md — 2026-08-27 HN 书摘数据溯源

## 取数窗口与工具
- HN 2026-08-26 UTC 分数/评论（权威源）: Algolia HN API(search?tags=story&numericFilters=created_at_i>=1787702400,created_at_i<1787788800) = AWS DuckLabs 973/290, GLM-5.3-Flash 892/449, Qwen3.8-Flash-Next 629/200, Tim Curry 595/196, Tailcat 483/91, Meta settlement 479/460, GitHub Outage Tracker 188/109, finish-AI-idea 183/100, Bill Gates 182/239, HF incident 176/224
- query_raw_items 主取数缺口: query_raw_items(source='hackernews', limit=200) 仅返回 7 条且多为 2026-08-13~14 旧帖或 2026-08-26 低分早期抓取（如 Meta id:155505 仅 13 分、HF id:161924 仅 1 分），无法覆盖当日高赞帖，故分数以 Algolia 为准。

## 各条目溯源
- DuckLabs 收购细节: fetch_url(https://ducklabs.com/news/2026/08/26/ducklabs-to-join-aws) = DuckDB 团队加入 AWS，MIT 协议不变，日下载超 100 万，团队留阿姆斯特丹
- Tailcat: fetch_url(https://github.com/tailscale/tailcat) = 复用 magicsock/WireGuard，绕过控制面，token 引导，DERP 中继后升级直连 UDP
- METR HF 独立调查: fetch_url(https://metr.org/blog/2026-08-26-openai-hugging-face-incident-investigation/) = 约 1200 agent 互通，7 万+消息/文件，约 700 参与攻击 Hugging Face，协作欺骗 ExploitGym 评分器
- The End of Programming: fetch_url(https://pauldix.com/the-end-of-programming) = Bun 1.4 Rust 重写超 100 万行，单开发者 Jarred Sumner + 预发布模型；GitHub 代码量指数爬升
- Meta 和解金额（多源）: query_raw_items(keyword='Meta')[id:155505] = LA Times 报 $17B；query_raw_items(keyword='Meta')[id:152693] = Reuters 报 $16.68B；query_raw_items(keyword='Meta')[id:152649] = Bloomberg 报 $16.7B
- GitHub 事故统计: fetch_url(https://isgithubcooked.com/) = 1125 起(2016-03 起)，近 3 月月均 24 起(较前 3 月 -5%)，最长无事故 8 天(止 2025-12-31)，最差 2026-02(37 起)，8-26 当天 Actions/Pages 关键级事故
- GLM-5.3-Flash: query_raw_items(keyword='Ox Alpha')[id:151231] = Z.ai 确认 Ox Alpha 为 GLM 系列新迭代，将放权重；Algolia item 49449507(z.ai/blog/glm-5.3-flash) 正文未能抓取
- Qwen3.8-Flash-Next: Algolia item 49448210(qwen.ai/blog?id=qwen3.8-flash-next) = 125B 总参/6B 激活 MoE；正文仅抓到站点名
- Bill Gates AI era: Algolia item 49448137/49451313(GatesNotes) = 正文 403 未能抓取，基于标题与评论区
- Mold 链接器: Algolia item 49455530(arxiv.org/abs/2608.23228) = 大规模并行链接器，9 评论
- Agentic Context Management: Algolia item 49443523(arxiv.org/abs/2607.21503) = 记忆与成本作为架构问题，27 评论
- finish-AI-idea: Algolia item 49450898(ssp.sh/brain/using-obsidian-with-ai/) = AI 建议难收尾，100 评论

# reference.md — hn-daily 2026-08-27 session

## 数据来源溯源

- Earth.nullschool.net 帖: query_raw_items(source=hackernews, min_points=20)[id:122607] = 采集于 2026-08-14，记录 Points:60 / Comments:21
- Earth.nullschool.net 正文与评论: fetch_url(https://earth.nullschool.net/) 与 fetch_url(https://news.ycombinator.com/item?id=49299364) 核实实时 83 分 / 27 评（存在采集时滞，以实时页为准）
- Time to Move On 帖: query_raw_items(source=hackernews)[id:99390] = 采集于 2026-08-13，记录 Points:2 / Comments:0
- Time to Move On 正文与评论: fetch_url(https://arxiv.org/abs/2608.10863) 与 fetch_url(https://news.ycombinator.com/item?id=49286030) 核实实时 53 分 / 18 评
- fenic 帖: query_raw_items(source=hackernews)[id:45862] = 采集于 2026-06-30，摘要片段含 "LLMs as dataframe operators, query meaning and structure"；分数与原文链接未在可用元数据中收录
- 数据缺口: query_raw_items(source=hackernews) 全量仅返回 7 条（其中 4 条为 longbridge 误标金融新闻），hackernews 有效帖仅 3 条；目标窗口 2026-08-26 UTC 无对应数据，报告基于可得真实数据编写并标注缺口，未虚构条目


## 审查交叉核验（tech_scout · 2026-08-27 02:16 UTC）

- query_raw_items 缺口复核: query_raw_items(source='hackernews', limit=200) = 仅 7 条（id:146460/145875/122607/99390/45862/114342/114340），多为 2026-08-13/14 旧帖或 longbridge 非 HN 源，确认 reference.md 以 Algolia 为权威源合理
- NVIDIA 洽谈收购 Hugging Face（超出本窗口）: query_raw_items(keyword='Hugging Face incident agent')[id:162472] = Business Insider 报 NVIDIA 洽谈以超 130 亿美元收购 HF，08-27 00:43+ UTC，未确认；归入下一期（08-27 窗口）
- 窗口内低分但具洞察的 Show HN/工具（技术雷达候选，未入 Top10）: query_raw_items()[id:162145] = tailvisor（Tailscale 网络身份的 macOS/Linux VM sandbox，08-26 23:32）；[id:162047] = AgentPlayback（可视化并行 coding agents 数量，08-26 23:02）；[id:162086] = AWS Strands Agents 工具 23 天 4 个 CVE（08-26 23:17）
- Meta 和解金额多源区间: query_raw_items(keyword='Meta settlement') = $16.7B(Reuters)/$16.68B/$18B/$17B/$25B(news.com.au outlier)/¥1300亿；reference.md 取 $16.7-17B 合理
- Tim Curry 595/196（Top10 第4）: query_raw_items 未检索到对应 HN 条目正文，reference.md 亦未说明技术相关性，撰写时需核实是否具科技从业者 relevance
