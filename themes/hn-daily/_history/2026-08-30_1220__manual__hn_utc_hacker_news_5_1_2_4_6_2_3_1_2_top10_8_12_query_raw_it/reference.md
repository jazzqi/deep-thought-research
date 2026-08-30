# 数据来源溯源（hn-daily · 2026-08-29 UTC 窗口）

## ⚠️ 取数源说明（重要）
- query_raw_items(source='hackernews', min_points=20) 查询层 source 过滤持续失效（2026-08-30 第 5+ 次确认）：仅返回 9 条、最高 ▲3、混入 longbridge 财经条目（id:146460/145875/114342/114340），且完全漏检 2026-08-29 真实高价值 HN 帖。该工具不可作为本日 HN 取数源。
- 真实 HN 数据改由 hn.algolia.com 官方 API 取数（fetch_url）：search?tags=story&numericFilters=created_at_i>=1787961600,created_at_i<1788048000（=2026-08-29 00:00 → 2026-08-30 00:00 UTC）。

## HN 榜单（fetch_url 抓取 Algolia）
- HN 2026-08-29 Top 故事: fetch_url(hn.algolia.com/api/v1/search?tags=story&numericFilters=created_at_i>=1787961600,created_at_i<1788048000&hitsPerPage=100) = Cursor/OpenAI/SpaceX 805pts·493c; Debian AI 475pts·442c; Internet cesspit 405pts·272c; DHS snoop 355pts·62c; Iceland EU 326pts·428c; Good Culture 293pts·70c; GrapheneOS MTE 275pts·145c; Samsung PIM 251pts·96c; Hy4 229pts·137c; StemDeck 210pts·59c
- HN 2026-08-30 部分(00:00-04:33 UTC): fetch_url(同API, created_at_i>=1788048000,<1788134400) = Bug Blindness 127pts·49c; FreeCORE TrueNAS 53pts·28c; Algorithmic Rent-Pricing 22pts·10c

## 条目正文（fetch_url 抓取）
- OpenAI Cursor 公告: fetch_url(web.archive.org/web/2026/https://openai.com/index/our-decision-on-cursor-following-its-acquisition-by-spacex/) = 拟 2026-11-12 终止合同；理由为 SpaceX 可能违反 ToS、Musk 旗下公司历史违约、xAI 宣誓承认违规
- Debian GR: fetch_url(https://lwn.net/Articles/1091231/) = 选项5"Responsible Use of Generative AI"胜出；两反AI选项低于"None of the Above"
- Internet cesspit: fetch_url(https://www.stephendiehl.com/posts/internet_predatory_cesspit/) = 平台以掠夺为组织原则，消费即分销
- Samsung PIM: fetch_url(https://chipsandcheese.com/p/hot-chips-2026-samsungs-processing) = LPDDR5X-PIM 614GB/s 片内带宽，8芯片 9.6 INT8 TOPS
- Tencent Hy4: fetch_url(https://www.tencent.com/tencent-releases-and-open-sources-tencent-hy4-preview/) = 770B/49B 激活/1M ctx；盲评 2.99 超 GLM-5.3(2.92)/Kimi K3(2.94)；推理吞吐 +31.8%；API $0.834/$2.501 每百万 token
- DHS snoop: fetch_url(https://www.theguardian.com/us-news/2026/aug/29/trump-dhs-1509-summons-records-journalists-nonprofits) = 19 USC 1509 海关条款绕开司法调取记者 6 个月记录
- Good Culture: fetch_url(https://newsletter.eng-leadership.com/p/good-culture-is-the-biggest-productivity) = 文化是 AI 之外最大生产力杠杆，Conway 定律
- Ocean temp: fetch_url(https://www.latimes.com/environment/story/2026-08-26/highest-ever-ocean-temperature-measured-as-powerful-el-nino-forms) = 全球海表温 8/22 创纪录 70°F（Copernicus，1979 起日跟踪）
- StemDeck: fetch_url(https://github.com/stemdeckapp/stemdeck) = 免费本地开源分轨，6 stem，无账号无上传
- TurboKV: fetch_url(https://github.com/kingroryg/turbokv) = Rust 嵌入式 KV，184 star，AES Bloom filter
- GDPR 文: fetch_url(https://matduggan.com/you-know-gdpr-is-good-based-on-who-hates-it/) = 以"谁恨它"作为 GDPR 有效的度量
- vLLM v0.28.0: fetch_url(https://github.com/vllm-project/vllm/releases/tag/v0.28.0) = Kimi-K3/DeepSeek V4 优化，584 commits/270 contributors

## HN 评论（fetch_url 抓取评论页）
- Cursor 评论 rgbrenner: fetch_url(https://news.ycombinator.com/item?id=49486172) = Anthropic 已因类似 ToS 违规封禁 xAI
- Debian 评论 bfgeek: fetch_url(https://news.ycombinator.com/item?id=49489982) = AI patch 淹没 reviewer，项目关闭外部贡献
- DHS 评论 softwaredoug/hackyhacky: fetch_url(https://news.ycombinator.com/item?id=49492219) = 1509 传票可不被遵守，公司合规是商业决策
- Good Culture 评论 dirtbag__dad: fetch_url(https://news.ycombinator.com/item?id=49491568) = 小公司好文化=可预测性+市场价+认真 HR


## tech_scout 交叉审查核验（2026-08-30 04:36 UTC）

- 08-29窗口真实HN条目还原(tech_scout独立核验): query_raw_items(keyword='github OR Show HN OR MCP OR agent OR rust OR llm')[id:192237] = Show HN: Delete yourself from data brokers ▲4 💬4 (2026-08-29 23:02, 窗口内最高可验证分)
- 08-29窗口次高(可验证): query_raw_items()[id:192095] = weirdest agent logs AI safety ▲3; [id:192358] = Flock abuse police ▲3; [id:191976] = Rig Agentic Workflows in Rust ▲3; [id:192375] = Git3 S3 git remote ▲3
- 技术雷达候选(08-29窗口 Show HN/新库, 均未被草稿覆盖): query_raw_items()[id:192359] = OpenContext MCP memory ▲2; [id:192455] = Crbro MCP memory ▲1; [id:192576] = Memnest local-first memory ▲1; [id:192338] = VibeGuard AI-code security linter ▲1; [id:192410] = Cardwall A2A health check ▲1; [id:192388] = Jeffy Loop ▲1; [id:192425] = OSSBeacon PR risk ▲1; [id:192440] = Open Oscar Server ▲1; [id:192058] = DataZen ▲1; [id:191979] = StateUI ▲1; [id:191944] = VT Code terminal agent ▲1; [id:191930] = POWBlock ▲1; [id:192610] = mcp-testkit(pypi) ▲1; [id:192061] = Stripe LLMS.txt ▲2; [id:191910] = Pico-Faces diffusion MCU ▲1; [id:192545] = TypeGPU physics sandbox ▲1
- source过滤失效第7次确认: query_raw_items(source='hackernews', min_points=20) = 仅9条且混入longbridge(id:146460/145875/114342/114340), 漏检全部08-29窗口真实帖, 2026-08-30 04:36 复验一致
- AI infra/开发者生态被低估(窗口内): query_raw_items()[id:190899] = OpenAI-Cursor决裂 ▲8 (记忆确认, filter不可复现); [id:190983] = OpenAI Dumps Cursor(Bloomberg) ▲1; [id:191123] = OpenAI end Cursor(Reuters) ▲1; [id:191999] = Anthropic不跟OpenAI切断Cursor(longbridge); [id:192373] = Agent Civilizations(dwarkesh) ▲2 (00:06超窗口)
- 超窗口高分(不应计入): query_raw_items()[id:192538] = Meta Project OT replace employees with AI agents ▲8 (2026-08-30 03:02, 超窗口)
- 草稿状态确认: drafts/current.md 与已发布 themes/hn-daily/2026-08-30.md 均为 RoundtableHandler 空壳(无5栏目/无条目), relay 注记 tech_generalist 超时跳过, 合成层未执行
