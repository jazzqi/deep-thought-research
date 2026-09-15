# Reference — zhou_jintao 溯源记录

## 日历事件数据（query_calendar_events）

- 🇺🇸 美国 8月 CPI 同比 3.4%、核心 CPI 环比 0.3%（09-11）: query_calendar_events(days=14, lookback_days=14, importance=high,medium, country=US)
- 🇺🇸 美国 8月 PPI 同比 5.4%、核心 PPI 同比 4.6%（09-10）: query_calendar_events(days=14, lookback_days=14, importance=high,medium, country=US)
- 🇪🇺 ECB 主要再融资利率 2.65%（09-10）: query_calendar_events(days=14, lookback_days=14, importance=high,medium, country=EU)
- 🇨🇳 中国 8月 CPI 同比 0.8%（09-09）: query_calendar_events(days=14, lookback_days=14, importance=high,medium, country=CN)
- 🇨🇳 中国 8月 PPI 同比 3.8%（09-09）: query_calendar_events(days=14, lookback_days=14, importance=high,medium, country=CN)
- 🇨🇳 中国 1-8月社融增量 23.91 万亿（09-12）: query_calendar_events(days=14, lookback_days=14, importance=high,medium, country=CN)
- 🇨🇳 中国 M2 同比 7.5%（09-12）: query_calendar_events(days=14, lookback_days=14, importance=high,medium, country=CN)
- 🇨🇳 中国 8月贸易顺差 $1191 亿（09-08）: query_calendar_events(days=14, lookback_days=14, importance=high,medium, country=CN)
- 🇺🇸 10Y 美债拍卖 4.834%（09-09）: query_calendar_events(days=14, lookback_days=14, importance=high, country=US)
- 🇺🇸 30Y 美债拍卖 5.308%（09-10）: query_calendar_events(days=14, lookback_days=14, importance=medium, country=US)
- 🇬🇧 英国 7月 GDP 环比 +0.4%（09-11）: query_calendar_events(days=14, lookback_days=14, importance=medium, country=GB)
- 🇺🇸 密歇根消费者信心 47.8（09-11）: query_calendar_events(days=14, lookback_days=14, importance=medium, country=US)
- 🇺🇸 NFIB 小企业信心 98.7（09-08）: query_calendar_events(days=14, lookback_days=14, importance=high, country=US)
- 🇪🇺 IAEA 理事会会议（09-13）: query_calendar_events(days=14, lookback_days=14, importance=high, country=EU)

## 市场报价（market_quote）

- SPY 760.88（-0.45%）: market_quote(['SPY.US'])
- QQQ 709.18（-0.80%）: market_quote(['QQQ.US'])
- GLD 392.84（-1.49%）: market_quote(['GLD.US'])
- USO 156.66（+1.14%）: market_quote(['USO.US'])

## 新闻快讯（query_raw_items）

- 加息概率飙升至 90%: query_raw_items(keyword='CPI OR 加息 OR Fed', source='telegram:Financial_Express', published_after='2026-09-14')[id:385771] = "CPI推动市场隐含的美联储加息概率升至约90%后，花旗、高盛和摩根大通利率策略师均转而预计美联储本周可能加息"
- 汇丰转向加息: query_raw_items(keyword='汇丰 OR HSBC')[id:379560] = "汇丰预计美联储将在9月和12月分别加息25bp"
- 摩根士丹利转向加息: query_raw_items(keyword='摩根士丹利')[id:386546] = "改为预计美联储在9月和12月各加息25bp"
- 霍尔木兹海峡通行量 4 艘: query_raw_items(keyword='霍尔木兹 OR Hormuz')[id:389151] = "周一经霍尔木兹海峡通行的散货船总数为4艘，较前一日的10艘下滑"
- 伊朗击落 MQ-1 无人机: query_raw_items(keyword='伊朗 OR Hormuz')[id:389581] = "伊朗革命卫队拦截并击毁一架MQ-1无人机"
- 沙特管道关闭+油价: query_raw_items(keyword='油价 OR Brent')[id:386784] = "10年期美债收益率近三年来首次盘中升破5.0%；油价反弹、黄金下跌"
- 国内原油破 900 元: query_raw_items(keyword='原油 OR 900')[id:386540] = "国内原油期货首次升破900元/桶"
- 油轮触雷: query_raw_items(keyword='伊朗 OR 油轮')[id:386878] = "伊朗称一艘油轮触雷，霍尔木兹仍被伊管控"
- 黄金 ETF 创纪录流入: query_raw_items(keyword='黄金 OR gold')[id:386826] = "全球黄金ETF资金净流入创纪录，金价在4300美元/盎司附近"
- 沙特多城预警: query_raw_items(keyword='沙特')[id:388510] = "沙特民防部门向延布、吉达等多城发布紧急预警"
- 中金 CPI 分析: query_raw_items(keyword='中金')[id:371382] = "核心CPI环比上涨0.3%略高于预期，已触及美联储加息门槛"
- 华泰证券: query_raw_items(keyword='华泰')[id:371215] = "核心通胀环比超预期使得美联储9月加息成为必选项"
- 中信建投黄金触底: query_raw_items(keyword='中信建投')[id:373713] = "加息预期充分定价，黄金有望触底回升"
- 招商证券: query_raw_items(keyword='招商证券')[id:373056] = "宏观压制逐步落地，中期布局机会显现"
- 加拿大 CPI: query_raw_items(keyword='加拿大')[id:381556] = "加拿大8月CPI维持3%，汽油同比+22.8%"
- AI 安全呼吁: query_raw_items(keyword='AI')[id:373663] = "三大AI巨头忧心AI安全，齐声呼吁放慢先进模型开发速度"

## FOMC 日程

- query_fomc(lookback_days=120, lookahead_days=365) = 返回空（无已排会议数据）
