# Reference — BTC 主题数据溯源

> Session: 2026-08-24_1319__manual__theme_update | 最后更新: 2026-08-24 13:22 UTC

## 价格数据
- BTC当前价 $76,949（8/24 05:22 UTC）: binance_get_ticker(BTCUSDT) = 24h涨跌+1.042%，高$78,057.6，低$75,870.0
- BTC 14日K线: binance_get_klines(BTCUSDT, 1d, 14) — 8/11低$62,484 → 8/21高$79,555，约23%涨幅
- BTC 8/20暴涨超11%，创6月2日以来新高: query_raw_items(telegram:Financial_Express)[id:134385]
- BTC 8/19暴涨至$69,000，60分钟$11亿空头爆仓: query_raw_items(telegram:Financial_Express)[id:132245]
- BTC 8/20全球超18万人爆仓，超$30亿，九成为空单: query_raw_items(telegram:Financial_Express)[id:134385]

## 催化剂与重大事件
- 特朗普8/19在白宫会见Coinbase/Payward/Blockchain.com加密高管，宣布讨论"大规模"BTC储备计划: query_raw_items(telegram:Financial_Express)[id:132576]
- BTC强势反弹触发2021年以来最大规模空头平仓潮: query_raw_items(telegram:Financial_Express)[id:132941]
- 加密股8/20随BTC上涨: COIN +5.7%, Strategy +5.7%, MARA +3.8%: query_raw_items(telegram:Financial_Express)[id:135055]

## ETF资金流
- 上周13只美国BTC ETF基金净吸引$19.2亿，创去年10月以来最高纪录: query_raw_items(telegram:Financial_Express)[id:137033]
- 每个交易日均有净流入，OKX SG CEO评论可持续性问题: query_raw_items(telegram:Financial_Express)[id:137040]

## 链上数据
- 巨鲸60天内增持约4.3万枚BTC（$27.5亿），中型持有者（100-1000枚BTC）掀起买入潮: query_raw_items(telegram:Financial_Express)[id:129400]
- 巨鲸$27.5亿重返市场: query_raw_items(telegram:Financial_Express)[id:130226]
- 算力从峰值下降17%至841 EH/s，矿企转向AI基础设施: query_raw_items(longbridge)（ai_specialist引用）

## 宏观环境
- 美国CPI同比3.4%（7月数据）: query_indicators(category=macro, country=us) = cpi_yoy_us_pct 3.4 (2026-07-01)
- Fed资产负债表$6.76万亿（8/12）: query_indicators(category=macro, country=us) = fed_balance_sheet 6759955.0
- 美国消费者信心49.5（6月）: query_indicators(category=macro, country=us) = consumer_confidence_us 49.5 ⚠️
- Fed利率3.50-3.75%（7/28-29 FOMC维持不变）: query_fomc = target_range 3.50–3.75%
- 7月FOMC纪要8/19公布，多位官员认为若通胀不降需加息: 历史记忆（20小时前）
- 30年期美债收益率5.31%（8/17，19年新高）: 历史记忆（4天前）
- 10年期美债收益率4.70%（19个月新高）: 历史记忆（1分钟前）
- 美国财政部8/19宣布将10年-30年期国债流动性支持回购规模提至$40亿: 历史记忆（4天前）query_raw_items[id:131882][id:131868]
- 穆迪Zandi：伊朗战争推高长期利率，Warsh模糊前瞻指引加剧不确定性: query_raw_items(telegram:Financial_Express)[id:136671]
- 券商分析：美债利率短期三重催化（中东冲突、Warsh紧缩担忧、科技巨头发债）: query_raw_items(telegram:Financial_Express)[id:136996]

## 机构参与
- Morgan Stanley Q2增持BlackRock IBIT 23%至1650万股，增持Grayscale以太坊ETF: 历史记忆（1分钟前）query_raw_items[id:115402]
- JPMorgan Q2比特币ETF增仓25%，以太坊ETF增仓超4倍: 历史记忆（1分钟前）query_raw_items[id:114852]
- 哈佛大学13F披露持有iShare Bitcoin Trust ETF: 历史记忆（1分钟前）

## FOMC与Jackson Hole
- 9/15-16 FOMC会议含SEP（点阵图）: query_fomc = event_date 2026-09-15, sep_meeting=True
- 8/29 Jackson Hole: Fed主席Warsh首次以主席身份讲话: 历史记忆（20小时前）
- 6/16 FOMC SEP点阵图中位数3.8%: query_fomc = sep_fed_funds_median 3.8
