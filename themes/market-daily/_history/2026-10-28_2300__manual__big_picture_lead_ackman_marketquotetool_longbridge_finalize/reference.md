# 2026-10-28 数据来源溯源（ackman lead）

## 行情（US 开盘确认，~15:00 UTC 快照）
- SPY 实时报价: market_quote(symbols=['SPY.US']) = last 770.36 / prev 769.66 / +0.09%（量 556.04 万，额 42.85 亿美元）
- QQQ 实时报价: market_quote(symbols=['QQQ.US']) = last 721.45 / prev 721.25 / +0.03%
- NVDA 实时报价: market_quote(symbols=['NVDA.US']) = last 217.69 / prev 217.94 / -0.11%
- BTC 现价: binance_get_ticker('BTCUSDT') = 80,642.3 美元，24h +0.23%，24h 高 81,800 / 低 80,206.7，24h 成交额约 90.06 亿美元

## 大宗与利率定价
- WTI/布伦特盘前报价: query_raw_items(keyword='美联储 OR FOMC OR 沃什')[id:585735] = 原油涨 2.01% 报 101.91 美元/桶；布伦特涨 1.81% 报 111.39 美元/桶
- 10月 FOMC 维持利率不变概率: query_raw_items[ id:585735] = CME 美联储观察 90.6%
- Kalshi 预测市场暂停概率: query_raw_items[ id:585498] = 95%
- 周四加息概率: query_raw_items[ id:583143] = 仅 7%，市场预期"鹰派暂停"、2-3 票异议
- 联邦基金目标区间: query_raw_items[ id:586850] = 3.75%-4.00%（9月 CPI/PPI 均超预期但官员不急于加息）
- SOFR/EFFR: query_raw_items[ id:586869] = SOFR 3.95%（前 3.93%），有效联邦基金利率 3.88%（持平）
- JPM 10Y 峰值预测: query_raw_items[ id:580851] = 预计 12 月+2027Q1 加息，10Y 从略高于 5% 升至 2027 年中 5.25%-5.5% 峰值，黄金承压

## 央行与地缘
- 加拿大央行加息 25bp 至 2.50%（"预防性"）: query_raw_items[ id:587993] = 汇丰前首席经济学家批评"缺乏魄力"；市场定价至 2027年9月累计加息 100bp [id:585043]
- 加央行行长麦克勒姆: query_raw_items[ id:587983/587985] = "通胀看起来不太可能得到良好控制""通胀得到控制的可能性降低"
- 美军海湾航行警告: query_raw_items[ id:585735] = 阿曼湾-霍尔木兹海峡港口间航行船只应避开相关海域
- EIA 美国原油产量: query_raw_items[ id:587988] = 最近一周升至纪录高位
- 新兴市场货币: query_raw_items[ id:587521] = 巴西雷亚尔、墨西哥比索刷新日低，油价与美债收益率走高，等待 FOMC
- 以色列大选僵局: query_raw_items[ id:587982] = TA-35 盘中约 -3%，谢克尔兑美元 -2.3% 至 3.1230
- 乌克兰三方会谈: query_raw_items[ id:587986] = 泽连斯基预计 11月10日前举行（阿布扎比等地点 [id:587999]）
- 亚丁机场遭袭: query_raw_items[ id:587995] = 数日内累计 6 次遭胡塞武装袭击

## 财报/事件日历
- 周三关键事件: query_raw_items[ id:576632] = FOMC 决议+沃什发布会、盘后 MSFT/GOOG 等巨头财报、苹果新品发布会
- 财政部短债依赖: query_raw_items[ id:586298] = JPM：私人持有短债 2026 年 +4010 亿美元、2027 年 +9910 亿美元，为 2023 年以来最密集
- 礼来 retatrutide: query_raw_items[ id:588013] = 血糖控制优于 Ozempic、减重效果两倍多
- 黄金 ETF: query_raw_items[ id:586421] = 9月以来国内黄金类 ETF 规模缩水超 180 亿元，10/29 凌晨 FOMC+GDP+PCE 共同决定金价方向

- 美股实时报价（2026-10-28 ~15:36 UTC）: market_quote(symbols=SPY,QQQ,MSFT,META,MU,NVDA,AAPL,GOOGL.US) = SPY 771.18 (+0.20%)、QQQ 722.07 (+0.11%)、MSFT 528.32 (-0.57%)、META 612.66 (-1.21%)、MU 970.34 (+4.48%)、NVDA 217.44 (-0.23%)、AAPL 345.27 (-0.53%)、GOOGL 323.69 (+0.97%)
- BTC 24h 行情: binance_get_ticker(BTCUSDT) = 80543.2 美元（24h +0.07%，最高 81800.0、最低 80387.9，2026-10-28）
- 未来 7 日高/中重要性宏观日历: query_calendar_events(days=7, importance=high,medium, lookback_days=1) = 10/29 12:30 美 Q3 GDP 年化季环比初值（前值 2.2、预期 3.0）、10/29 12:30 初请（前值 19.4 万）、10/29 13:15 ECB 存款便利利率（前值 2.5、预期维持）、10/31 16:00 OPEC+ 会议、11/1 06:00 北美冬令时、11/1 00:00 韩国 10 月出口（前值 +83.5%）、11/2 15:00 美 ISM 制造业（前值 54.5）
- 10/28 加拿大央行利率决议: query_calendar_events(days=7) = 10/28 13:45 UTC 隔夜贷款利率，前值 2.25（实际加息至 2.50 见 [id:586873]）
- PIMCO 减持 AI 融资仓位: query_raw_items(published_after=2026-10-28T12:00:00Z)[id:589075] = PIMCO 在 AI 债券融资热潮中获利了结，显著减持 Meta 与 Oracle 仓位各约一半
- TTF 天然气触及 100 欧元: query_raw_items(published_after=2026-10-28T12:00:00Z)[id:588575] = 荷兰天然气价格因胡塞袭击与 QatarEnergy 不可抗力触及 100 欧元/兆瓦时
- 美国设备部门再裁员: query_raw_items(published_after=2026-10-28T12:00:00Z)[id:588577] = Amazon 在产品发布潮后削减设备部门更多岗位
- A 股放量反弹: query_raw_items(published_after=2026-10-28T12:00:00Z)[id:589068] = 10/28 A 股放量反弹，成交 1.6423 万亿元
- NVIDIA 边缘 AI 铺货: query_raw_items(published_after=2026-10-28T12:00:00Z)[id:589081][id:589082][id:589083] = DGX Spark 64GB 开售、RTX Spark 笔记本 2599 美元起、六大 OEM 铺货

- 美股盘中最新报价: market_quote(MSFT.US,GOOGL.US,META.US,SMH.US,MU.US) = SMH 565.18(+1.29%)/MU 973.00(+4.76%)/MSFT 528.30(-0.57%)/GOOGL 323.81(+1.01%)/META 613.25(-1.12%)（10/28 盘中）
- SK海力士Q3营收/营业利润超预期、美股存储股普涨: query_raw_items(keyword='Microsoft OR 微软 earnings OR Azure')[id:587402] = SK Hynix Q3 超预期，美股存储股普涨、SK海力士相关标的盘中涨近10%
- SK海力士产能售罄至2029年: query_raw_items(keyword='Fed OR 美联储 OR 利率',published_after='2026-10-28T18:00:00Z')[id:586216] = SK Hynix 记录级季度业绩、产能售罄至 2029，NVDA 计划扩产
- FOMC预期2-3票异议(Hammack/Logan可能反对): query_raw_items(keyword='FOMC OR Warsh OR 沃什 OR 美联储')[id:583143] = 10/29凌晨加息概率仅7%，鹰派暂停下预计2-3票异议
- 官员异议渠道判断(哈马克/洛根或投反对票): query_raw_items(keyword='FOMC OR Warsh OR 沃什 OR 美联储')[id:586850] = 分析师称市场预计美联储维持利率不变，通胀压力仍存
- Kalshi 维持利率概率95%: query_raw_items(keyword='FOMC OR Warsh OR 沃什 OR 美联储')[id:585498] = Kalshi 预测市场显示美联储维持当前利率概率 95%
- MUFG：鹰派暂停则12月加息概率或>80%: query_raw_items(keyword='FOMC OR Warsh OR 沃什 OR 美联储')[id:581305] = 三菱日联称若10月FOMC鹰派暂停，12月加息概率有望升至80%以上
- BMO：预期鹰派暂停+数名官员异议: query_raw_items(keyword='FOMC OR Warsh OR 沃什 OR 美联储')[id:580816] = BMO 预计信号鹰派暂停，发布会可能有数名官员异议
- 盘前油价 WTI 101.91/布伦特 111.39 美元: query_raw_items(keyword='FOMC OR Warsh OR 沃什 OR 美联储')[id:585735] = 美股盘前要闻速递，原油涨2.01%至101.91、布伦特111.39
- 油价涨破110美元成FOMC焦点: query_raw_items(keyword='FOMC OR Warsh OR 沃什 OR 美联储')[id:586831] = Fed决策前瞻，地缘紧张下油价升破110美元/桶
- AI泡沫对冲ETF（不做空英伟达）: query_raw_items(limit=50)[id:589134] = Bloomberg Balchunas 提示5只可防AI估值回调的对冲ETF
- 巨头发债资金沉淀货基回流美债: query_raw_items(keyword='Microsoft OR 微软 earnings OR Azure')[id:587411] = Federated Hermes Cunningham：大科技发债资金入货基再买美债、未挤占国债需求
- 美Q3 GDP初值+初请: query_calendar_events(days=7,lookback_days=1) = 10/29 12:30 UTC GDP 预期3.0/前值2.2年化；初请前值19.4万
- ECB议息: query_calendar_events(days=7,lookback_days=1) = 10/29 13:15 UTC 存款利率前值2.5%（预期不变）
- OPEC+会议: query_calendar_events(days=7,lookback_days=1) = 10/31 16:00 UTC
- 苹果10月第二场发布会: query_calendar_events(days=7,lookback_days=1) = 10/28 17:00 UTC 首款触控MacBook与新iPad mini
- SK海力士三季报电话会: query_calendar_events(days=7,lookback_days=1) = 10/28 00:00 UTC
- 北美冬令时/韩国10月出口: query_calendar_events(days=7,lookback_days=1) = 11/1 冬令时生效；韩国出口前值+83.5%

- 最新盘面 10/28 15:44 UTC: market_quote(SPY,QQQ,MU,MSFT,GOOGL,META,NVDA,SMH,AAPL,TSLA) = SPY 771.45 +0.23% / QQQ 722.47 +0.17% / MU 972.24 +4.68% / SMH 565.29 +1.31% / META 613.60 -1.06% / MSFT 527.49 -0.72% / GOOGL 323.76 +0.99% / NVDA 217.67 -0.12% / AAPL 345.24 -0.54% / TSLA 401.84 -1.38%
- WTI 日内 +3% 至 102.91 美元/桶（FOMC 前 2 小时加速）: query_raw_items(source=telegram:Financial_Express)[id:589152] = WTI 原油日内涨幅达 3.0%，报 102.91 美元/桶
- WTI 日内 +3% 现报 102.90 美元/桶: query_raw_items(source=telegram:Financial_Express)[id:589149] = WTI 原油日内涨 3%，现报 102.90 美元/桶
- 以色列大选特殊选票 43–48 万张: query_raw_items(source=telegram:Financial_Express)[id:589155] = 以选举委员会预计双层信封特殊选票 43 万至 48 万张，少于此前报道的约 60 万张，或将影响最终大选格局
- PIMCO 减持 Meta 与 Oracle 各约一半: query_raw_items(keyword=Fed OR 沃什 OR Warsh OR FOMC)[id:589075] = 债券巨头 PIMCO 在 AI 债务融资热潮中获利了结，大幅减持 Meta 与 Oracle 仓位各约一半
- 美银客户两周净卖出 185 亿美元美股: query_raw_items(published_after=2026-10-28T10:00:00Z)[id:587975] = 美银客户上周净卖出 35 亿美元美股，前周流出 150 亿美元
- 5 只 AI 泡沫对冲 ETF: query_raw_items(published_after=2026-10-28T10:00:00Z)[id:589134] = Bloomberg Balchunas 提示 5 只不做空英伟达也能防 AI 泡沫的对冲 ETF
- TTF 天然气触及 100 欧元/兆瓦时: query_raw_items(published_after=2026-10-28T10:00:00Z)[id:588575] = 胡塞袭击 + QatarEnergy 不可抗力，荷兰天然气价格触及 100 欧元/兆瓦时
- 加拿大央行加息 25bp 至 2.50%: query_raw_items(keyword=Fed OR 沃什 OR Warsh OR FOMC)[id:586873] = BoC 三年来首次加息、明言用于限制油价传导（详见正文引用）
- Anthropic IPO 散户份额最高 20%: query_raw_items(published_after=2026-10-28T10:00:00Z)[id:585910] = Anthropic IPO 拟向散户开放最高 20% 份额、JPMorgan 主承销
- 美债收益率升破 5%: query_raw_items(published_after=2026-10-28T10:00:00Z)[id:585912] = 美债收益率升破 5%（详见正文引用）
- SpaceX 路易斯安那项目法律挑战: query_raw_items(published_after=2026-10-28T10:00:00Z)[id:587471] = SpaceX 1000 亿美元项目遭当地法律挑战、SPCX 盘中 -3.6%

- 美股盘中最新报价（10/28 ~15:50 UTC）: market_quote(symbols=['SPY.US','QQQ.US','MSFT.US','GOOGL.US','MU.US']) = SPY 771.33 (+0.22%) / QQQ 722.24 (+0.14%) / MSFT 527.08 (-0.80%) / GOOGL 323.75 (+0.99%) / MU 970.93 (+4.54%)
- BTC 24h 行情: binance_get_ticker(symbol='BTCUSDT') = 80498.0 美元，24h -0.107%，区间 80387.9–81800，成交额 84.39 亿美元（10/28 15:49 UTC）
- Anthropic IPO 招股书披露政府报复风险: query_raw_items(source='telegram:Financial_Express')[id:589168] = Anthropic 警告投资者其 AI 安全倡导立场可能使其成为政府报复目标，过去一年与特朗普政府多次摩擦
- WTI 突破 103 美元: query_raw_items(source='telegram:Financial_Express')[id:589167] = WTI 原油突破 103 美元/桶，日内涨 3.13%（10/28 15:45 UTC）
- WTI 日内 +3% 至 102.91 美元: query_raw_items(source='telegram:Financial_Express')[id:589152] = WTI 原油日内涨幅达 3.0%，报 102.91 美元/桶（15:39 UTC）
- 以色列特殊选票 43–48 万张: query_raw_items(source='telegram:Financial_Express')[id:589166] = 以色列中央选举委员会公布议会选举特殊选票预计 43 万至 48 万张，或将影响最终大选格局（15:45 UTC）
- 埃尼重启委内瑞拉 Junin-5: query_raw_items(source='telegram:Financial_Express')[id:589150] = 埃尼预计 Junin-5 第一阶段到 2028 年产量达 20 万桶/日
- PIMCO 减持 Meta 与 Oracle: query_raw_items(keyword='PIMCO')[id:589075] = PIMCO 在 AI 债券融资热潮中大幅减持 Meta 与 Oracle 仓位各约一半
- SpaceX 路易斯安那项目法律挑战: query_raw_items(keyword='SpaceX')[id:587471] = SpaceX 1000 亿美元路易斯安那项目遭当地法律挑战，SPCX 盘中 -3.6%
- 加拿大央行加息 25bp: query_raw_items(keyword='加拿大央行')[id:586873] = 加拿大央行三年来首次加息 25bp 至 2.50%，行长麦克勒姆称用于限制油价传导
- SK 海力士 Q3 财报: query_raw_items(keyword='SK海力士')[id:587402] = SK 海力士 Q3 营收 104.62 万亿韩元创纪录、股价 +10%
- SK 海力士产能售罄: query_raw_items(keyword='SK海力士')[id:586216] = SK 海力士产能售罄至 2029 年
- 微软财报预期与 Azure 首次披露: query_raw_items(keyword='微软')[id:587973] = 微软 Q1 FY27 预期 EPS 4.72 美元、营收 907 亿美元，首次披露 Azure 季度美元收入
- Anthropic IPO 散户份额: query_raw_items(keyword='Anthropic IPO')[id:585910] = Anthropic IPO 拟向散户开放最高 20% 份额、JPMorgan 主承销、Dimon 拟个人参与
- Anthropic 亏损与估值口径: query_raw_items(keyword='Anthropic')[id:586308] = 报道口径上半年净亏损 807 亿美元、估值 1.5–2 万亿美元
- 美银客户两周净卖出美股: query_raw_items(keyword='美银')[id:587975] = 美银客户上周净卖出 35 亿美元美股、前周流出 150 亿美元
- 恩智浦 Q4 指引不及预期: query_raw_items(keyword='恩智浦')[id:587472] = 恩智浦因 Q3 营收 37.9 亿美元不理想、Q4 指引不及预期跌超 6%
- Vertiv 上调指引: query_raw_items(keyword='Vertiv')[id:588574] = Vertiv 因强劲 Q3 财报、上调全年指引，盘中 +13.3%
- TTF 天然气 100 欧元: query_raw_items(keyword='TTF')[id:588575] = 荷兰 TTF 天然气触及 100 欧元/兆瓦时，胡塞袭击 + QatarEnergy 不可抗力
- 10Y 美债收益率破 5%: query_raw_items(keyword='美债收益率')[id:585912] = 美债收益率升破 5%
