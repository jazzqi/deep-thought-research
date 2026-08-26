# reference.md — PDD 圆桌数据溯源记录 (Round 2 Update)
# Updated: 2026-08-26 05:27 UTC

## [NEW] Round 2 分析数据来源

### Q2 2026 财报（2026-08-24 发布，沿用前次）

- Q2 2026 营收 1,124亿元 vs 预估 1,152亿元（Miss ~2.4%）: query_raw_items(keyword="PDD OR 拼多多 OR Temu", limit=30)[id:138951]
- Q2 2026 调整后每 ADS 收益 19.33元 vs 预估 18.51元（Beat 4.4%）: query_raw_items(keyword="PDD OR 拼多多 OR Temu", limit=30)[id:138951]
- Q2 2026 交易服务收入同比增长 13%: query_raw_items(keyword="PDD OR 拼多多 OR Temu", limit=30)[id:138951]
- Q2 2026 Non-GAAP 研发投入 43亿元，同比增长 40%: query_raw_items(keyword="PDD OR 拼多多 OR Temu", limit=30)[id:138881]
- 盘前一度跌 5%，随后拉升转涨，收盘涨超 2%: query_raw_items(keyword="PDD OR 拼多多 OR Temu", limit=30)[id:138965]

### 管理层电话会关键表态（2026-08-24）

- 陈磊：欧盟关税变化短期对跨境业务产生重大影响: query_raw_items(keyword="PDD OR 拼多多 OR Temu", limit=30)[id:138746]
- 陈磊：中长期将扩大本地商品供应，提升本地履约覆盖范围: query_raw_items(keyword="PDD OR 拼多多 OR Temu", limit=30)[id:138752]
- 陈磊：不会因短期波动改变全球化业务长期方向: query_raw_items(keyword="PDD OR 拼多多 OR Temu", limit=30)[id:139976]
- 赵佳臻：品牌自营业务启动所需时间比预期更长，但对前景有信心: query_raw_items(keyword="PDD OR 拼多多 OR Temu", limit=30)[id:139983]
- 赵佳臻：平台治理常态化，6月集中落地50余个细分领域专项方案: query_raw_items(keyword="PDD OR 拼多多 OR Temu", limit=30)[id:138725]

### 竞争动态

- 速卖通8月大促首日登顶巴西购物下载榜，销售额环比涨85%，超越Temu: query_raw_items(keyword="PDD OR 拼多多 OR Temu", limit=30)[id:140665]
- 多位Temu一二级主管转回国内做多多买菜，多多买菜今年营收有望超4000亿元: query_raw_items(keyword="PDD OR 拼多多 OR Temu", limit=30)[id:139132]

### 股价与估值

- PDD 收盘价 $87.75（2026-08-25），盘后 $87.72: fetch_url(yahoo.com/quote/PDD)
- PE TTM 9.07x，EPS TTM $9.67: fetch_url(yahoo.com/quote/PDD)
- 52周区间 $71.94-$139.41: fetch_url(yahoo.com/quote/PDD)
- 分析师1Y目标价 $116.74: fetch_url(yahoo.com/quote/PDD)
- YTD -22.91%，1Y -31.56%: fetch_url(yahoo.com/quote/PDD)
- 纳斯达克金龙中国指数收涨1.11%，拼多多涨0.78%（2026-08-25）: query_raw_items(keyword="PDD OR 拼多多 OR Temu", limit=30)[id:143340]

### 年度财务数据（沿用前次）

- FY2025: Revenue $60.53B, Op Income $13.05B, Net Income $13.71B, EPS $9.25
- FY2024: Revenue $54.70B, Op Income $15.06B, Net Income $15.62B, EPS $10.56
- FY2025 营收增速 10.6%，净利润 -12.2% YoY
- FY2025 D/E 0.52, Operating CF $14.99B, Free CF $12.00B

### Q1 2026 实际（沿用前次）

- Q1 2026 Revenue $15.37B vs Est $15.83B (Miss -2.9%)
- Q1 2026 Net Income $1.82B vs Est $3.20B (Miss -43.2%)

### 中国宏观数据（沿用前次）

- 1-7月社会消费品零售总额同比 +1.2%
- 制造业 PMI 49.2 / 非制造业 PMI 49.0（2026年7月）
- 8月LPR 1Y=3.0%、5Y=3.5% 不变


## [Round 2] soros 接力补充数据来源

### 新闻类数据（query_raw_items）

- ECB Schnabel称利率必须进一步上升: query_raw_items(keyword="EU tariff OR Temu regulation OR EU FSR OR de minimis", limit=15)[id:144179]
- Shein港股IPO簿记全额认购（最高$18亿）: query_raw_items(keyword="Shein OR 速卖通 OR AliExpress OR 跨境电商", limit=15)[id:140644]
- Shein以~$27B估值港股上市，9/1开始交易: query_raw_items(keyword="Shein OR 速卖通 OR AliExpress OR 跨境电商", limit=15)[id:136844]
- 美国国会"中国委员会"批评摩根大通等参与Shein IPO: query_raw_items(keyword="Shein OR 速卖通 OR AliExpress OR 跨境电商", limit=15)[id:142966]
- Shein配合FTC调查美国业务运营: query_raw_items(keyword="Shein OR 速卖通 OR AliExpress OR 跨境电商", limit=15)[id:136205]
- TikTok Shop与米奥会展举办AI出海大会: query_raw_items(keyword="Shein OR 速卖通 OR AliExpress OR 跨境电商", limit=15)[id:140696]

### 股价数据（fetch_url）

- PDD 收盘价 $87.75，盘后 $87.72: fetch_url(yahoo.com/quote/PDD)
- PE TTM 9.07x，EPS TTM $9.67: fetch_url(yahoo.com/quote/PDD)
- 市值 $124.9B: fetch_url(yahoo.com/quote/PDD)
- 52周区间 $71.94-$139.41: fetch_url(yahoo.com/quote/PDD)
- 分析师1Y目标价 $116.74: fetch_url(yahoo.com/quote/PDD)
- YTD -22.91%，1Y -31.56%: fetch_url(yahoo.com/quote/PDD)

### 宏观/日历数据（query_calendar_events）

- 8月LPR 1Y=3.0%，5Y=3.5%不变（2026-08-20）: query_calendar_events(country=CN, days=14)
- 7月规模以上工业企业利润同比（前值15.1%，8/27公布）: query_calendar_events(country=CN, days=14)
- 8月MLF净回笼1000亿元: query_raw_items(keyword="PDD", limit=30)[id:139823]

### 市场指数

- 纳斯达克金龙中国指数收涨1.11%（2026-08-25）: query_raw_items(keyword="PDD", limit=30)[id:143340]


## [Review] lynch 交叉审查独立数据核验（2026-08-26）

### 核验使用数据源

- Q2 财报核心数据核验: query_raw_items(keyword="PDD OR 拼多多 OR Temu", limit=30)[id:138363] = 营收1,124亿, 预估1,152亿; 调整后每ADS 19.33元, 预估18.51元
- Q2 营收1123.6亿/交易服务+13%: query_raw_items(keyword="PDD OR 拼多多 OR Temu", limit=30)[id:138951] = Q2营收1123.6亿，交易服务收入增长13%
- 盘前-5%逆转: query_raw_items(keyword="PDD OR 拼多多 OR Temu", limit=30)[id:138362] = 盘前下跌5%; [id:138375] = 盘前走低后迅速拉升，现涨超3%
- 收盘涨2.6%: query_raw_items(keyword="PDD OR 拼多多 OR Temu", limit=30)[id:138965] = 股价上涨2.6%
- 陈磊EU关税表态: query_raw_items(keyword="PDD OR 拼多多 OR Temu", limit=30)[id:138746] = "预计欧盟关税的变化短期内将对我们的跨境业务产生重大影响"
- 陈磊短期影响: query_raw_items(keyword="PDD OR 拼多多 OR Temu", limit=30)[id:138755] = "短期内，受影响市场的跨境订单将面临较低的履约效率和更高的成本"
- 陈磊中长期策略: query_raw_items(keyword="PDD OR 拼多多 Temu", limit=30)[id:138752] = "中长期来看，将扩大本地商品供应，并提升本地履约覆盖范围"
- 陈磊长期方向: query_raw_items(keyword="PDD OR 拼多多 OR Temu", limit=30)[id:139976] = "不会因短期波动改变全球化业务长期方向"
- 赵佳臻自营: query_raw_items(keyword="PDD OR 拼多多 OR Temu", limit=30)[id:139983] = "启动所需时间相较预期更长，但对前景有信心"
- 赵佳臻治理: query_raw_items(keyword="PDD OR 拼多多 OR Temu", limit=30)[id:138725] = 6月集中落地50余个细分领域专项方案
- 多位Temu主管转做多多买菜: query_raw_items(keyword="PDD OR 拼多多 OR Temu", limit=30)[id:139132] = 多位Temu一二级主管转回国内做多多买菜，多多买菜今年营收有望超4000亿元
- 速卖通巴西: query_raw_items(keyword="PDD OR 拼多多 OR Temu", limit=30)[id:140665] = 速卖通登顶巴西购物下载榜，超越Temu等，首日销售额环比涨85%
- R&D投入: query_raw_items(keyword="PDD OR 拼多多 OR Temu", limit=30)[id:138470] = 二季度营收1124亿元，Non-GAAP研发投入43亿元，同比增长40%



## [Review] lynch 交叉审查独立数据来源 (2026-08-26 05:40 UTC)

### PDD 新闻独立核验（query_raw_items）

- Q2 营收1,124亿 vs预估1,152亿（miss ~2.4%）：query_raw_items(keyword="PDD OR 拼多多 OR Temu", limit=30)[id:138363]
- Q2 调整后EPS 19.33 vs预估18.51（beat 4.4%）：query_raw_items(keyword="PDD OR 拼多多 OR Temu", limit=30)[id:138363]
- Q2 交易服务收入增长13%：query_raw_items(keyword="PDD OR 拼多多 OR Temu", limit=30)[id:138951]
- Non-GAAP研发投入43亿，同比+40%：query_raw_items(keyword="PDD OR 拼多多 OR Temu", limit=30)[id:138470]
- 盘前跌5%逆转收涨超2%：query_raw_items(keyword="PDD OR 拼多多 OR Temu", limit=30)[id:138362][id:138375][id:138965]
- 陈磊EU关税重大影响表态：query_raw_items(keyword="PDD OR 拼多多 OR Temu", limit=30)[id:138746][id:138752][id:139976]
- 赵佳臻自营业务进展：query_raw_items(keyword="PDD OR 拼多多 OR Temu", limit=30)[id:139983]
- Temu主管转调多多买菜（营收超4000亿）：query_raw_items(keyword="PDD OR 拼多多 OR Temu", limit=30)[id:139132]
- 速卖通登顶巴西购物榜（环比涨85%）：query_raw_items(keyword="PDD OR 拼多多 OR Temu", limit=30)[id:140665]
- 纳斯达克金龙中国指数+1.11%，拼多多+0.78%（2026-08-25）：query_raw_items(keyword="PDD OR 拼多多 OR Temu", limit=30)[id:143340]
- MLF净回笼1000亿（近四月首次缩量）：query_raw_items(keyword="PDD OR 拼多多 OR Temu", limit=30)[id:139823]

### 竞争对手事件（query_raw_items）——文档遗漏

- Shein港股IPO~$27B估值，9/1上市：query_raw_items(keyword="Shein OR 速卖通 OR AliExpress OR 跨境电商", limit=20)[id:136844]
- Shein IPO簿记全额认购（最高$18亿）：query_raw_items(keyword="Shein OR 速卖通 OR AliExpress OR 跨境电商", limit=20)[id:140644]
- Shein配合FTC调查美国业务：query_raw_items(keyword="Shein OR 速卖通 OR AliExpress OR 跨境电商", limit=20)[id:136205]
- 美国国会中国委员会批评银行参与Shein IPO：query_raw_items(keyword="Shein OR 速卖通 OR AliExpress OR 跨境电商", limit=20)[id:142966]

### 宏观数据核验

- 制造业PMI 49.2 / 非制造业PMI 49.0（2026年7月）：query_indicators(category=pmi, country=china, time_range=7d)
- 7月规模以上工业企业利润同比（前值15.1%，8/27公布）：query_calendar_events(country=CN, days=14, importance=high)
