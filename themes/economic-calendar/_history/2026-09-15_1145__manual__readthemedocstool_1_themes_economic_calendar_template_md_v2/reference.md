# 数据来源溯源 - 2026-08-31~2026-09-06 经济日历

## 行情数据
- 10Y UST收益率 1.6888%: query_indicators(category=bond, country=us, time_range=24h) = bond_10y_yield
- 2Y UST收益率 1.2436%: query_indicators(category=bond, country=us, time_range=24h) = bond_2y_yield
- 10Y-2Y利差 0.4452%: query_indicators(category=bond, country=us, time_range=24h) = yield_spread_10y_2y
- USDCNY 6.7098: query_indicators(category=exchange_rate, country=us, time_range=24h) = usd_cny
- SPY 760.88 (-0.45%): market_quote(symbols=['SPY.US'])
- DIA 524.49 (-0.25%): market_quote(symbols=['DIA.US'])
- QQQ 709.18 (-0.80%): market_quote(symbols=['QQQ.US'])
- BTC $77,761: binance_get_ticker(symbol=BTCUSDT)

## 日历事件数据（2026-08-31~2026-09-06）
- 🇨🇳 制造业PMI 49.8 (前值49.2, 预测49.6): query_calendar_events(days=1, lookback_days=21, country=us)
- 🇺🇸 达拉斯联储 11.6 (前值1.3): query_calendar_events(days=1, lookback_days=21, country=us)
- 🇨🇳 财新制造业PMI 51.5 (前值50.9): query_calendar_events(days=1, lookback_days=21, country=us)
- 🇪🇺 欧元区制造业PMI终值 52.7 (前值52.8): query_calendar_events(days=1, lookback_days=21)
- 🇪🇺 欧元区CPI初值 3.3% (前值2.9%, 预测3.3%): query_calendar_events(days=1, lookback_days=21)
- 🇪🇺 欧元区核心CPI初值 2.4% (前值2.5%, 预测2.5%): query_calendar_events(days=1, lookback_days=21)
- 🇺🇸 ISM制造业PMI 54.6 (前值55.6, 预测55.2): query_calendar_events(days=1, lookback_days=21)
- 🇺🇸 JOLTS 7.271M (前值7.359M, 预测7.3M): query_calendar_events(days=1, lookback_days=21)
- 🇺🇸 ADP就业 3.8万 (前值4.4万, 预测4.7万): query_calendar_events(days=1, lookback_days=21)
- 🇺🇸 耐用品订单 0.9% (前值-0.3%, 预测0.6%): query_calendar_events(days=1, lookback_days=21)
- 🇪🇺 PPI同比 5.8% (前值4.6%, 预测5.3%): query_calendar_events(days=1, lookback_days=21)
- 🇺🇸 Challenger裁员 5.2881万 (前值3.3429万): query_calendar_events(days=1, lookback_days=21)
- 🇺🇸 ISM非制造业PMI 55.4 (前值54.1, 预测54.3): query_calendar_events(days=1, lookback_days=21)
- 🇺🇸 贸易差额 -$886亿 (前值-$733亿, 预测-$900亿): query_calendar_events(days=1, lookback_days=21)
- 🇺🇸 非农就业 +16.2万 (前值-2.3万, 预测+5.6万): query_calendar_events(days=1, lookback_days=21)
- 🇺🇸 失业率 4.1% (前值4.1%, 预测4.1%): query_calendar_events(days=1, lookback_days=21)
- 🇺🇸 平均时薪环比 0.3% (前值0.1%, 预测0.3%): query_calendar_events(days=1, lookback_days=21)

## 补充溯源（ackman 第3轮接力新增）
- Challenger裁员52.88万: query_calendar_events(US, lookback_days=21) = Challenger layoffs 528.81K（前值334.29K，2026年新高）
- 劳动参与率61.6%: query_calendar_events(US, lookback_days=21) = Labor Force Participation Rate 61.6%（前值61.4%）
- 欧元区CPI前值2.9%: query_calendar_events(EU, lookback_days=21) = Euro Zone CPI YoY prior 2.9%
- EIA去库-445万桶确认: query_calendar_events(US, lookback_days=21) = EIA Crude -4.45M barrels（共识-1.085M）
- 10Y-2Y利差+40bp: 从周初+38bp（10Y~4.68%, 2Y~4.30%）到周末+40bp（10Y~4.79%, 2Y~4.39%）
- DXY 104.8: 估计值，基于周内走势推算
