# 数据来源溯源（2026-10-27 期）

- HN 榜单 50 条（2026-10-26 UTC 窗口，hn_points>=20）: query_raw_items(source='hackernews', min_points=20, published_after='2026-10-26T00:00:00Z', published_before='2026-10-27T00:00:00Z', limit=50) = 50 条
- Anthropic S-1 榜单热度/元数据: query_raw_items(same window)[id:546052] = ▲1262 · 💬1223 · 作者 SiNTEx
- Anthropic S-1 封面信息（PBC/Delaware/Dario Amodei/Daniela Amodei/548 Market Street）: fetch_url(SEC S-1 原文) = 已抓取
- S-1 评论摘录（wongarsu: Claude Fable 5 隐性降质争议）: fetch_url(https://hn.algolia.com/api/v1/items/50242939) = 已抓取
- ETH 论文榜单热度: query_raw_items(same window)[id:555118] = ▲147 · 💬62 · 作者 vok
- ETH 论文元数据（OpenAI Math Release, 2026-10-25）与评论分歧（eru: 运行时界过不了多项式归约）: fetch_url(github openai/math README + hn.algolia.com/api/v1/items/50251661) = 已抓取；PDF 正文未能解析
- 微软买断（6 万人/四分之一/部门参与清单/1900 亿 capex/1.5 万裁员）: fetch_url(seattletimes 文章) = 已抓取；榜单条目 [id:550474]（重复条目 [id:555000] 已合并去重）
- 微软买断评论摘录（pipes: 先接受第一个要约）: fetch_url(https://hn.algolia.com/api/v1/items/50245524) = 已抓取
- Raschka 课程（8 视频 11 小时/评测/inference scaling/RL/蒸馏）: fetch_url(magazine.sebastianraschka.com) = 已抓取；榜单条目 [id:550473]
- GPT-6.1 Terra: query_raw_items(same window)[id:553375] = ▲160 · 💬74；fetch_url(openai.com) 403 未能抓取正文
- IBM CEO 开放权重: query_raw_items(same window)[id:535868] = ▲402 · 💬301；fetch_url(theregister) 反爬拦截未能抓取正文
- Brown AI 数据劳工研究: query_raw_items(same window)[id:548338] = ▲170 · 💬157
- Cloudflare KV 缓存泄露（155 条响应/681,280 token/SGLang/Gadi Evron/9-8 报告 9-9 修复）: fetch_url(blog.cloudflare.com) = 已抓取；榜单条目 [id:555119]
- Cohere Qwen3.8 行为披露（诊断文件→北京存储容器/推理流称零工具）: fetch_url(cohere.com blog) = 已抓取；榜单条目 [id:552233]
- vLLM 工具调用准确率: query_raw_items(same window)[id:546869] = ▲132 · 💬64；fetch_url(ubicloud blog) 仅返回导航框架未能抓取正文
- Cognitive Mercantilism（Joyce Appleby/重商主义四信念/零和智能）: fetch_url(contraptions.venkateshrao.com) = 已抓取；榜单条目 [id:538842]
- 404 Media ChatGPT 客服转介（俄罗斯用户/俄语对话/邮箱代写邮件）: fetch_url(404media.co) = 已抓取；榜单条目 [id:553372]
- Top10 快照分数/评论数: query_raw_items(same window) 各条目 [id:535526][id:544505][id:551589][id:536008][id:553374][id:545844] = 见 draft 数据速览表
- 跨天去重基线: ReadThemeDocsTool(themes/hn-daily/2026-10-26.md) = 10-26 期覆盖 10-25 窗口，本窗口条目均为新增


## 第三棒（tech_generalist，2026-10-27 00:44 UTC）增量来源

- 10-26 美股收盘复核（QQQ/NVDA/MSFT）: market_quote(symbols=['QQQ.US','NVDA.US','MSFT.US']) = QQQ 712.20 +1.11%；NVDA 216.00 +2.39%；MSFT 532.60 +1.54%（15 分钟延迟报价，收盘后即终值；佐证 SOX/Nasdaq 涨幅口径方向一致）
- NVIDIA 拟对 AI 基础设施上运行 agent 按 GPU 收 $2,000/年软件费: query_raw_items(source=hackernews, keyword='Anthropic IPO OR S-1 OR NVIDIA agent fee OR ETH', min_points=20, 2026-10-26 窗口)[id:554818] = Tom's Hardware 披露该费率尚在讨论中，HN ▲23/💬14，早期信号
- Anthropic S-1 官方公告交叉验证: query_raw_items(...)[id:550471] = anthropic.com/news/s1-sec，▲24/💬1
- OpenAI/Anthropic 数月内降价至多 80% 分析文: query_raw_items(...)[id:535304] = minimaxir.com，▲402/💬407（tech_scout 论据二引用）
- S-1 承诺年化口径复核（算术核对，非新增数据源）: 对 [id:546052] 评论区所列七家承诺求和 = 1612+1205+1145+1100+449+446+413 = 6370 亿美元总额；"每年 637 亿"= 总额÷10 粗摊；按合同期加权年化：Broadcom≈269（2026-31）、SpaceX≈301（2026-29）、Google≈143（2026-33）、Amazon≈100（2026-36），头部四家合计≈813 亿美元/年
- 收入口径矛盾存疑记录: [id:546052] 评论区 Maxatar 推算年收入≈672 亿美元 vs 作者 trjordan 设问"$50b→$500b"（≈500 亿起算），两口径相差约 13 倍，招股书财务页未能直接核验，报告中并列存疑



## 审查人（tech_scout，2026-10-27 00:53 UTC）独立核验增量来源

- 10-26 UTC 窗口独立榜单核验（审查基线）: query_raw_items(source='hackernews', min_points=40, published_after='2026-10-26T00:00:00Z', published_before='2026-10-27T00:00:00Z', limit=60) = 48 条，头部排序与稿内引用一致（Anthropic S-1 ▲1262 居首）
- Economist《If AI displaces human workers…》条目核验（#13，稿内"77 条评论"属实）: query_raw_items(keyword='displaces OR economist', 2026-10-20→10-27)[id:536903] = ▲37 · 💬77 · 作者 andsoitis
- NVIDIA $2,000/GPU/年 agent 软件费条目核验（稿内 [id:554818] 引用真实存在）: query_raw_items(keyword='Nvidia agent', min_points=20, 2026-10-25→10-27)[id:554818] = Tom's Hardware，▲23 · 💬14，标题确认"discusses $2k-per-GPU annual fee"
- 审查发现的漏项证据 PaperPilot（纯 Rust 零云 PDF 引擎，WASM+MCP）: query_raw_items(same window)[id:536876] = ▲219 · 💬77 · 作者 vardhan1237
- 审查发现的漏项证据 OpenAI math《The Exponential Time Hypothesis Is False》: query_raw_items(same window)[id:555118] = ▲147 · 💬62 · 作者 vok（稿件仅在共识5一句带过，无独立条目）
- 审查附带证据 Pharo 14 发布: query_raw_items(same window)[id:548378] = ▲222 · 💬55；C++26 contracts 投票 [id:543649] = ▲57 · 💬96
- Show HN 窗口扫描（审查重点①）: query_raw_items(keyword='Show HN', 2026-10-25→10-27, limit=30) = 30 条，当日最高为 TitleArt [id:536008]（▲365，稿内已提及），其余均 ≤▲177 低热项，无遗漏级信号
- news/company 交叉核验尝试: query_longbridge_by_route(path='news/company', symbol='MSFT.US') = 失败（longbridge 限流 429002，约 3.2 小时后恢复）——本审查以 HN 窗口独立扫描替代覆盖核验，窗口内重大事件（S-1/微软买断/Lula）稿件均已覆盖
