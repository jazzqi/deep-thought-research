# reference.md — HN 书摘 2026-08-28（UTC 窗口）数据溯源

## 取数说明（数据质量）
- query_raw_items(source='hackernews', limit=50) 查询层 source 过滤持续失效（第 3+ 次确认，2026-08-29 复验）：仅返回 9 条，且混入 longbridge 财经条目（id:146460/145875/114342/114340），真实 HN 帖漏检。本刊真实榜单改以 Algolia HN API 为准。
- 真实 HN 取数窗口：created_at_i ∈ [1787875200, 1787961600) = 2026-08-28 00:00:00Z → 2026-08-29 00:00:00Z（前一日 UTC 窗口）。

## 数据点溯源
- HN 2026-08-28 UTC 窗口 Top 故事与分数/评论: fetch_url(hn.algolia.com/api/v1/search?tags=story&numericFilters=created_at_i>=1787875200,created_at_i<=1787961600&hitsPerPage=200) = GUIs keyboard-driven ▲755💬380 / Get your Windows license refund ▲679💬281 / GLM-5.3 open-weight ▲677💬226 / "It works better in the app" ▲650💬443 / Htmx 4.0 ▲631💬155 / Anthropic blacklist ruled illegal(NYT) ▲570💬413 / U.S. sanctions A/I Collective ▲566💬555 / Inception curved map ▲485💬159 / Luanti DMCA takedown ▲484💬145 / Pentagon Anthropic unlawful(Reuters) ▲324💬3 / rumour-of-bug exploit ▲302💬105 / Virtual iPhone ▲236💬69 / AI slop CV ▲211💬141 / LLM memory program analysis ▲112💬21
- HN 评论树(GLM-5.3 帖 id:49479878): fetch_url(hn.algolia.com/api/v1/items/49479878) = petu 评论(id:49481588) 确认 FP8 设为默认、路由专家层转 FP8、下载体积约减半
- HN 评论树(Anthropic 帖 id:49473522): fetch_url(hn.algolia.com/api/v1/items/49473522) = 顶层高赞评论偏向制造业/劳动力成本与中美制造对比，未直接评裁决法律意义
- HN 评论树(GUIs keyboard 帖 id:49479837): fetch_url(hn.algolia.com/api/v1/items/49479837) = Arainach/BeetleB 等关于 Web/Electron vs 原生 UI、键盘导航与无障碍
- HN 评论树(AI slop CV 帖 id:49474143): fetch_url(hn.algolia.com/api/v1/items/49474143) = 维护者关于低价值 PR 甄别与「以意图拒合法贡献」分歧
- 正文抓取成功: fetch_url(en.refund4freedom.org/) / fetch_url(shkspr.mobi/blog/2026/08/it-works-better-in-the-app/) / fetch_url(four.htmx.org/announcements/2026-08-28-htmx-4.0.0-is-released) / fetch_url(blog.luanti.org/2026/08/27/luanti-dmca-tracer-ai/) / fetch_url(github.com/Lakr233/vphone-cli) / fetch_url(neilalexander.dev/2026/06/30/flooding-contributions) / fetch_url(www.inventati.org/)
- 正文抓取失败(超时/无正文，摘要基于 Algolia 元数据+评论): z.ai/blog/glm-5.3（无正文）、ckardaris.com/blog/2026/08/28/keyboard-driven-guis.html（连接超时）、reuters.com Anthropic 裁决（401）、nytimes.com Anthropic 裁决（受限）
- 市场背景(仅作 Big Picture 旁证，非 HN 帖): query_raw_items 泄漏 longbridge 条目 id:190121(2026-08-28 NVIDIA 跌超 4%、费城半导体跌超 3%) / id:190810(Marvell 财报后 -10%、NVIDIA -4%) / id:190112(Marvell 跌至 $217.54)

# reference.md — hn-daily 2026-08-29（覆盖 2026-08-28 UTC 窗口）

- 取数方法: query_raw_items(source='hackernews') 查询层 source 过滤失效（第3次确认，2026-08-29 07:45 复验），返回 9 条中含 4 条 longbridge 财经泄漏（id:146460/145875/114342/114340）；真实 HN 帖以 keyword 检索补位还原。
- Anthropic 五角大楼案胜诉: query_raw_items(keyword=Anthropic)[id:190642] = IBTimes 报道；fetch_url(https://www.ibtimes.com/anthropic-just-beat-pentagon-court-judge-said-national-security-was-used-punish-its-ai-rules-3806895) 正文 = 法官 Rita Lin 裁定封杀违法、违反第一/第五修正案、政府预计上诉。
- MHS 物理世界接口: query_raw_items(keyword=Anthropic)[id:178106] = Ars Technica 报道；fetch_url(https://www.theregister.com/ai-and-ml/2026/08/28/anthropic-proposes-plumbing-spec-to-link-ai-agents-to-lab-kit-and-robots/5293135) 正文 = MHS 用 read/write 原语、HHMI Janelia 实测、集成数周→数小时。
- AAR 自改进对齐: query_raw_items(keyword=Anthropic)[id:190074] = TechCrunch 报道；fetch_url(https://techcrunch.com/2026/08/28/an-anthropic-researcher-just-gave-us-a-peek-at-self-improving-ai/) 正文 = 最强 AAR 6 小时超人类、$4/小时 vs $150/小时。
- AAR 论文: query_raw_items(keyword=Anthropic)[id:189006] = alignment.anthropic.com 论文；fetch_url(https://alignment.anthropic.com/2026/automated-alignment-researchers/) 正文 = 10 类对齐失败、泛化到 4.7× 更大模型、28 名人类研究员不及。
- MatX 70 亿收购: query_raw_items(keyword=Anthropic)[id:178113] = The Star/Reuters 报道；fetch_url(https://www.thestar.com.my/tech/tech-news/2026/08/28/exclusive-anthropic-planned-then-abandoned-7-billion-purchase-of-matx-sources-say) 正文 = 拟 $7B 收购、现转合作、MatX 估值 $4B、IPO 传 $2T 锚定 2028 营收 $200B。
- prmpt.cash: query_raw_items(keyword=Anthropic)[id:189922] = Show HN；fetch_url(https://prmpt.cash/) 正文 = stop hook 打印广告行、70% 分成、Base/Solana 结算。
- SF 专栏: query_raw_items(keyword=Anthropic)[id:186252] = SFGate 专栏（正文 fetch 失败，仅标题可证）。
- 分数快照: 各帖 hn_points 取自 query_raw_items metadata（入库快照）；190642 实时 HN 页 07:58 已升至 16，说明窗口尾部帖仍在爬分。
- 技术雷达补充帖（08-29 凌晨，超出严格窗口）: id:191185 Tokensift、id:190964 TurboKV、id:191201 Kaspersky 零日，均 source=hackernews。
