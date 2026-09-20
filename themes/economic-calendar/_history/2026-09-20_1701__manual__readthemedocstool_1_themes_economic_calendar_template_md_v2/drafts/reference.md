# 数据来源溯源 — W39 (2026-09-21 ~ 27) forecast

## 行情快照
- 10Y UST 1.682%: query_indicators(bond, us, 7d) [akshare, 2026-09-18]
- 2Y UST 1.2557%: query_indicators(bond, us, 7d) [akshare, 2026-09-18]
- 10Y-2Y Spread 0.4263%: query_indicators(bond, us, 7d) [akshare, 2026-09-18]
- S&P 500 7650.50: query_raw_items[427154] = 标普500指数收涨12.74点，涨幅0.17%，报7650.50点
- Dow Jones 51682.64: query_raw_items[427154] = 道琼斯工业平均指数收跌95.40点，跌幅0.18%，报51682.64点
- Nasdaq 26522.545: query_raw_items[427154] = 纳斯达克综合指数收涨104.247点，涨幅0.40%，报26522.545点
- Gold $4,377.73/oz: query_raw_items[427051] = 现货黄金涨0.83%，报4377.73美元/盎司，本周累计上涨0.68%
- Silver $66.2452/oz: query_raw_items[427051] = 现货白银涨1.57%，报66.2452美元/盎司，本周累涨2.73%
- Brent Crude ~$100/bbl: query_raw_items[427197] = 布伦特原油下跌近1%，跌破100美元/桶
- BTC $80,248.9: binance_get_ticker(BTCUSDT) = -1.38%
- ETH $2,575.17: binance_get_ticker(ETHUSDT) = -2.77%

## 美联储事件
- FOMC 9月加息25bp至3.75%-4.00%: query_calendar_events(US, high) [actual=4.0% upper]
- FedWatch 10月加息概率53.1%: query_raw_items[427116] = 美联储10月加息概率为53.1%
- 点阵图16/18官员预计年内再加一次: query_raw_items[428188] = 美联储官员普遍预计2026年仍有一次加息

## 中国市场
- LPR 1Y=3.0%, 5Y=3.5% 维持不变: query_raw_items[428205] = 1年期和5年期以上LPR保持不变
- 中国8月工业增加值+5.2%: query_calendar_events(CN) [actual=5.2, prev=4.5]
- 中国8月零售+0.4%: query_calendar_events(CN) [actual=0.4, prev=0.6]
- 中国固定资产投资-7.2%: query_calendar_events(CN) [actual=-7.2, prev=-6.7]
- 房地产投资-19.9%: query_calendar_events(CN) [actual=-19.9, prev=-19.2]
- 失业率5.3%: query_calendar_events(CN) [actual=5.3, prev=5.2]

## 中东地缘
- 胡塞-沙特冲突升级: query_raw_items[428576] = 美国驻中东多国大使馆19日发布新的安全警报
- 沙特防空告急: query_raw_items[428442] = 沙特防空拦截弹已经所剩无几
- 霍尔木兹通航改善: query_raw_items[427959] = 美军指挥官：霍尔木兹海峡石油运量创六个月新高
- 格雷厄姆制裁法案签署: query_raw_items[427848] = 美方将格雷厄姆制裁俄罗斯和伊朗法案签署成法
- 全球原油运输成本飙升: query_raw_items[427826] = 从休斯顿向亚洲运输一船原油每桶成本增加约26美元
- 法国11%加油站断供: query_raw_items[427955] = 法国目前有11%的加油站汽油或柴油断供

## 英国
- 英国8月CPI同比3.1%: query_calendar_events(GB) [actual=3.1, prev=2.9, forecast=3.1]
- 英国央行维持3.75%: query_calendar_events(GB) [actual=3.75, prev=3.75]

## 欧元区
- 欧元区8月CPI终值3.2%: query_calendar_events(EU) [actual=3.2, prev=3.3]
- 欧洲央行官员考虑10月加息: query_raw_items[427951] = 欧洲央行官员为进一步收紧货币政策铺路

## 日本
- 日本央行加息至1.25%: query_calendar_events(JP) [actual=1.25, prev=1.0]
- 日本8月CPI同比1.9%: query_calendar_events(JP) [actual=1.9, prev=1.9]

## 美国近期数据
- 8月零售+1.2% (vs +0.8%预期): query_calendar_events(US) [actual=1.2, forecast=0.8]
- 9月纽约联储制造业7.6 (vs 12.1预期): query_calendar_events(US) [actual=7.6, forecast=12.1]
- 初请失业金19.6万 (vs 20.7万预期): query_calendar_events(US) [actual=19.6, forecast=20.7]
- 8月进口价格指数+7.0%: query_calendar_events(US) [actual=7.0, prev=5.9, forecast=6.6]
- NAHB房产指数32 (vs 34预期): query_calendar_events(US) [actual=32, forecast=34]
- 费城联储制造业37.8 (vs 32.5预期): query_calendar_events(US) [actual=37.8, forecast=32.5]
- 工业产出月率0.0% (vs +0.3%预期): query_calendar_events(US) [actual=0.0, forecast=0.3]
- 制造业产出月率-0.3%: query_calendar_events(US) [actual=-0.3, prev=0.2]
- 领先指标-0.1%: query_calendar_events(US) [actual=-0.1, prev=0.2]
- 8月新屋开工127.5万户 (vs 130.9预期): query_calendar_events(US) [actual=127.5, forecast=130.9]
- 营建许可139.4万户 (vs 141.0预期): query_calendar_events(US) [actual=139.4, forecast=141.0]
- 7月外资净买入长期证券-279亿美元 (vs +1727亿前值): query_calendar_events(US) [actual=-279.0]

## 纳斯达克再平衡
- SpaceX权重升至2.82%: query_raw_items[428116] = SpaceX在该指数中的权重将升至2.82%
