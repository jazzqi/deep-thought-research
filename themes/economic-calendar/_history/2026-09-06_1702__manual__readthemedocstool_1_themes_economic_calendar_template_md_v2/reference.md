# 数据来源追踪（2026-09-07 ~ 2026-09-13 forecast）

## 行情数据
- SPY.US: market_quote(symbols=['SPY.US']) = 770.19 (-0.39%)
- GLD.US: market_quote(symbols=['GLD.US']) = 406.77 (-0.84%)
- UUP.US: market_quote(symbols=['UUP.US']) = 28.08 (+0.25%)
- USO.US: market_quote(symbols=['USO.US']) = 141.96 (-0.09%)
- FXI.US: market_quote(symbols=['FXI.US']) = 35.88 (+1.53%)
- EEM.US: market_quote(symbols=['EEM.US']) = 68.70 (+1.82%)

## 宏观指标
- CPI同比(US) 3.4%: query_indicators(category='macro', country='us') = cpi_yoy_us_pct
- Fed资产负债表 67372亿美元: query_indicators(category='macro', country='us') = fed_balance_sheet
- PPI(US) 284.057: query_indicators(category='macro', country='us') = us_ppi

## FOMC
- 当前利率区间 3.50-3.75%: query_fomc(lookback_days=120, lookahead_days=120) = 2026-06-16/07-28决议
- 下次会议 2026-09-15: query_fomc() = FOMC会议（September 2026），SEP会议
- FedWatch 维持59.9% / 加息40.1%: FactPack系统只读锚点(2026-08-26)

## 新闻
- 美银预测核心CPI 0.22%年率3.4%支持加息: query_raw_items(keyword='Fed OR inflation', limit=20)[id:295429]
- 花旗预测核心CPI 0.184%年率2.3%: query_raw_items(keyword='Fed OR inflation', limit=20)[id:295429]
- 特朗普政府施压沃什要求降息: query_raw_items(keyword='Fed OR inflation', limit=20)[id:295025]
- ADP就业38万低于预期48万: query_calendar_events(days=14, importance=high) = ADP非农就业(8月)
- ISM制造业54.6(前值55.6): query_calendar_events(days=14, importance=high) = ISM制造业PMI(8月)
- ISM非制造业55.4(前值54.1): query_calendar_events(days=14, importance=high) = ISM非制造业PMI(8月)
- JOLTS职位空缺727.1万(前值735.9万): query_calendar_events(days=14, importance=high) = JOLTS
- EIA原油库存变动-445万桶: query_calendar_events(days=14, importance=high) = EIA原油库存

## 日历事件
- 8月非农(US): query_calendar_events(days=14, importance=high) = 失业率4.1%(持平)
- 欧元区CPI初值3.3%(前值2.9%): query_calendar_events(days=14, importance=high) = Euro Zone CPI
- 欧元区核心CPI初值2.4%(前值2.5%): query_calendar_events(days=14, importance=high) = Euro Zone core CPI
- 中国制造业PMI 49.8(前值49.2): query_calendar_events(days=14, importance=high) = China NBS PMI
- 中国财新制造业PMI 51.5(前值50.9): query_calendar_events(days=14, importance=high) = China RatingDog PMI
