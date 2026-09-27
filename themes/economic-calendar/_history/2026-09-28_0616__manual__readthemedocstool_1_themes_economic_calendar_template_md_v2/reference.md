# 数据来源溯源（reference.md）

## 行情与资产价格
- BTCUSDT: binance_get_ticker(symbol=BTCUSDT) = $84,111.5 (2026-09-27)
- S&P 500 near ATH: query_raw_items(keyword='S&P 500', source='telegram:Financial_Express')[id:432448] = 标普500收涨114.20点至7764.70点（2026-09-21）
- 半导体指数周涨6.4%: query_raw_items(keyword='S&P 500', source='telegram:Financial_Express')[id:444660] = 半导体指数累涨6.4%

## 美联储
- FOMC 9月加息25bp至3.75-4.00%: query_fomc(lookahead_days=365) + query_calendar_events(country='US') = 目标利率上限4.00%（2026-09-16公布）
- 下次FOMC会议: 2026-10-27（无SEP/无发布会）
- 美联储拟提高银行监管门槛: query_raw_items(keyword='Fed', source='telegram:Financial_Express')[id:443919] = 美联储拟提高触发更严格监管的资产门槛（2026-09-25）
- 机构：美联储加息意味债券收益率将维持高位: query_raw_items(keyword='Fed', source='telegram:Financial_Express')[id:441799] = Federated Hermes策略师称利率水平已明显上升（2026-09-24）

## 美国经济数据
- ISM非制造业PMI 8月: 55.4（前值54.1，超预期54.1）: query_raw_items(keyword='ISM', source='telegram:Financial_Express')[id:270896] = 55.4, 预期54.3, 前值54.1（2026-09-03）
- ISM非制造业新订单: 60.9（前值57.2）: query_raw_items(keyword='ISM', source='telegram:Financial_Express')[id:270898]
- ISM非制造业就业: 47.8（前值47.4）: query_raw_items(keyword='ISM', source='telegram:Financial_Express')[id:270899]
- ISM非制造业物价: 72.6（前值70.3）: query_raw_items(keyword='ISM', source='telegram:Financial_Express')[id:270900]
- ISM非制造业库存: 56.7（前值51.4）: query_raw_items(keyword='ISM', source='telegram:Financial_Express')[id:270905]
- ISM非制造业供应商交付: 51.3（前值52.8）: query_raw_items(keyword='ISM', source='telegram:Financial_Express')[id:270906]
- 首次申请失业救济人数（9/12当周）: 19.6万人（前值20.6万，预期20.8万）: query_calendar_events(country='US')
- 续请失业救济人数（9/5当周）: 173.0万人（前值177.4万）: query_calendar_events(country='US')
- 10Y UST收益率: query_raw_items(keyword='ISM', source='telegram:Financial_Express')[id:270913] = 4.754%（2026-09-03）

## 中国经济数据
- M2同比 8月: 7.5%（前值7.7%）: query_calendar_events(country='CN')
- 新增人民币贷款 8月: 600亿（前值-3400亿）: query_calendar_events(country='CN')
- 社会融资规模（1-8月）: 239100亿元（前值222500亿）: query_calendar_events(country='CN')
- 规模以上工业增加值 8月: 5.2%（前值4.5%，超预期4.8%）: query_calendar_events(country='CN')
- 社零 8月: 0.4%同比（前值0.6%，不及预期0.8%）: query_calendar_events(country='CN')
- 固定资产投资（1-8月）: -7.2%同比（前值-6.7%）: query_calendar_events(country='CN')
- 房地产投资（1-8月）: -19.9%（前值-19.2%）: query_calendar_events(country='CN')
- 城镇调查失业率 8月: 5.3%（前值5.2%）: query_calendar_events(country='CN')

## 日本经济数据
- 日本央行加息至1.25%（2026-09-18）: query_calendar_events(country='JP')
- 日本CPI 8月: 1.9%同比（核心1.7%）: query_calendar_events(country='JP')
- 日本贸易收支 8月: -11056亿日元: query_calendar_events(country='JP')

## 欧洲经济数据
- 欧元区制造业PMI 9月初值: 52.7（前值52.7）: query_calendar_events(country='EU')
- 欧元区ZEW经济景气 9月: 25.8（前值31.4）: query_calendar_events(country='EU')
- 德国ZEW经济景气 9月: 34.7（前值34.2）: query_calendar_events(country='EU')
- 英国央行维持3.75%利率不变: query_calendar_events(country='GB')

## 本周日历事件（10月5-11日）
- ISM非制造业指数 9月（10/5）: query_calendar_events(country='US', days=30)
- 中国外汇储备 9月（10/6-7）: query_calendar_events(country='CN', days=30)
- 首次申请失业救济人数（10/3当周）（10/8）: query_calendar_events(country='US', days=30)
- M2货币供应同比 9月（10/8）: query_calendar_events(country='CN', days=30)
- 社会融资规模增量 1-9月（10/8）: query_calendar_events(country='CN', days=30)
- 新增人民币贷款 1-9月（10/8）: query_calendar_events(country='CN', days=30)
- EU/UK/Japan PMI终值 9月（10/5）: query_calendar_events(country='EU,GB,JP', days=30)
- EU Sentix投资者信心 10月（10/5）: query_calendar_events(country='EU', days=30)
- EU PPI 8月（10/5）: query_calendar_events(country='EU', days=30)
- EU零售销售 8月（10/6）: query_calendar_events(country='EU', days=30)
- 日本贸易收支 8月（10/7）: query_calendar_events(country='JP', days=30)
