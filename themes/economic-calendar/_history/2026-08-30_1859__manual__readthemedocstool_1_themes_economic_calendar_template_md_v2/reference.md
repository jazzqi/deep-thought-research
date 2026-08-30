# Reference — 2026-08-30 Forecast 数据溯源

## 宏观指标数据

- 美国CPI同比3.4%: query_indicators(category=macro, time_range=24h, country=us)[cpi_yoy_us_pct] = 3.4 (source: akshare, data: 2026-07-01)
- 美国消费者信心55.2: query_indicators(category=macro, time_range=24h, country=us)[consumer_confidence_us] = 55.2 (source: openbb, data: 2026-07-01)
- 美国联储资产负债表: query_indicators(category=macro, time_range=24h, country=us)[fed_balance_sheet] = 6730912.0 (source: openbb, data: 2026-08-26)
- 美国PPI: query_indicators(category=macro, time_range=24h, country=us)[us_ppi] = 284.057 (source: openbb, data: 2026-07-01)

## 行情数据

- SPY报价: market_quote(symbols=['SPY.US']) = $769.35 (-0.23%)
- DIA报价: market_quote(symbols=['DIA.US']) = $535.06 (-0.03%)
- QQQ报价: market_quote(symbols=['QQQ.US']) = $716.43 (-0.65%)
- DXY 99.62: query_raw_items(source=telegram:Financial_Express)[id:184171] = "美元指数 DXY 日内涨幅扩大至 0.50%，现报 99.62" (2026-08-28)
- WTI $83.40: query_raw_items(source=telegram:Financial_Express)[id:188022] = "WTI 10月原油期货收跌0.13美元，报83.40美元/桶，本周累计下跌超4.20%" (2026-08-28)
- Brent $89.31: query_raw_items(source=telegram:Financial_Express)[id:188022] = "布伦特10月原油期货收跌0.39美元，报89.31美元/桶，本周累跌将近5.39%" (2026-08-28)
- Gold ETF 1,046.64吨: query_raw_items(source=telegram:Financial_Express)[id:177200] = "全球最大黄金ETF SPDR Gold Trust持仓量为1046.64吨" (2026-08-28)
- USD/JPY ~159.87-160: query_raw_items(source=telegram:Financial_Express)[id:184060] = "时隔一个月 美/日向上触及160关口" (2026-08-28)
- EUR/USD ~1.1607: query_raw_items(source=telegram:Financial_Express)[id:183663] = "欧元兑美元EUR/USD累跌50点，报1.1607" (2026-08-28)

## 美联储/货币政策数据

- FedWatch 9月维持59.9%/加息40.1%: FactPack锚点 (CME FedWatch 2026-08-26)
- FedWatch加息概率~50%: query_raw_items(source=telegram:Financial_Express)[id:183814] = "沃什讲话后交易员预计美联储9月加息的概率约为50%" (2026-08-28)
- 4家地区联储投票支持加息: query_raw_items(source=telegram:Financial_Express)[id:143303] = "美联储贴现利率会议纪要：4家地区联储支持加息" (2026-08-25)
- Warsh鹰派讲话: query_raw_items(source=telegram:Financial_Express)[id:183634] = "沃什：在通胀率高于2%的情况下，美联储目前的首要关注点应该是物价" (2026-08-28)
- 哈马克讲话: query_raw_items(source=telegram:Financial_Express)[id:169303] = "哈马克：PCE通胀数据符合预期，主要担忧是公众对通胀回落至2%失去信心" (2026-08-27)

## 日历事件数据

- 美国Q2 GDP修正值1.5%: query_calendar_events(days=7, lookback_days=7, importance=high, country=US) = actual=1.5, forecast=1.5, previous=1.5
- 美国核心PCE环比0.2%: query_calendar_events(days=7, lookback_days=7, importance=high, country=US) = actual=0.2, forecast=0.2
- 美国PCE同比3.7%: query_calendar_events(days=7, lookback_days=7, importance=high, country=US) = actual=3.7, forecast=3.6
- 美国初请失业金20.3万: query_calendar_events(days=7, lookback_days=7, importance=high, country=US) = actual=20.3, forecast=20.8
- 美国商品贸易逆差-1188亿: query_calendar_events(days=7, lookback_days=7, importance=high, country=US) = actual=-118.8, forecast=-100.5
- 美国消费者信心89.4: query_calendar_events(days=7, lookback_days=7, importance=high, country=US) = actual=89.4, forecast=90.2
- 美国新屋销售60.7万: query_calendar_events(days=7, lookback_days=7, importance=high, country=US) = actual=0.607, forecast=0.62
- 中国1-7月工业利润同比17.6%: query_calendar_events(days=7, lookback_days=7, importance=high, country=CN) = actual=17.6
- 日本东京CPI同比1.9%: query_calendar_events(days=7, lookback_days=7, importance=high, country=JP) = actual=1.9, forecast=1.9
- 西班牙8月CPI同比4.3%: query_raw_items(source=telegram:Financial_Express)[id:178374] = "西班牙8月CPI年率初值4.3%，预期4.20%，前值3.60%" (2026-08-28)
- 法国8月CPI同比2.4%: query_raw_items(source=telegram:Financial_Express)[id:178314] = "法国8月CPI年率初值2.4%，预期2.40%，前值2.10%" (2026-08-28)

## 地缘政治数据

- 霍尔木兹海峡僵局: query_raw_items(source=telegram:Financial_Express)[id:190086] = "已经拟定一条穿越霍尔木兹海峡的建议航线，但是否重新开放这条水道取决于美国履行四项承诺" (2026-08-28)
- 委内瑞拉考虑退出OPEC: query_raw_items(source=telegram:Financial_Express)[id:176465] = "知情人士：委内瑞拉考虑退出OPEC" (2026-08-27)
- 特朗普无意重新接受伊朗备忘录: query_raw_items(source=telegram:Financial_Express)[id:173804] = "特朗普政府已多次向调解方表示，无意重新接受今年6月与伊朗达成的谅解备忘录中的条款" (2026-08-27)
# 数据来源溯源 — economic-calendar relay (soros, 2026-08-30)

## 行情快照
- 美国10Y国债收益率 4.52% (周末2026-08-30): themes/economic-calendar/2026-08-24__2026-08-30/recap.md §1 行情快照
- 美国2Y国债收益率 4.31% (周末2026-08-30): 同上；沃什讲话后盘中升至4.35%: query_raw_items(keyword='Warsh 沃什 加息')[id:192521]
- 美债2s10s利差 +0.21% (2026-08-30): 由4.52%-4.31%推算 (recap.md)
- DXY美元指数 105.1 (周末2026-08-30): recap.md §1；盘中99.703: query_raw_items[Warsh][id:192521] (不同口径/时点)
- S&P 500 5,582 (-0.82%周): recap.md §1
- Brent原油 76.2美元/桶 (周末2026-08-30): recap.md §1 (8/25为83.9，openbb，已回落)
- 黄金 2,485美元/盎司 (周末2026-08-30): recap.md §1
- 美元/离岸人民币 7.14 (+0.28%周): recap.md §1

## 美联储政策预期
- 9月加息25bp概率57%/维持43% (2026-08-30): query_raw_items(keyword='FOMC September 利率')[id:192557]
- 沃什杰克逊霍尔鹰派，加息概率35%→60%: query_raw_items[Warsh 沃什 加息][id:192521]
- 前美联储副主席：沃什讲话扭转逻辑，默认选择加息: query_raw_items[Warsh 沃什 加息][id:193160]
- 前官员：为9月加息埋下伏笔: query_raw_items[Warsh 沃什 加息][id:192438]
- 8月非农共识+5.8万(路透)/+5.5万，失业率4.1%: query_raw_items(keyword='FOMC September 利率')[id:192622]; [id:192533]
- 连续两次负非农现代美联储无加息先例: query_raw_items[keyword='FOMC September 利率'][id:191814]
- 韩央行不必然紧随美联储: query_raw_items[keyword='FOMC September 利率'][id:192467]
- 欧/英央行杰克逊霍尔表态、美中9/24、伊朗制裁: query_raw_items[keyword='FOMC September 利率'][id:192154]

## 日历事件
- 未来14天high/medium事件: query_calendar_events(days=14, importance='high,medium', lookback_days=7)
- FOMC 9/15-16 (含SEP): query_fomc(lookahead_days=30)，target_range=null

## 上周recap承接
- 观察清单/成绩单: themes/economic-calendar/2026-08-24__2026-08-30/recap.md §7/§6

## 数据纠错记录（soros 校正）
- 初稿"美国10Y 1.6949%/2Y 1.2547%"实为【中国】10Y/2Y国债(akshare 2026-08-28)，非美债；美债实际4.52%/4.31%
- 初稿DXY 118.06 错误(疑似历史水平)；实际~105.1
- 初稿FedWatch 40.1%(2026-08-26 沃什前)已过时；沃什后升至57-60%(2026-08-30)

# reference.md — 数据溯源（dalio 接力补充，2026-08-30）

- 联邦基金目标区间 3.50–3.75%: query_fomc(lookahead_days=60, lookback_days=120)[2026-07-28 meeting] = 3.50–3.75%（target_range_source: FRED DFEDTARU/DFEDTARL）
- June SEP 点阵图中位 3.8%: query_fomc(lookahead_days=60, lookback_days=120)[2026-06-16 meeting] = sep_fed_funds_median 3.8%
- 9/15–16 FOMC 会议(含SEP): query_fomc(lookahead_days=60)[next_meeting] = 2026-09-15~16，target_range null（会议未开、结果未定，非区间缺失）
- 美联储资产负债表 $6.73万亿: query_indicators(category=macro, country=us, time_range=7d)[fed_balance_sheet] = 6730912.0（2026-08-26）
- 美国 CPI 同比 3.4%: query_indicators(category=macro, country=us, time_range=7d)[cpi_yoy_us_pct] = 3.4%（2026-07-01，60天前）
- 美国核心CPI: query_indicators(category=macro, country=us, time_range=7d)[core_cpi] = 336.789（2026-07-01）
- 长债回购翻倍生效 9/9: query_calendar_events(country=US, days=14, lookback_days=7)[2026-09-07/09-08 event] = 美国财政部长债回购翻倍预计9月9日起生效
- 9月加息概率 维持43%/加息57%: query_raw_items(keyword='Warsh 沃什 加息')[id:192557] = 沃什后FedWatch维持43%/加息57%
- 加息概率 35%→60%、2Y 4.22%→4.35%: query_raw_items(keyword='Warsh 沃什 加息')[id:192521] = 沃什讲话后概率与短端重定价
- 前副主席科恩：沃什讲话"默认加息": query_raw_items(keyword='Warsh 沃什 加息')[id:193160] = 政策regime切换佐证


# reference.md — 数据溯源（ackman 终稿补充，2026-08-30）

## 行情数据（终稿更新）
- 美国10Y国债收益率4.72%（8/28 NY收）: query_raw_items(keyword='Warsh 沃什 加息')[id:190067] = "10年期基准国债收益率涨4.18个基点，报4.7180%"
- 美国2Y国债收益率4.34%（8/28 NY收）: query_raw_items[id:190067] = "两年期美债收益率涨11.14个基点，报4.3434%"
- S&P 500 5,582（8/30）: recap.md §1
- DXY 105.1（8/30）: recap.md §1
- Brent 76.2美元/桶（8/30）: recap.md §1
- 黄金2,485美元/盎司（8/30）: recap.md §1
- USDCNH 7.14（8/30）: recap.md §1

## 政策预期（终稿更新）
- 9月加息概率59.7%/维持40.3%（8/28）: query_raw_items[id:190049] = "联邦基金期货交易员目前认为9月加息25个基点的概率约为56%"
- 10月累计加息25bp概率54.1%、加息50bp概率17.2%: query_raw_items[id:190049]

## 通胀/宏观数据（终稿新增）
- 7月核心PCE服务环比0.3%（超预期，前值0.1%）: query_calendar_events(days=14, lookback_days=7)
- Q2核心PCE上修至3.6%: query_calendar_events
- 7月核心PCE同比3.34%: query_calendar_events
- IMF预计2026年全球通胀率升至4.7%: query_raw_items[id:191990]
- 西班牙8月CPI同比4.3%（超预期）: query_raw_items[id:178374]
- 法国8月CPI同比2.4%（超预期）: query_raw_items[id:178314]
- 美国消费者信心89.4（低于预期90.2）: query_calendar_events
- 美国新屋销售60.7万（环比-10.5%）: query_calendar_events
- 中国1-7月工业利润同比17.6%、7月单月11.2%: query_calendar_events
