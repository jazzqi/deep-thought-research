# 数据来源溯源

## 行情快照
- 美国10Y国债收益率 4.63%（8月13日）: 个人记忆（Dalio 2026-08-23 上下文）
- 美国2Y国债收益率 4.15%（8月13日）: 个人记忆（Dalio 2026-08-23 上下文）
- 2s10s利差 +0.51%（8月14日）: 个人记忆（Dalio 2026-08-23 上下文）
- 美国30Y国债收益率 5.273%（8月21日），周内高点5.34%（2007年以来新高）: query_raw_items()[id:135394]
- 贝森特讲话后30Y收益率 5.227%（8月20日）: query_raw_items()[id:135276]
- 美元指数DXY 119.06（8月7日）: 个人记忆（Dalio 2026-08-23 上下文）；中信证券提及"短期内美元走弱" query_raw_items()[id:135751]
- VIX 14.63（8月13日）: 个人记忆（Dalio 2026-08-23 上下文）
- 现货黄金 >$4530/盎司（8月20日）: query_raw_items()[id:135230]
- 联邦基金利率目标区间 3.50%-3.75%（7月28-29日FOMC决议）: query_fomc() source=fomc_official
- 6月SEP联邦基金利率中值 3.8%: 个人记忆（Dalio 2026-08-23 上下文）
- 下次FOMC 9月15-16日（含SEP点阵图）: query_fomc()
- BTCUSDT 76487.7美元（8月23日）: binance_get_price(symbol=BTCUSDT)

## 本周事件日历
- 美国Q2 GDP二次估值 前值1.5% 预期1.5%（8月26日）: query_calendar_events(country=US, importance=high)
- 美国7月核心PCE环比 前值0.1% 预期0.2%（8月26日）: query_calendar_events(country=US, importance=medium)
- 美国7月核心PCE同比 前值3.3% 预期3.3%（8月26日）: query_calendar_events(country=US, importance=medium)
- 美国7月PCE同比 前值3.7% 预期3.6%（8月26日）: query_calendar_events(country=US, importance=medium)
- 美国Q2核心PCE物价指数年化季环比修正 前值3.4%（8月26日）: query_calendar_events(country=US, importance=medium)
- 美国Q2 GDP平减指数年化季环比修正 前值6.2% 预期6.2%（8月26日）: query_calendar_events(country=US, importance=medium)
- 杰克逊霍尔央行年会（8月27-29日）: query_calendar_events(country=US)
- 英伟达8月26日美股盘后公布财报: query_calendar_events(country=US)
- 中国7月规模以上工业企业利润同比 前值15.1%（8月27日）: query_calendar_events(country=CN)
- 中国1-7月规模以上工业企业利润同比 前值18.7%（8月27日）: query_calendar_events(country=CN)
- 十四届全国人大常委会第二十四次会议（8月25-28日）: query_calendar_events(country=CN)
- 日本7月CPI同比 前值1.6% 预期1.9%（8月20日）: query_calendar_events(country=JP, importance=high)
- 日本央行副行长冰见野良三讲话（8月26日）: query_calendar_events(country=JP)
- 日本8月东京CPI同比 前值2.0%（8月27日）: query_calendar_events(country=JP)
- 德国二季度GDP终值 前值0.2%环比（8月25日）: query_calendar_events(country=DE)
- 德国8月IFO商业景气指数 前值86.6（8月25日）: query_calendar_events(country=DE)
- 加拿大二季度GDP年化季环比 前值-0.1%（8月28日）: query_calendar_events(country=CA)
- 美国8月密歇根大学消费者信心指数终值 前值51.0（8月28日）: query_calendar_events(country=US)
- 美国8月芝加哥PMI 前值57.6（8月28日）: query_calendar_events(country=US)

## 重大新闻/地缘事件
- 美加贸易战升级：美国对200亿美元加拿大商品征收50%关税（8月22日生效）: query_raw_items()[id:135407][id:135408][id:135372]
- 加拿大总理卡尼宣布等额报复性关税9月8日生效，涵盖乳制品、钢铁、家电、电子产品: query_raw_items()[id:135372][id:135565]
- 美贸易代表格里尔：原本可暂缓乳制品/葡萄酒50%关税，提议钢铁降至25%铝降至25%: query_raw_items()[id:135343][id:135342]
- Fed 8月19日公布的会议纪要显示许多官员称若通胀不降可能需要加息: query_raw_items()[id:132467]
- Kevin Warsh将做为Fed主席首次在Jackson Hole演讲: query_raw_items()[id:135539]
- 旧金山联储Daly：债券市场显示对Fed政策定位的信任: query_raw_items()[id:135028]
- 贝森特：收益率未反映基本面，回购上限可能超过40亿美元: query_raw_items()[id:135320][id:135237]
- 中信证券：美国长端利率持续上行因素未根本变化: query_raw_items()[id:135751]
- NVIDIA 210亿美元SpaceX股权披露: query_raw_items()[id:128533]
- OpenAI与NVIDIA扩大计算合作（PORTS-Pike项目8GW）: query_raw_items()[id:126485]
- 阿里巴巴AI年化收入突破495亿元，云外部商业化收入增速45%: query_raw_items()[id:134673][id:134144]
- 沃尔玛Q2业绩超预期上调全年指引，但Q2同店销售增速创六年新低: query_raw_items()[id:134562]
- 瑞典央行维持利率不变，重申若伊朗战争引发通胀可能加息: query_raw_items()[id:133677]
- 石油暴利税：欧盟六国呼吁对石油公司征收暴利税: query_raw_items()[id:135718]
