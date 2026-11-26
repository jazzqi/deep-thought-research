# Reference — HN 书摘 2026-11-26

## query_raw_items（source='hackernews'，2026-11-26 UTC 窗口，limit=50）

- Google Research 无条件亚指数整数分解（▲116/💬15，Points:20/1评论）: query_raw_items(source='hackernews', limit=50)[id:823908] = Cogentic agent（Gemini 4 底座）无人工干预生成整数分解论文 + Lean 4 形式化
- Google Workspace MCP 强制令（▲96/💬110，Points:24/5评论）: query_raw_items(source='hackernews', limit=50)[id:824318] = 2027-02-01 起 AI agent 必须经 MCP 访问 Workspace，Gmail MCP 发不出邮件
- Notion 官方 MCP 注入隐藏 upsell（▲27/💬9，Points:20/7评论）: query_raw_items(source='hackernews', limit=50)[id:825148] = Notion MCP 向 agent 上下文注入隐藏商业指令
- OpenAI 成本调优实测（▲27/💬10，Points:26/9评论）: query_raw_items(source='hackernews', limit=50)[id:825133] = Astra/Sol 6.2 推理与输出 token 显著下降，p 值显著
- OpenAI 收紧 GPT-6.2 用量（▲435/💬245，Points:22/7评论）: query_raw_items(source='hackernews', limit=50)[id:822984] = Astra 触限快 40%、Sol 快 25%
- f-ck_data_brokers.py（▲70/💬10，Points:66/10评论）: query_raw_items(source='hackernews', limit=50)[id:825193] = 零依赖 Python 脚本批量向数据经纪发删除请求
- Mirror life 监管社论（▲49/💬74，Points:39/48评论）: query_raw_items(source='hackernews', limit=50)[id:823699] = 经济学人主张事前监管镜像生命
- S&P 警告英伟达董事会（▲32/💬6，Points:20/4评论）: query_raw_items(source='hackernews', limit=50)[id:822237] = 美方未发现中国指使间谍证据，S&P 仍警告董事会被渗透
- AMD llama.cpp 补丁（▲60/💬14，Points:37/6评论）: query_raw_items(source='hackernews', limit=50)[id:825020] = rdna-boosts 把 token 生成 35→55/s、prefill 700→1300/s
- Minipg 单可执行文件（▲264/💬42，Points:21/1评论）: query_raw_items(source='hackernews', limit=50)[id:823049] = Zig h9 运行 postgres:18-alpine，无 Docker/VM
- Rvoip Rust VoIP 栈（▲35/💬12，Points:20/4评论）: query_raw_items(source='hackernews', limit=50)[id:825210] = SIP/RTP/WebRTC/QUIC/voice-AI 统一库，3165 commits
- Ask HN 41 岁人生意义（▲41/💬70）: query_raw_items(source='hackernews', limit=50)[id:825086] = AI 冲击下的开发者情绪切片

## fetch_url（正文与评论抓取）

- 整数分解论文 README: fetch_url(github.com/google-research/.../integer_factorization) = L_N[1/3,105] 期望时间、Mathlib-only Lean 4 形式化、Gemini 4 底座、无人工干预
- 整数分解 HN 评论: fetch_url(news.ycombinator.com/item?id=50651627) = mentalgear 引 Gemini"不威胁 RSA"；credit_guy"上界≠下界"
- Google MCP 正文: fetch_url(techstackups.com/articles/google-workspace-ai-agents-mcp/) = 2027-02-01 生效、30 天记忆上限、禁训练
- Google MCP HN 评论: fetch_url(news.ycombinator.com/item?id=50653477) = Schnitz"浏览器绕过"；mooreds"提示注入上头条"
- OpenAI cost control 正文: fetch_url(micjm.com/blog/openai-is-in-cost-control-mode/) = 输出下降 p=0.0055/0.022，推理下降 p=0.00013/0.0064
- AMD llama.cpp 正文: fetch_url(devnull.land/amd-specific-llama-cpp) = 35→55 tokens/s、700→1300 tokens/s；Strata 16GB 跑 180B
- Minipg 正文: fetch_url(progrium.github.io/minipg/) = h9/Zig、postgres:18-alpine、35MB demo
- Rvoip 正文: fetch_url(github.com/eisenzopf/rvoip) = 3165 commits、Asterisk/FreeSWITCH 互操作
- f-ck_data_brokers 正文: fetch_url(github.com/gary23w/f-ck_data_brokers) = 数据经纪产量放大近 1000 倍（作者称）
- Ask HN 评论: fetch_url(news.ycombinator.com/item?id=50657957) = 68 岁创业者"AI 如 90 年代互联网泡沫，量级更大"


- NP_R≠PAR_R（▲76/💬61，Points:34/13评论）: query_raw_items(source='hackernews', limit=50)[id:825000] = BSS 模型实数 permanent 无短证书，Claude Fable 5.2 生成、Lean 4 形式化、未同行评议
- 量子引力代数量子化（▲135/💬38，Points:22/2评论）: query_raw_items(source='hackernews', limit=50)[id:824028] = arXiv 2611.34924，null cone 背景无关量子化，54 页
- DeepSeekMath（▲30/💬8，Points:20/5评论）: query_raw_items(source='hackernews', limit=50)[id:825101] = 7B 模型 MATH 基准 51.7%
- Moat 作为 OpenRouter 替代（▲152/💬98，Points:26/16评论）: query_raw_items(source='hackernews', limit=50)[id:823792] = $5/月无限批发 token 会员制
- Nvidia 暂停东南亚出货（▲27/💬5，Points:20/4评论）: query_raw_items(source='hackernews', limit=50)[id:824416] = FT 报道
- NP_R≠PAR_R 正文: fetch_url(github.com/samueleverett01/bss-permanent-separations) = Claude Fable 5.2 找到证明、Lean 4 形式化、明确未同行评议
- DeepSeekMath 正文: fetch_url(github.com/deepseek-ai/deepseek-math) = 7B、MATH 51.7%、500B token 数学继续预训练
- 量子引力正文: fetch_url(arxiv.org/abs/2611.34924) = 2026-11-25 提交、54 页、Bekenstein-Hawking 熵与一圈对数修正


## ai_specialist 接力补充（2026-11-26 22:26 UTC，LongBridge news/company 查询）

- AI 基建信用压力（CDS 创纪录）: query_longbridge_by_route(news/company, symbol=GOOGL.US) = 2026-11-25 报道 NVIDIA/Oracle/Alphabet/SpaceX/CoreWeave 五年期 CDS 利差同创历史新高，CoreWeave 隐含 68% 五年违约风险，S&P 将 NVIDIA 列入负面观察
- 美股 AI 抛售: query_longbridge_by_route(news/company, symbol=AMD.US) = 2026-11-25 Nasdaq 跌逾 3%、半导体 ETF 跌 7%、NVIDIA 跌 8%、AMD/Micron/Intel 跌逾 9%
- AMD 认股权证绑定 GPU 采购: query_longbridge_by_route(news/company, symbol=AMD.US) = 2026-11-26 AMD 股价 -1.75% 至 $406.03，注册 3.37 亿股转售，主要关联 OpenAI/Meta 持有的 GPU 采购认股权证，归属条件含 6GW Instinct GPU 部署与最高 $600 股价目标
- OpenAI-AMD GPU 优化合作: query_longbridge_by_route(news/company, symbol=AMD.US) = 2026-11-25 OpenAI 与 AMD 合作优化旗舰 GPU，性能提升 14%
- NVIDIA 出口管制收紧: query_longbridge_by_route(news/company, symbol=NVDA.US) = 2026-11-26 芯片卖家要求 neocloud 买家排除中国租户，NVIDIA 暂停对马来西亚/新加坡/泰国/印尼服务器出货
- Alphabet Gemini 延迟股东诉讼: query_longbridge_by_route(news/company, symbol=GOOGL.US) = 2026-11-26 集体诉讼指控 2026-05 至 07 就 Gemini 3.5 Pro 开发时间线作虚假陈述，首席原告截止日 2026-12-01
- Gemini 推荐 Amazon 却不链接: query_longbridge_by_route(news/company, symbol=GOOGL.US) = 2026-11-26 Semrush 研究显示 Gemini 在 40.5% 假日购物提示中提及 Amazon 但从不引用 amazon.com，因 Amazon 用 robots.txt 屏蔽 Google-Extended 爬虫



## tech_generalist 接力补充（2026-11-26 22:30 UTC，估值/一致预期/评级/行情 + 宏观框架）

- NVDA 实时报价（2026-11-26）: market_quote(NVDA.US) = 149.30，prev 155.38，-6.08（-3.91%），量 3.67 亿股，额 533.17 亿美元
- AMD 实时报价（2026-11-26）: market_quote(AMD.US) = 406.03，prev 413.27，-7.24（-1.75%），量 5163.20 万股
- GOOGL 实时报价（2026-11-26）: market_quote(GOOGL.US) = 273.10，prev 279.05，-5.95（-2.13%）
- MSFT 实时报价（2026-11-26）: market_quote(MSFT.US) = 489.93，prev 496.13，-6.20（-1.25%）
- META 实时报价（2026-11-26）: market_quote(META.US) = 609.89，prev 589.82，+20.07（+3.40%，五巨头中唯一上涨）
- NVDA 估值（2026-11-26）: query_longbridge_by_route(fundamental/valuation/pe, symbol=NVDA.US) = PE 28.55x（区间 28.55–44.68，中位 33.92，处历史最低位）
- AMD 估值（2026-11-26）: query_longbridge_by_route(fundamental/valuation/pe, symbol=AMD.US) = PE 92.83x（区间 92.83–157.48，中位 121.28，处历史最低位）
- GOOGL 估值（2026-11-26）: query_longbridge_by_route(fundamental/valuation/pe, symbol=GOOGL.US) = PE 17.17x（区间 17.17–30.41，中位 27.65，处历史最低位）
- NVDA 一致预期（2026-11-26）: query_longbridge_by_route(fundamental/consensus, symbol=NVDA.US) = FY2027 Q3 营收实际 1158.44 亿美元 vs 预期 1087.11 亿（Beat 6.6%），EPS 实际 2.70 vs 预期 2.4597（Beat）；FY2027 Q4 营收预期 1308.26 亿美元
- AMD 一致预期（2026-11-26）: query_longbridge_by_route(fundamental/consensus, symbol=AMD.US) = FY2026 Q3 营收实际 133.77 亿美元 vs 预期 130.94 亿（Beat），EPS 实际 1.46 vs 预期 1.4176（Beat）
- NVDA 机构评级（2026-11-26）: query_longbridge_by_route(market/institutional_rating, symbol=NVDA.US) = Buy（SB39/B10/H12/S2）；目标价 425 与现价 149.30 偏离 +185%，口径存疑未采用
- AMD 机构评级（2026-11-25）: query_longbridge_by_route(market/institutional_rating, symbol=AMD.US) = StrongBuy（SB42/B6/H6）；目标价 1250 与现价 406.03 偏离 +208%，口径存疑未采用
- GOOGL 机构评级（2026-11-25）: query_longbridge_by_route(market/institutional_rating, symbol=GOOGL.US) = StrongBuy（SB43/B11/H6）；目标价 500 与现价 273.10 偏离 +83%，口径存疑未采用
- 宏观折现率框架（2026-11-17 基准）: read_skill(shared/us-macro-backdrop.md) = Goolsbee 将 AI CapEx 定性为通胀源，传导链 AI CapEx↑→通胀↑→利率更高更久→Mag7 自由现金流折现率上升；联邦基金 3.75–4.00%，12 月加息 25bp 概率 95%（SEP 会议，2026-11-16 CME FedWatch）
