# Reference Traceability — W38 · 2026-09-14 ~ 20

## Bond & Rates
- 10Y UST 收益率 4.9669% (9/13 收盘, +18.48bp/周): query_raw_items(id:370435)
- 2Y UST 收益率 4.6254% (9/13 收盘, +25.93bp/周): query_raw_items(id:370379)
- 10Y UST 盘中高点 4.9792%, 逼近 2023/10/23 顶部 5.0187%: query_raw_items(id:370435)
- 曲线 2s10s 收窄 3.5bp, 5s30s 收窄 1.5bp: query_raw_items(id:366960)
- 美债"扭转式趋平"(twist flattening): query_raw_items(id:366960)
- 10Y-2Y 利差 +34bp (推算): 计算值
- 日本 10Y 国债收益率 2.990% (+0.5bp): query_raw_items(id:375811)
- 30Y UST 5.38% 近二十年新高: query_raw_items(id:362972)

## Fed Policy
- CME FedWatch 9月加息概率 86.2%, 维持利率 13.8%: query_raw_items(id:373454)
- 高盛转向加息预期: query_raw_items(id:375529)
- 摩根大通 9月+12月各25bp: query_raw_items(id:376182)
- 德意志银行 9月+12月+2027年3月共3次加息: query_raw_items(id:377491)
- 巴克莱分析: query_raw_items(id:377171)
- 中金"从维护美联储信誉角度": query_raw_items(id:373765)
- 中金"加息未必是坏事": query_raw_items(id:373803)
- 特朗普反对加息: query_raw_items(id:377533)
- 美联储资产负债表 6,740,619M: query_indicators(category=macro, country=us)

## Inflation
- 美国 8月CPI同比 3.4%: query_indicators(category=macro, country=us)
- 美国 8月核心CPI环比 +0.3% (超预期 +0.2%): query_calendar_events
- 美国 8月PPI同比 5.4% (超预期 5.3%): query_calendar_events
- 美国 8月核心PPI环比 +0.2% (低于预期 +0.3%): query_calendar_events
- 中信建投"一次性服务扰动": query_raw_items(id:373659)

## Energy & Geopolitics
- 上期所原油暴涨 11%至 907 元/桶 (上市新高): query_raw_items(id:376477)
- 霍尔木兹海峡通行量个位数 (低于14艘/日均值): query_raw_items(id:375522)
- 伯恩斯坦 Brent $120-150 目标: query_raw_items(id:374084)
- 中金上调4Q26布伦特中枢至 $85: query_raw_items(id:373812)
- 柴油破 $6/加仑 (史无前例): query_raw_items(id:364017)
- 沙特管道遭袭: query_raw_items(id:373889)
- 摩根士丹利亚洲能源股上行风险: query_raw_items(id:374999)

## China
- 8月CPI同比 +0.8%: query_calendar_events
- 8月PPI同比 +3.8%: query_calendar_events
- 8月外储 3.438万亿$ (超预期): query_calendar_events
- 8月出口同比 +25.0% (美元计): query_calendar_events
- 8月进口同比 +28.2% (美元计): query_calendar_events

## Japan
- 日本 8月CPI同比 前值 1.9%: query_calendar_events
- 日本Q2 GDP终值 年化 1.4%: query_calendar_events
- 日元投机净多头 (2月以来首次): query_raw_items(id:373478)
- 日本经济2026年增长0.8% (彭博调查): query_raw_items(id:373912)

## FX & EM
- USDCNH ≈6.707: 基于roundtable数据
- 亚洲货币走软 (美元兑韩元/日元上涨0.3%): query_raw_items(id:377180)
- 新兴市场资金外流: query_raw_items(id:362673)
- 美股资金流出142亿/3周: query_raw_items(id:364685)

## Other
- 瑞银黄金观点: query_raw_items(id:376503)
- 美国预算赤字1.97万亿: query_raw_items(id:373663)
- BTC/USDT $77,553 (+0.47%): binance_get_ticker
