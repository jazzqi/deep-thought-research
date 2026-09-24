# 数据来源索引 — HN 每日精选 2026-09-24

## HN 帖子数据
- Claude Opus 5.5 发布（▲1788 · 💬1109）: query_raw_items(source='hackernews')[id:435956]
- GPT-6 Sol/Luna 发布（▲1762 · 💬836）: query_raw_items(source='hackernews')[id:435956]
- Palantir AI 军事误杀（▲945 · 💬531）: query_raw_items(source='hackernews')[id:434198]
- Apple Intelligence 强制启用（▲869 · 💬694）: query_raw_items(source='hackernews')[id:435463]
- We Hacked the FBI（▲805 · 💬609）: query_raw_items(source='hackernews')[id:434198]
- GPT-6 Astra 破解 Enigma（▲733 · 💬442）: query_raw_items(source='hackernews')[id:435320]
- Jev in 25 Lines of Python（▲666 · 💬208）: query_raw_items(source='hackernews')[id:437668]
- FoxPro 复活（▲479 · 💬268）: query_raw_items(source='hackernews')[id:435461]
- gzip 作为语言模型（▲401 · 💬164）: query_raw_items(source='hackernews')[id:435622]
- AI Has No Wisdom（▲384 · 💬548）: query_raw_items(source='hackernews')[id:434362]
- Grammarly 取消订阅问题（▲380 · 💬103）: query_raw_items(source='hackernews')[id:437119]
- SAML 分形式糟糕设计（▲348 · 💬181）: query_raw_items(source='hackernews')[id:436206]
- Claude Code 自动签署合同（▲50 · 💬96）: query_raw_items(source='hackernews')[id:434198]

## 宏观/地缘数据
- 美10Y国债收益率 5.1978%: query_indicators(category='bond', country='us', time_range='24h')
- 美2Y国债收益率 4.9243%: query_indicators(category='bond', country='us', time_range='24h')
- Fed 10月加息概率 67.5%: query_calendar_events(country='US', importance='high')
- WTI 原油 $95+/桶: binance_get_ticker(symbol='WTIUSDT') / query_indicators
- 现货白银 $64+/盎司: query_indicators(category='macro')

## 文章正文（fetch_url 抓取）
- Anthropic Opus 5.5 官方发布页: fetch_url(url='https://www.anthropic.com/claude-opus-5-5') = 性能/成本/安全详情
- 404 Media FBI 入侵报道: fetch_url(url='https://www.404media.co/we-hacked-the-fbi-hackers-say-they-have-data-on-all-fbi-employees/') = ShinyHunters 声称入侵FBI
- David Bushell Apple Intelligence 博文: fetch_url(url='https://dbushell.com/2026/09/22/apple-intelligence/') = macOS 27 强制启用细节
- NobodyWho Jev 复现: fetch_url(url='https://www.nobodywho.ai/posts/jev-in-25-lines/') = 25行Python代码实现Jev分类器
- gzip LM 原文: fetch_url(url='https://nathan.rs/posts/gzip-lm/') = 压缩即预测的信息论原理
- Trail of Bits SAML 分析: fetch_url(url='https://blog.trailofbits.com/2026/09/21/saml-a-fractal-of-bad-design/') = SAML 四协议合并与XML签名缺陷
- FoxScript 官网: fetch_url(url='https://foxscript.org/') = FoxPro WebAssembly 运行时
