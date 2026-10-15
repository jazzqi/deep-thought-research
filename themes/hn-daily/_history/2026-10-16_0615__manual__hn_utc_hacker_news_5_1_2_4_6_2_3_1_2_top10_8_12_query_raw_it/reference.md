# 数据来源溯源 · HN 书摘 2026-10-15

- 候选池（50 条，2026-10-14 UTC 窗口）: query_raw_items(source='hackernews', min_points=20, published_after='2026-10-14T00:00:00Z', published_before='2026-10-15T00:00:00Z') = 50 条
- AI agent 安全基本功缺失报道: query_raw_items(source='hackernews', min_points=20, published_after='2026-10-14T00:00:00Z')[id:480719] = CSO Online：四起前沿模型越权事件归因安全工程欠账，▲933/💬585
- Linus 首个 LLM 辅助补丁: query_raw_items(...)[id:480663] = LWN：10 补丁 RCU folio 优化，read() 提速 10x，评审发现竞态，▲118/💬99
- ASML Q4 指引: query_raw_items(...)[id:480376] = Reuters：订单强劲缓解 AI 开支见顶担忧，▲172/💬34（正文 401 未抓取）
- Amazon 定价机制: query_raw_items(...)[id:479431] = not-ship.com 正文 fetch：卖家抽成 19%(2014)→近半，FTC 反垄断案核心，▲910/💬707
- AI 数据中心债转手: query_raw_items(...)[id:480775] = startupfortune 正文 fetch：JPM/Morgan Stanley/SMBC/MUFG 探索 SRT，$38B Oracle 租赁项目债 6 个月未分销，▲374/💬264
- Passkeys 辟谣: query_raw_items(...)[id:480381] = scotthelme 正文 fetch：同步密钥不返回 attestation，AAGUID 不暴露 OS/浏览器，▲637/💬787
- Scion vs Mononoke: query_raw_items(...)[id:480939] = sunshowers 正文 fetch：derived data 表述雷同，"近乎抄袭"，Opus 5.5/GPT-6 Astra 均可指出相似性，▲407/💬148
- LFM2.5-24B-A2B: query_raw_items(...)[id:481225] = liquid.ai 正文 fetch：24B/2B 激活，LiveClaw 48.09 vs Qwen3.6-35B-A3B 38.19，M5 Max 184 tok/s，▲278/💬73
- pg_vectorsearch: query_raw_items(...)[id:479831] = GitHub 仓库 fetch（仅 README 开头）：自称快过 pgvector IVFFlat/HNSW，▲206/💬52
- Yandex 遭袭后机器人迁移: query_raw_items(...)[id:480915] = Cloudflare 博客 fetch：AS13238 降幅几乎全是验证爬虫，恶意流量迁至其他托管商，10-13 仍低于基线 86-90%，▲275/💬114
- 理性主义博客冗长批评: query_raw_items(...)[id:479429] = alexwennerberg 正文 fetch：2.5 万词 Scott Alexander 长文、Gwern 尼古丁 9000 词结论被证伪，▲399/💬412
- TV4 AI agent 删素材: query_raw_items(...)[id:479889] = swedenherald：真人秀停播至 2027，正文未抓取，▲152/💬86
- Top10 快照分数/评论: query_raw_items(...)[id:480881,480719,479431,480955,478998,481018,480381,480594,480617,480661] = 见数据速览表
- 评论摘录（CSO 帖）: fetch_url(https://hn.algolia.com/api/v1/items/50091788) = 作者 altmanaltman 恐惧营销论及子线程反驳
- 评论摘录（Mononoke 帖）: fetch_url(https://hn.algolia.com/api/v1/items/50094694) = 作者 sunshowers 与作者 nomel 关于法律 vs 规范的多轮交锋
- 跨期去重基线: ReadThemeDocsTool(themes/hn-daily/2026-10-14.md) = 昨期覆盖 Gemini 4 Argon/Character.ai/HomeView/Rust unsoundness/Firefox Enterprise/Scion(Anthropic 博文本体)/Apple Minions/IMF 等，本期 Scion-Mononoke 为新帖新信息非重复

# 数据溯源 · HN 书摘 2026-10-15（覆盖 2026-10-14~10-15 UTC 双日窗口）

- 候选池（10-14 窗口，hn_points≥20）: query_raw_items(source=hackernews, published_after=2026-10-14T00:00:00Z, published_before=2026-10-15T00:00:00Z, min_points=20, limit=50) = 50 条
- 候选池（10-15 窗口，hn_points≥20）: query_raw_items(source=hackernews, published_after=2026-10-15T00:00:00Z, published_before=2026-10-16T00:00:00Z, min_points=20, limit=30) = 30 条
- 银行甩卖 AI 数据中心债（$38B Oracle 项目债滞销/Oracle CDS ~151bp/S&P BBB-/$40B 再融资）: fetch_url(https://startupfortune.com/banks-are-now-trying-to-offload-the-ai-data-center-debt-they-just-underwrote/) = 正文全文 [对应条目 id:480775]
- 银行甩卖帖评论（崩盘→消费级硬件减价联想）: fetch_url(https://hn.algolia.com/api/v1/items/50092664) = 评论树（作者 fasterik 等）
- ASML Q4 指引超预期: query_raw_items(source=hackernews, 10-14 窗口)[id:480376] = "ASML's strong orders ease fears AI spending boom is running out of steam"（▲49 · 💬34）
- ASML 订单簿排至 2029-2030/取消成本评论: fetch_url(https://hn.algolia.com/api/v1/items/50088430) = 评论树（作者 tartoran/jeroenhd 等）
- 路透：市场抛售与利率上行测试 AI 数据中心交易热潮: query_raw_items(source=hackernews, 10-15 窗口)[id:484529] = "Market selloff, rising rates test AI data centre deal boom"（▲27 · 💬14）
- 前沿实验室跳过安全基本功（OpenAI/Anthropic/Meta/Google 越权事件与专家诊断）: fetch_url(https://www.csoonline.com/article/4234854/ai-agents-arent-going-rogue-frontier-labs-are-skipping-security-basics.html) = 正文全文 [对应条目 id:480719]
- Scion 借鉴 Mononoke 争议: fetch_url(https://sunshowers.io/posts/anthropic-mononoke/) = 正文全文 [对应条目 id:480939]
- Scion/Mononoke 10-15 后续帖: query_raw_items(source=hackernews, 10-15 窗口)[id:484602] = "More on Anthropic's Scion ripping off Mononoke"（▲27 · 💬1）
- Scion/Mononoke 评论（诉诸规范而非法律）: fetch_url(https://hn.algolia.com/api/v1/items/50094694) = 评论树（作者 sunshowers/nomel 等）
- Passkeys 逐条反驳: fetch_url(https://scotthelme.co.uk/passkeys-are-not-a-trap/) = 正文全文 [对应条目 id:480381]
- AI 批量反编译游戏: fetch_url(https://popcar.bearblog.dev/ai-is-mass-decompiling-games-thats-both-awesome-and-scary/) = 正文全文 [对应条目 id:480520]
- AdFection 零点击间谍软件经广告投递: fetch_url(https://www.theguardian.com/technology/2026/oct/15/israeli-firm-digital-ads-enabling-installation-of-zero-click-spyware-researchers-say) = 正文全文 [条目 id:483860，Citizen Lab 原报告对应 id:484092]
- 数学家的哀歌（Duminil-Copin/Strogatz 语）: fetch_url(https://www.derekthompson.org/p/i-know-why-the-mathematicians-weep) = 正文全文 [对应条目 id:484074]
- LFM2.5-24B-A2B 规格与基准: fetch_url(https://www.liquid.ai/blog/lfm2-5-24b-a2b) = 正文全文 [对应条目 id:481225]
- Meta Muse Spark Open 规格（816B/42B 激活/1M 上下文/双 M5 Ultra 桌面运行）: fetch_url(https://research.meta.ai/blog/muse-spark-open) = 正文全文 [对应条目 id:484588]
- Torvalds 首个 LLM 辅助 patch 系列: fetch_url(https://lwn.net/Articles/1100449/) = 正文全文 [对应条目 id:480663]
- 理性主义博客冗长批评: fetch_url(https://alexwennerberg.com/blog/2026-10-13-long.html) = 正文全文 [对应条目 id:479429]
- Cloudflare：Yandex 宕机恶意机器人迁移而非消失: fetch_url(https://blog.cloudflare.com/yandex-outage/) = 正文全文 [对应条目 id:480915]
- Tesla Robotaxi 校园区超速 NHTSA 请愿: fetch_url(https://www.extremetech.com/cars/teslas-robotaxis-blow-through-school-zones-nhtsa-petition-alleges) = 正文全文 [对应条目 id:480715]
- LLM pelican 多样性坍塌/Design Creativity Bench: fetch_url(https://arcfu.com/post/the-emperor-pelican-has-no-clothes/) = 正文全文 [对应条目 id:480595]
- Top10 快照分数/评论数: query_raw_items(source=hackernews, 10-14 与 10-15 双窗口, min_points=20) = 各条 Points/Comments 元数据
- 跨天去重基线: ReadThemeDocsTool(themes/hn-daily/2026-10-14.md, themes/hn-daily/index.md) = 往期标题比对，本期条目与往期无重复

- 美国 CPI 同比最新可查读数: query_indicators(category=macro, country=us, time_range=7d) = 3.7%（cpi_yoy_us_pct，akshare，数据标注 2026-09）
- 美联储资产负债表: query_indicators(category=macro, country=us, time_range=7d) = 6,747,560 百万美元（openbb，2026-10-07）
- Reuters 抛售与利率上行测试 AI 数据中心交易: query_raw_items(source=hackernews, published_after=2026-10-13T00:00:00Z)[id:484529] = ▲51/51 评论，Market selloff, rising rates test AI data centre deal boom
- 本轮条目 id 与快照分数复核: query_raw_items(source=hackernews, published_after=2026-10-13T00:00:00Z) = [id:480719]▲933（CSO 安全基本功）、[id:480939]▲407（Scion/Mononoke 首篇）、[id:484602]▲72（续篇 ripping off）、[id:484588]▲70（Muse Spark Open）、[id:481225]▲278（LFM2.5-24B-A2B）、[id:480775]▲374（银行甩卖 AI 数据中心债）、[id:480376]▲172（ASML 订单强劲）


## 2026-10-15 HN 日报 · tech_scout 复核轮追加

- AdFection 事件正文（Controlium 平台细节/Al Jazeera 中招/投放面含 UN、NATO、ICC、IAEA 网络用户）: fetch_url(https://www.theguardian.com/technology/2026/oct/15/israeli-firm-digital-ads-enabling-installation-of-zero-click-spyware-researchers-say) = Guardian 2026-10-15 正文，Citizen Lab（多伦多大学）称 Discover Tech 的 Controlium 平台在广告展示环节 harvest 身份/IP，目标用户随即被第三方间谍软件零点击植入；2024 年起全球数百万用户被投放（含也门/巴西/墨西哥/捷克），Al Jazeera 数十台设备被入侵；Confiant 相关工作显示广告出现在欧美政府机构、联合国、NATO、ICC、IAEA 网络
- AdFection HN 讨论高赞业内评论（AdTech 工程师 13 年）: fetch_url(https://news.ycombinator.com/item?id=50101813) = 主帖抓取时 348 points/506 comments（快照 308/459）；作者 Postosuchus 指报告 zero-click 机制含糊、AdTech 无单一"ad provider"、体量决定无法逐条审查、监管大概率"罚 Google 放走真凶"
- HN 窗口条目与分数复核: query_raw_items(source=hackernews, published_after=2026-10-14T00:00:00Z, published_before=2026-10-16T12:00:00Z, min_points=20, limit=60) = 60 条；稿件引用条目 id:480719(▲933)、id:480955(▲813)、id:480381(▲637)、id:483860(▲491)、id:480939(▲407)、id:480775(▲374)、id:484074(▲310)、id:484092(▲308)、id:481225(▲278)、id:480376(▲172)、id:480976(▲326)、id:4808663(▲118)、id:484393(▲101) 与稿件一致
- OpenCode 2.0 正文复抓: fetch_url(https://anoma.ly/notes/opencode-2-0/) = 仍为重度 CSS 渲染，正文未抽出，维持"未能抓取"标注

- Goodfire《Neural Networks Are Already Clean》快照: query_raw_items(source=hackernews, published_after=2026-10-15, min_points=20)[id:484505] = ▲444/163评，Goodfire（Nick Cammarata）主张 polysemanticity 的 superposition 解释被误读，机制可解释性前景好于预期
- Goodfire 长文正文核验: fetch_url(https://already-clean.goodfire.com/) = "网络的机制本身就是可读构建块……叠加是错误解释，真实模式是递归泛化；现已能理解至万亿参数模型的大多数神经元"
- 404media ChatGPT 广告定向实测: query_raw_items(source=hackernews, published_after=2026-10-15, min_points=20)[id:484294] = ▲36/6评，OpenAI 广告可按 prompt、邮箱、手机号/设备标识定向，404media 自行投放两条测试广告
- 404media 正文核验: fetch_url(https://www.404media.co/how-chatgpt-targets-ads-to-you-based-on-your-prompts-phone-number-and-email/) = 广告主可上传个人数据定向 ChatGPT 用户；定向维度含 prompts；OpenAI 2026-02 起在美国上线广告并扩至图像生成结果
- passkeys 争论时间线复核: query_raw_items(keyword=passkeys, source=hackernews, published_after=2026-09-15)[id:426173][id:473095][id:480381] = 9-18《I don't like passkeys》▲833/803评 → 10-12 Apple 工程师 Ricky Mondello 公开回应 ▲36 → 10-14《Passkeys Are Not a Trap》▲637/787评
- 2026-10-15 UTC 窗口全量复核: query_raw_items(source=hackernews, published_after=2026-10-15, min_points=20, limit=60) = 60 条，当日最高分 Guardian AdFection 报道 [id:483860] ▲491；Citizen Lab 原始研究 [id:484092] ▲308/459评；Scion 续篇 [id:484602] ▲72；Muse Spark Open [id:484588] ▲70

- 当日高分帖独立核验（Goodfire ▲444 未覆盖）: query_raw_items(source=hackernews, published_after=2026-10-13, published_before=2026-10-16)[id:484505] = Neural Networks Are Already Clean，Goodfire 出品，163 评论
- prompt injection 实测数据（未覆盖）: query_raw_items(source=hackernews, 2026-10-13~10-16)[id:484296] = HTTP header prompt injection，217M Web 响应
- Krea 3 图像模型（未覆盖）: query_raw_items(source=hackernews, 2026-10-13~10-16)[id:484506] = Krea 3，宣称 4× 快于 Nano Banana Pro，▲226
- ChatGPT 广告定向（未覆盖）: query_raw_items(source=hackernews, 2026-10-13~10-16)[id:484294] = 404media，按 prompt/手机号/邮箱投广告
- AI 数据中心交易承压（未覆盖）: query_raw_items(source=hackernews, 2026-10-13~10-16)[id:484529] = Reuters 抛售+利率测试 AI data centre deal boom，▲51
- Jev 电车难题帖（未覆盖）: query_raw_items(source=hackernews, 2026-10-13~10-16)[id:484658] = Jev Meets the Trolley Problem，▲65
- Simons Foundation AI 时代数学家（未覆盖）: query_raw_items(source=hackernews, 2026-10-13~10-16)[id:484298] = $15M effort，▲215
