# 数据来源追溯（reference.md）

## 行情数据
- 10Y UST 4.63%（08-13）: query_indicators(category='bond', country='us', time_range='24h', limit=10)
- 2Y UST 4.15%（08-13）: query_indicators(category='bond', country='us', time_range='24h', limit=10)
- 30Y UST 5.31%（08-17）: query_raw_items(id:131882, 131868, 132047) - 美国财政部提高国债回购规模
- DXY 98.84（08-20）: query_raw_items(id:135298) - Bloomberg Economics
- VIX 14.63（08-13）: query_indicators(category='sentiment', country='us', time_range='24h', limit=10)
- Brent ~$94/桶（08-20）: query_raw_items(id:134602) - Financial_Express
- WTI ~$87/桶（08-20）: query_raw_items(id:134602) - Financial_Express
- Gold $4,530/oz（08-20）: query_raw_items(id:135230) - Financial_Express

## 日历事件数据
- 美国 7 月 PCE 物价指数（08-26）: query_calendar_events(country='US', days=10, importance='high,medium', limit=50)
- 美国 Q2 GDP 修正值（08-26）: query_calendar_events(country='US', days=10, importance='high,medium', limit=50)
- 英伟达财报（08-26 盘后）: query_calendar_events(country='US', days=10, importance='high,medium', limit=50)
- 加拿大 Q2 GDP（08-28）: query_calendar_events(country='CA', days=10, importance='high,medium', limit=50)
- 日本东京 CPI（08-27）: query_calendar_events(country='JP', days=10, importance='high,medium', limit=50)
- 中国 7 月工业利润（08-27）: query_calendar_events(country='CN', days=10, importance='high,medium', limit=50)
- 中国 8 月官方 PMI（08-31）: query_calendar_events(country='CN', days=10, importance='high,medium', limit=50)

## 宏观指标
- FOMC 利率决议（2026-04-28 至 2026-07-28）: query_fomc(lookback_days=120, lookahead_days=365, limit=10)
- 联邦基金利率 3.50-3.75%: query_fomc() - FRED (DFEDTARU/DFEDTARL)
- 美国政府债务 40.05 万亿美元: query_raw_items(id:134718) - Financial_Express

## 新闻条目引用
- Kevin Warsh Jackson Hole 演讲: query_raw_items(id:135539) - Bloomberg Economics
- 加拿大报复性关税: query_raw_items(id:135565, 135528, 135544) - AlJazeera, NYT
- 霍尔木兹海峡通行状况: query_raw_items(id:135349, 135355, 135631) - Financial_Express
- JPMorgan 警告美债回购治标不治本: query_raw_items(id:133493) - Financial_Express
- AI 投资热潮史上最大资本开支: query_raw_items(id:134684) - Financial_Express
- 谘商会 GDP 预测 1.9%: query_raw_items(id:135112) - Financial_Express
- 英伟达信用评级确认: query_raw_items(id:129644, 129189) - Bloomberg Economics
- 英伟达投资 Mercor: query_raw_items(id:132423) - Financial_Express
- 全球粮食供应链冲击: query_raw_items(id:135770) - NYT World
- 瑞士与中国贸易协定: query_raw_items(id:135295) - Bloomberg Economics

## 工具查询记录
- query_calendar_events: 覆盖 US/CN/EU/JP/GB/CA 共 200+ 条事件
- query_fomc: 6 次 FOMC 会议数据（2026-04 至 2026-12）
- query_indicators: 美国国债/CPI/消费者信心等宏观指标
- query_raw_items: Financial_Express、Bloomberg Economics、NYT、AlJazeera、BBC 等源
