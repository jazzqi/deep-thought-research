# 数据来源溯源 · HN 书摘 2026-10-08（窗口 2026-10-07 UTC）

> 管道状态：raw_items hackernews 源仍停摆（最新入库条目 2026-09-23，2026-10-08 复核无新增）。本期热度/评论数据全部经 fetch_url 直查 HN 公开 Algolia API 绕行获取。

## 主窗口取数（Algolia API）

- 2026-10-07 UTC 窗口 Top 帖列表（分数/评论/作者/时间）: fetch_url(https://hn.algolia.com/api/v1/search?tags=story&numericFilters=created_at_i>1791331200,created_at_i<1791417600&hitsPerPage=30) = Claude Haiku 5.5 ▲540/💬251 [story_id:49996437]；JPEG XL in Chrome ▲450/💬289 [49991227]；Visa/MC 诉讼 ▲429/💬291 [49993914]；GPT-6 Intelligent UI ▲388/💬186 [49996425]；C64 键帽字体 ▲363/💬61 [49990224]；化学诺奖 ▲276/💬53 [49990470]；Strands Decider 2B ▲274/💬78 [49987076]；Bigwords.page ▲265/💬92 [49994443]；ASCII 动画 ▲240/💬55 [49993857]；GitHub 故障 ▲223/💬176 [49994027]；Navier-Stokes 论文 ▲198/💬137 [49994145]；Meta/MS 缩减 Claude ▲192/💬202 [49997161]
- 窗口次级帖（points<198 补充）: fetch_url(同上 + numericFilters …,points<198) = 反模式博客 ▲179/💬101 [49992257]；ESP32-C3 Adblock ▲177/💬73 [49986862]；Mathocalypse ▲149/💬156 [49997718]；PSP→WASM ▲137/💬73 [49991243]；3D 艺术博物馆 Show HN ▲137/💬60 [49992057]；伪造 TLS 证书 ▲137/💬47 [49988230]

## 正文抓取

- Claude Haiku 5.5 发布页（成本/基准/调价）: fetch_url(https://www.anthropic.com/claude-haiku-5-5) = 较 Haiku 4.5 便宜约 75%；GDPval-AA 1620（Luna 1437/Sonnet 5.5 1840）；OSWorld 72.4%；TB4.0 39.2%（Luna 16.4%）；Sonnet 5.5 缓存读取砍半；Max/Team 新增月度 API credit
- JPEG XL in Chrome: fetch_url(https://developer.chrome.com/blog/jpeg-xl-in-chrome) = Chrome 155 起解码；纯 Rust jxl-rs；压缩率高 30-50%；target_feature_11 + SIMD 无 unsafe
- Strands Decider 2B: fetch_url(https://strandsagents.com/blog/introducing-strands-decider/) = Qwen3.5-2B 躯干 + pointer head（~1M 参数）；v19；权重/数据/脚本全开源；JevBench 对齐
- Navier–Stokes Lost in Translation 摘要: fetch_url(https://arxiv.org/abs/2610.08144) = arXiv:2610.08144（2026-10-06 提交）；SCI=∞ 论证；点名 OpenAI NS 证明 Lean 形式化与 NL 证明不对应
- Meta/MS 缩减 Claude（The Information 二手转述）: fetch_url(https://www.rswebsols.com/news/meta-and-microsoft-take-steps-to-reduce-employee-usage-of-claude-ai/) = 微软内部 Anthropic 年支出预期砍超 1/3（原超 $1B）；月度支出上限 $100k→约 $10k；Meta Claude Code 用户 6 万→3 万；MetaCode 3 万+内部用户；Muse Code 6 千+；Meta 28 天向 Claude Code 投入超 $105M；Anthropic 年化收入节奏 $65B
- The Mathocalypse（Aaronson）: fetch_url(https://scottaaronson.blog/?p=10169) = OpenAI 一日发布 372 项成果含 UGC 证明、L=BPL、整数乘法 O(n log^0.9999999999999 n)；Lean 证书在但无人读懂；Moshkovitz 一线吐槽
- ESP32-C3 Adblock README: fetch_url(https://github.com/M-Abozaid/esp32-c3-adblock) = 40-bit FNV-1a 哈希存 flash 二分；14 万域名 0.67MB flash/~50KB RAM/~10ms
- PSP→WASM README: fetch_url(https://github.com/snuri00/psp-web-recomp) = 静态重编译 + HLE 内核 + WebGL2；GoW 60fps@4x；Ghost of Sparta 55-60fps@3x
- 反模式博客正文: fetch_url(https://refactoringenglish.com/blog/anti-patterns-software-blogging/) = 游荡式开场等 8 类反模式；前 3 句须答"写给谁、有何好处"
- Bigwords.page / 3D 艺术博物馆: fetch_url(https://bigwords.page/) = URL 即全屏标牌，无账号无服务器；fetch_url(https://artmuseum.artfrompixels.com/) = Wikipedia 数据构建可步行 3D 艺术史博物馆
- GPT-6 Intelligent UI 正文: fetch_url(https://openai.com/index/gpt-6-for-everyone/) = 403 未能抓取（已在稿件标注）
- 伪造 TLS 证书正文: fetch_url(arstechnica.com/…) = 405 未能抓取（仅用标题+热度，入 Top10 快照不入正文栏目）

## 评论摘录（Algolia comments API）

- Haiku 5.5 评论: fetch_url(hn.algolia.com/api/v1/search?tags=comment,story_49996437) = 作者 XCSme 实测对比链接；作者 cjav_dev（Anthropic）回应 credits FAQ
- GPT-6 UI 评论: fetch_url(…comment,story_49996425) = 作者 skapadia 按需生成 UI 观点
- JPEG XL 评论: fetch_url(…comment,story_49991227) = 作者 F3nd0 指 Mozilla 对 AVIF/JXL 双标
- Navier-Stokes 评论: fetch_url(…comment,story_49994145) = 作者 auggierose / NewsaHackO 对论文示例的质疑
- Mathocalypse 评论: fetch_url(…comment,story_49997718) = 作者 furyofantares 算力-可及性评论
- Meta/MS 评论: fetch_url(…comment,story_49997161) = 作者 pinkmuffinere 边际效用评论
- Strands Decider 评论: fetch_url(…comment,story_49987076) = 作者 girvo 需求侧自建数据集
- ESP32 评论: fetch_url(…comment,story_49986862) = 作者 Muhammad523 "Claude 贡献者"弃读评论
- 反模式博客评论: fetch_url(…comment,story_49992257) = 作者 godelski 讲故事/LLM 反感评论

## 跨天去重判定（fallback 注入条目）

- 跨天去重弃用（fallback 注入 12 条，全部与往期已发布条目重复）: query_raw_items(source='hackernews', min_points=1 全源兜底)[id:396507,400453,427782,435736,435956,427861,426873,394966,432439,432085] = 2026-09-15~09-22 冻结快照条目（e-ink 鸟/Jev/AI 海报/Opus 5.5/GPT-6 Sol+Luna/Laya/Android 17/PNG/MiMo/Attention），已见于 2026-09-15~09-22 及 2026-10-07 各期，按跨天去重规则整体不入本期
- query_raw_items(source='hackernews', published_after=2026-10-07, published_before=2026-10-08, min_points=20) = 返回 4 条无关旧条目（日期过滤未命中，管道断流所致），已弃用


## 第 3/3 棒（tech_generalist 收尾）补充取数

- MSFT 财务/估值（10-07 收盘）: fetch_url(https://stockanalysis.com/stocks/msft/) = 529.76 美元；市值 3.93T；TTM 营收 331.84B(+17.8%)；净利 133.75B(+31.3%)；PE 29.49 / 前瞻 26.77；56 分析师一致 Strong Buy、目标价 587.63(+10.9%)；财报日 2026-10-28
- META 财务/估值（10-07 收盘）: fetch_url(https://stockanalysis.com/stocks/meta/) = 721.31 美元(-2.38%)；市值 1.84T；TTM 营收 228.25B(+27.7%)；TTM 净利 68.10B(-4.8%)；PE 27.18 / 前瞻 22.43；63 分析师目标价 798.48(+10.7%)；财报日 2026-10-28
- GOOGL 财务/估值（10-07 收盘）: fetch_url(https://stockanalysis.com/stocks/googl/) = 350.50 美元；市值 4.29T（页面标注 +44.5%）；TTM 营收 445.87B(+20.1%)；净利 244.12B(+111.3%)；PE 17.59；目标价 429.47(+22.53%)；财报日 2026-10-28
- 长桥 news/company 与 market_quote 查询失败（MSFT/META/GOOGL/NVDA）: query_longbridge_by_route(news/company, market_quote) = OpenApiException code=401003 token expired，公司新闻与报价未能交叉验证，本期财务坐标全部改用 stockanalysis.com 公开页
- query_indicators(country=us, category=sentiment, 24h) = 无指标返回，宏观情绪数据缺失


## tech_scout 交叉审查核验补充（2026-10-08，审查人 tech_scout）

> 说明：审查人独立用 query_raw_items 复核 draft 的关键事实与同窗口遗漏事件。长桥 market_quote 与 news/company 复测均 401003 token expired（与 draft 披露一致），公司/宏观交叉验证改由 telegram:Financial_Express 快讯承担。

- 独立核验 Haiku 5.5（75% 降本/Sonnet 5.5 缓存砍半至 $0.10/M/Max+Team 月度 API credit/AWS·GCP·Azure 全平台上线）: query_raw_items(keyword='Anthropic', published_after=2026-10-01)[id:466592,466796,466577] = Financial Express 多条快讯，与 draft 条 2 摘要吻合
- 三星电子 Q3 初步业绩（营业利润 107.4 万亿韩元，同比约 +783%，超分析师预期；营收 195 万亿韩元不及预期）: query_raw_items(keyword='三星 OR Samsung', published_after=2026-10-01)[id:466860,466869,466908] = 10-07 22:45 UTC 监管申报口径，AI 内存需求驱动
- 三星 12 层 HBM4E 通过英伟达等客户质量验证: query_raw_items(keyword='三星 OR Samsung', published_after=2026-10-01)[id:465295] = 韩国经济日报，供应规模/量产时点未定
- 隔夜要闻：SpaceX 洽谈 400 亿美元英伟达 GPU 采购融资（Apollo 等）；GPT-6 全量上线所有 ChatGPT 用户并取代 GPT-5.6 SOL/LUNA；博通为 OpenAI 定制芯片安排超 50 亿美元债务；Fed 纪要 9 月升息一致支持、多数倾向年内再加一次: query_raw_items(keyword='SpaceX OR 英伟达 OR GPU', published_after=2026-10-05)[id:466875] = 10-08 隔夜要闻一览（10-07 23:00 UTC）
- 甲骨文/博通/SpaceX 为 AI 芯片寻求债务协议（WSJ）: query_raw_items(keyword='SpaceX OR 英伟达 OR GPU', published_after=2026-10-05)[id:466774] = 10-07 21:02 UTC
- SpaceX 大举举债引发信用风险担忧: query_raw_items(keyword='SpaceX OR 英伟达 OR GPU', published_after=2026-10-05)[id:466596,466594] = 10-07 18:21-18:23 UTC
- 谷歌 SynthID Detector 全球开放（日检测请求超 100 万次，伙伴含 OpenAI/英伟达/Kakao，苹果将加入）: query_raw_items(keyword='SpaceX OR 英伟达 OR GPU', published_after=2026-10-05)[id:466667] = 10-07 19:23 UTC
- 英伟达竞购 OpenRouter 失利，推进多笔大额投资（含 60 亿美元 Poolside 授权/团队吸纳以推进 Nemotron）: query_raw_items(keyword='Strands OR Decider OR AWS OR 开源', published_after=2026-09-28)[id:466008] = 10-07 13:09 UTC
- AWS 推出物理人工智能（Physical AI）工具链: query_raw_items(keyword='Strands OR Decider OR AWS OR 开源', published_after=2026-09-28)[id:466782,466783] = 10-07 21:10-21:11 UTC
- 佛州总检察长申请对 Meta 下达临时禁令（关闭致青少年成瘾功能）: query_raw_items(keyword='Microsoft OR Meta OR Claude')[id:466279,466283] = 10-07 15:12-15:15 UTC
- 微软：Meta Muse 模型即将登陆 Windows；Copilot 混合本地模型数月内上线；Microsoft Execution Containers 阻止 AI 智能体未授权访问数据: query_raw_items(keyword='Microsoft OR Meta OR Claude')[id:466494,466495,466453,466454] = 10-07 17:15-17:35 UTC
- Surface Laptop Ultra 定价 2599 美元起、主打本地 AI（本地推理速度约为 MacBook Pro M5 两倍）: query_raw_items(keyword='SpaceX OR 英伟达 OR GPU', published_after=2026-10-05)[id:466624] = 10-07 18:56 UTC
- 美股 10-07 收盘（Meta -2.38%、微软 +0.09%、谷歌 +0.81%）: query_raw_items(keyword='Microsoft OR Meta OR Claude')[id:466713] = 10-07 20:01 UTC，佐证 draft 条 3 财务段 Meta 当日跌幅
- 10 年期美债收益率一度升破 5.352%（创 24 年新高）: query_raw_items(全源最近条目 limit=50)[id:466925] = 10-07 23:28 UTC
- 韩国多家银行遭黑客攻击（开源工具 ARTEX 滥用，可调用 Claude/GPT）: query_raw_items(全源最近条目 limit=50)[id:466918] = 10-07 23:20 UTC
- 长桥复测（审查人独立验证 draft 的 token 过期披露）: query_longbridge_by_route(news/company, symbol=MSFT.US) 与 market_quote([GOOGL.US,MSFT.US,META.US]) = 均 401003 token expired，与 draft/reference 披露一致
