# Reference Data Sources — 2026-09-24 HN Daily

## 帖子数据来源（query_raw_items）

- Claude Opus 5.5 发布: query_raw_items(source='hackernews', keyword='Claude Opus 5.5', published_after='2026-09-22T00:00:00Z', published_before='2026-09-25T00:00:00Z')[id:435736] = ▲1788 💬1109，Anthropic 发布 Claude 5.5 系列首款模型
- GPT-6 Sol and Luna 发布: query_raw_items(source='hackernews', keyword='GPT-6 Sol Luna', published_after='2026-09-22T00:00:00Z', published_before='2026-09-25T00:00:00Z')[id:435956] = ▲1762 💬836，OpenAI 发布双模型矩阵
- Palantir AI 军事误杀: query_raw_items(source='hackernews', keyword='Palantir Pentagon', published_after='2026-09-22T00:00:00Z', published_before='2026-09-25T00:00:00Z')[id:436090] = ▲945 💬531，五角大楼确认 AI 过度依赖导致误杀
- Apple Intelligence 强制启用: query_raw_items(source='hackernews', keyword='Apple Intelligence', published_after='2026-09-22T00:00:00Z', published_before='2026-09-25T00:00:00Z')[id:434197] = ▲869 💬694，用户关闭后被自动重新启用
- Apple iOS 持久性广告: query_raw_items(source='hackernews', keyword='Apple ads iOS', published_after='2026-09-22T00:00:00Z', published_before='2026-09-25T00:00:00Z')[id:435463] = ▲799 💬592，用户无法关闭推荐内容
- FBI 数据泄露: query_raw_items(source='hackernews', keyword='FBI hacked', published_after='2026-09-22T00:00:00Z', published_before='2026-09-25T00:00:00Z') = ▲805 💬609，ShinyHunters 声称获取全部雇员数据
- Jev in 25 Lines of Python: query_raw_items(source='hackernews', keyword='Jev Python', published_after='2026-09-22T00:00:00Z', published_before='2026-09-25T00:00:00Z')[id:437668] = ▲666 💬208，极简复现 Jev 架构核心
- SAML fractal of bad design: query_raw_items(source='hackernews', keyword='SAML', published_after='2026-09-22T00:00:00Z', published_before='2026-09-25T00:00:00Z')[id:436147] = ▲348 💬181，Trail of Bits 深度剖析协议缺陷
- FoxScript FoxPro: query_raw_items(source='hackernews', keyword='FoxScript FoxPro', published_after='2026-09-22T00:00:00Z', published_before='2026-09-25T00:00:00Z')[id:436274] = ▲479 💬268，WebAssembly 运行时复活经典语言
- gzip as language model: query_raw_items(source='hackernews', keyword='gzip language model', published_after='2026-09-22T00:00:00Z', published_before='2026-09-25T00:00:00Z')[id:433788] = ▲401 💬164，压缩即预测的信息论验证
- GPT-6 Astra Enigma: query_raw_items(source='hackernews', keyword='GPT-6 Astra Enigma', published_after='2026-09-18T00:00:00Z', published_before='2026-09-25T00:00:00Z')[id:427676] = ▲396 💬180，破解 WWI 德国无线电密码
- Claude Code 自动签约: query_raw_items(source='hackernews', keyword='Claude Code contract', published_after='2026-09-22T00:00:00Z', published_before='2026-09-25T00:00:00Z')[id:434198] = ▲50 💬96，AI 代理越权签署法律文件
- AI Has No Wisdom: query_raw_items(source='hackernews', keyword='AI wisdom', published_after='2026-09-22T00:00:00Z', published_before='2026-09-25T00:00:00Z') = ▲384 💬548，哲学反思 AI 能力与智慧的区别
- Mac Mini M6 review: query_raw_items(source='hackernews', keyword='Mac Mini M6', published_after='2026-09-18T00:00:00Z', published_before='2026-09-25T00:00:00Z')[id:432031] = ▲109 💬90，Ars Technica 评测

## 宏观数据来源

- 美 10Y 国债收益率: query_indicators(category='bond', time_range='24h', limit=10, country='us') = 5.1978%
- 美 2Y 国债收益率: query_indicators(category='bond', time_range='24h', limit=10, country='us') = 4.9243%
- Fed 加息概率: query_calendar_events(days=14, lookback_days=7, importance='high,medium', country='US', limit=50) = CME FedWatch
- WTI 原油: query_indicators(category='macro', time_range='24h', limit=5, country='us') = $95+/桶
- 现货白银: query_indicators(category='macro', time_range='24h', limit=5) = $64+/盎司
- 富时 A50 期指: query_indicators(category='macro', time_range='24h', limit=5, country='cn') = 14318