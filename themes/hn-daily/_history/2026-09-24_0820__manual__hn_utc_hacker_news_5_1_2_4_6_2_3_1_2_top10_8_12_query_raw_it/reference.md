# Reference Data Sources

## Raw Items (Hacker News)
- GPT-6 Sol and Luna: query_raw_items(keyword=GPT-6, source=hackernews, published_after=2026-09-22T00:00:00Z, published_before=2026-09-24T00:00:00Z)[id:435956] = OpenAI发布GPT-6 Sol和Luna两个新模型
- Palantir AI Overreliance: query_raw_items(keyword=Palantir, source=hackernews, published_after=2026-09-22T00:00:00Z, published_before=2026-09-24T00:00:00Z)[id:436090] = 五角大楼承认Palantir AI技术过度依赖导致空袭造成123名伊朗儿童死亡
- GPT-6 Astra breaks Enigma: query_raw_items(keyword=GPT-6, source=hackernews, published_after=2026-09-22T00:00:00Z, published_before=2026-09-24T00:00:00Z)[id:435320] = OpenAI GPT-6 Astra自主破解2005年以来未解的Enigma密码
- Jev in 25 Lines of Python: query_raw_items(keyword=Jev, source=hackernews, published_after=2026-09-22T00:00:00Z, published_before=2026-09-24T00:00:00Z)[id:437668] = NobodyWho发布讽刺性博文，用25行Python代码实现"Jev架构"
- SAML: A Fractal of Bad Design: query_raw_items(keyword=SAML, source=hackernews, published_after=2026-09-22T00:00:00Z, published_before=2026-09-24T00:00:00Z)[id:436147] = Trail of Bits深度分析SAML协议设计缺陷
- Claude Opus 5.5 Analysis: query_raw_items(keyword=Claude, source=hackernews, published_after=2026-09-22T00:00:00Z, published_before=2026-09-24T00:00:00Z)[id:435876] = Artificial Analysis对Claude Opus 5.5的全面评估
- Waymo Transit Rewards: query_raw_items(keyword=Waymo, source=hackernews, published_after=2026-09-22T00:00:00Z, published_before=2026-09-24T00:00:00Z)[id:436989] = Waymo推出"Transit Rewards"计划，付费让用户乘坐公共交通
- Meta Muse 0-day: query_raw_items(keyword=Meta, source=hackernews, published_after=2026-09-22T00:00:00Z, published_before=2026-09-24T00:00:00Z)[id:435578] = Meta的AI助手Muse存在严重零日漏洞
- Drop rootless sandbox: query_raw_items(keyword=Drop, source=hackernews, published_after=2026-09-22T00:00:00Z, published_before=2026-09-24T00:00:00Z)[id:435461] = 新开源项目Drop提供无根Linux沙箱环境
- Unreal Agent: query_raw_items(keyword=Unreal, source=hackernews, published_after=2026-09-22T00:00:00Z, published_before=2026-09-24T00:00:00Z)[id:436106] = Unreal Labs发布Unreal Agent项目
- OpenAI employee fired: query_raw_items(keyword=OpenAI, source=hackernews, published_after=2026-09-22T00:00:00Z, published_before=2026-09-24T00:00:00Z)[id:435351] = OpenAI数据标注员工因使用AI训练AI而被解雇

## Article Content
- GPT-6 Astra breaks Enigma: fetch_url(url=https://www.cryptocellar.org/bgac/the-mvueh-break.html) = 详细技术分析，GPT-6 Astra自主开发Enigma模拟器和Bombe程序破解MVUEH消息
- Jev in 25 Lines of Python: fetch_url(url=https://www.nobodywho.ai/posts/jev-in-25-lines/) = 讽刺性博文，用25行Python实现本地LLM分类决策
- SAML: A Fractal of Bad Design: fetch_url(url=https://blog.trailofbits.com/2026/09/21/saml-a-fractal-of-bad-design/) = Trail of Bits深度分析SAML协议的XML签名包装攻击和设计缺陷
- Claude Opus 5.5 Analysis: fetch_url(url=https://artificialanalysis.ai/models/claude-opus-5-5) = Artificial Analysis评估Claude Opus 5.5智能指数58，成本$5.98/任务
- Waymo Transit Rewards: fetch_url(url=https://waymo.com/blog/2026/09/transit-rewards/) = Waymo推出交通奖励计划，连接Waymo出行和公共交通

## Macro Indicators
- CPI YoY US: query_indicators(category=macro, country=us, time_range=7d) = 3.4% (2026-08-01)
- Consumer Confidence US: query_indicators(category=macro, country=us, time_range=7d) = 55.2 (2026-07-01) ⚠️过时数据
- Fed Balance Sheet: query_indicators(category=macro, country=us, time_range=7d) = 6.8万亿美元 (2026-09-16)
- PPI US: query_indicators(category=macro, country=us, time_range=7d) = 287.928 (2026-08-01)

## Calendar Events
- 首次申请失业救济人数: query_calendar_events(days=7, lookback_days=7, importance=high, country=US) = 前值19.6万，预测20.0万 (2026-09-24)
- ADP就业人数: query_calendar_events(days=7, lookback_days=7, importance=high, country=US) = 前值3.8万，预测5.8万 (2026-09-30)
- Q2 GDP终值: query_calendar_events(days=7, lookback_days=7, importance=high, country=US) = 前值1.5%，预测1.5% (2026-09-30)
- 制造业PMI初值: query_calendar_events(days=7, lookback_days=7, importance=medium, country=US) = 前值53.9，预测53.7，实际57.0 (2026-09-23)
