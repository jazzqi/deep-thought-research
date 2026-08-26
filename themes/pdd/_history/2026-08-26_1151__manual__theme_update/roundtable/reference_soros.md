# Reference Data Sources — soros relay draft

> 更新时间：2026-08-26
> 基于 index.md 已有数据 + 2026-08-26 新增查询

## Q2 2026 财报数据

- Q2 2026 营收 ¥1,124 亿 vs 预期 ¥1,152 亿（Miss -2.4%）: query_raw_items(keyword="拼多多 财报", limit=30)[id:138363]
- Q2 2026 调整后每 ADS 收益 ¥19.33 vs 预期 ¥18.51（Beat +4.4%）: query_raw_items(keyword="拼多多 财报", limit=30)[id:138363]
- Q2 2026 研发投入 ¥43 亿，同比增长 40%: query_raw_items(keyword="拼多多 财报", limit=30)[id:138470]
- Q2 营收 1123.6 亿，交易服务收入增长 13%: query_raw_items(keyword="拼多多 财报", limit=30)[id:138951]
- PDD 盘前跌 5% 后反转涨超 3%: query_raw_items(keyword="拼多多 财报", limit=30)[id:138375]
- PDD 收盘涨 2.6%: query_raw_items(keyword="拼多多 财报", limit=30)[id:138965]

## 管理层表态

- 陈磊：欧盟关税变化短期内将对跨境业务产生重大影响: query_raw_items(keyword="拼多多 Temu", limit=20)[id:138746]
- 陈磊：不会因短期波动改变全球化业务长期方向: query_raw_items(keyword="拼多多 Temu", limit=20)[id:139976]
- 陈磊：中长期将扩大本地商品供应，提升本地履约覆盖范围: query_raw_items(keyword="拼多多 Temu", limit=20)[id:138752]
- 陈磊：受影响市场跨境订单将面临较低履约效率和更高成本: query_raw_items(keyword="拼多多 Temu", limit=20)[id:138755]
- 赵佳臻：千亿扶持惠商战略逐步从投入期进入收效期: query_raw_items(keyword="拼多多 Temu", limit=20)[id:139983]
- 赵佳臻：品牌自营启动所需时间相较预期更长，但对前景有信心: query_raw_items(keyword="拼多多 Temu", limit=20)[id:139983]
- 赵佳臻：6 月份集中落地 50 余个细分领域治理方案: query_raw_items(keyword="拼多多 Temu", limit=20)[id:138725]

## 战略动向

- 多位 Temu 一二级主管转回国内做多多买菜，年营收有望超 4000 亿元: query_raw_items(keyword="拼多多 Temu", limit=20)[id:139132]
- 速卖通登顶巴西购物榜，超越 Temu，首日销售额环比 +85%: query_raw_items(keyword="Temu", limit=20)[id:140665]

## 宏观数据（中国）

- 1-7 月社零同比 +1.2%（前值 +1.3%）: query_calendar_events(country=CN, lookback_days=14)[event:1至7月社会消费品零售总额同比]
- 7 月城镇调查失业率 5.2%（前值 5.0%）: query_calendar_events(country=CN, lookback_days=14)[event:7月城镇调查失业率]
- 7 月规模以上工业增加值同比 +4.5%（前值 +5.3%）: query_calendar_events(country=CN, lookback_days=14)[event:7月规模以上工业增加值同比]
- 1-7 月固定资产投资同比 -6.7%（前值 -5.7%）: query_calendar_events(country=CN, lookback_days=14)[event:1至7月城镇固定资产投资同比]
- 1-7 月房地产开发投资 -19.2%（前值 -18.0%）: query_calendar_events(country=CN, lookback_days=14)[event:1至7月全国房地产开发投资]
- 7 月 M2 同比 +7.7%（前值 +8.0%）: query_calendar_events(country=CN, lookback_days=14)[event:7月M2货币供应同比]
- 7 月 M0 同比 +11.6%（前值 +11.8%）: query_calendar_events(country=CN, lookback_days=14)[event:7月M0货币供应同比]

## 全球贸易

- 加拿大对 700+ 种美国商品加征 50% 报复性关税: query_raw_items(limit=5)[id:143042, 142922, 142760]

## 历史数据（index.md 继承）

- FY2025: Revenue $60.53B, Net Income $13.71B, EPS $9.25: themes/pdd/index.md
- FY2024: Revenue $54.70B, Net Income $15.62B, EPS $10.56: themes/pdd/index.md
- FY2023: Revenue $34.72B, Net Income $8.42B, EPS $5.77: themes/pdd/index.md
- PE TTM current=9.81, high=12.99, low=9.81, median=10.59: themes/pdd/index.md
- Q1 2026: Revenue $15.37B vs Est $15.83B (Miss), Net Income $1.82B vs Est $3.20B (Miss 43%): themes/pdd/index.md
- Analyst rating: Buy 18, Buy 4, Hold 14, Underperform 1, Target $170.20: themes/pdd/index.md
