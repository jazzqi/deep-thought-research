# reference · 目标周 2026-11-02__2026-11-08 · soros（第1/3棒）

## 行情快照
- 10Y UST收益率: fetch_url(query1.finance.yahoo.com/v8/finance/chart/^TNX?range=5d&interval=1d) = 4.988%（2026-10-23收盘；10-19为5.136%，10-21周内高点5.146%，10-22回落4.953）
- 2Y UST收益率: query_indicators(time_range=7d) = 4.74%（source:openbb, data:2026-10-16，⚠️非最新）
- 2s10s利差: query_indicators(time_range=7d) = 38bp（source:openbb, data:2026-10-19）
- 美元指数DXY: fetch_url(query1.finance.yahoo.com/v8/finance/chart/DX-Y.NYB?range=5d&interval=1d) = 101.752（2026-10-23，52周区间95.55-102.95）
- 欧元兑美元: fetch_url(query1.finance.yahoo.com/v8/finance/chart/EURUSD=X?range=5d&interval=1d) = 1.1216（2026-10-25，用于交叉验证DXY）
- 标普500: fetch_url(query1.finance.yahoo.com/v8/finance/chart/^GSPC?range=5d&interval=1d) = 7623.68点（2026-10-23收盘，当日-0.52%；周初10-19为7690.73点，周跌0.87%；52周高7844.52）
- Brent原油期货: fetch_url(query1.finance.yahoo.com/v8/finance/chart/BZ=F?range=5d&interval=1d) = 110.28美元/桶（2026-10-25；10-23收盘116.72，52周区间58.72-126.10）
- COMEX黄金12月合约: fetch_url(query1.finance.yahoo.com/v8/finance/chart/GC=F?range=5d&interval=1d) = 4008.9美元/盎司（2026-10-25；10-20收盘4142.6；52周高5586.2）
- USDCNH: fetch_url(query1.finance.yahoo.com/v8/finance/chart/USDCNH=X?range=5d&interval=1d) = 6.6686（2026-10-25；52周区间显示6.6661-6.6687，口径异常窄，仅取现价）
- VIX: query_indicators(time_range=7d) = 18.44（source:openbb, data:2026-10-19）
- 美国高收益债利差: query_indicators(time_range=7d) = 3.29%（source:openbb, data:2026-10-19）
- 美元指数(冲突未采用): query_indicators(time_range=7d) = 121.4048（source:openbb, data:2026-10-16，与Yahoo DXY及EURUSD交叉验证冲突，本稿未采用）

## 宏观指标
- 美国CPI同比: query_indicators(time_range=24h) = 3.7%（source:akshare, data:2026-09）
- 美国联邦基金利率: query_indicators(time_range=7d) = 3.75%（source:openbb, data:2026-09，目标区间3.75-4.00%）
- 中国9月CPI同比: query_indicators(time_range=24h) = 0.9%（source:akshare, data:2026年09月份）
- 中国9月PPI同比: query_indicators(time_range=24h) = 5.0%（source:akshare, data:2026年09月份）
- 中国三季度GDP同比: query_indicators(time_range=24h) = 4.6%（source:akshare, data:2026年第1-3季度）
- 中国9月M2同比: query_indicators(time_range=24h) = 7.2%（source:akshare, data:2026年09月份）
- 中国官方制造业PMI: query_indicators(time_range=24h) = 50.1（source:akshare, data:2026年09月份）
- 中国10年期国债收益率: query_indicators(time_range=24h) = 1.64%（source:akshare, data:2026-10-23）
- 中国2年期国债收益率: query_indicators(time_range=24h) = 1.2452%（source:akshare, data:2026-10-23）

## 日历事件（query_calendar_events）
- 美国10月ISM制造业指数: query_calendar_events(country=US, days=16, importance=high,medium, limit=200) = 发布2026-11-02 15:00 UTC，前值54.5（分项前值：新订单55.3/就业52.7/物价支付77.9）；市场预测⚠️缺
- 美国10月ADP就业人数变动: query_calendar_events(country=US, days=16) = 发布2026-11-04 13:15 UTC，前值9.0万；市场预测⚠️缺
- 美国10月ISM非制造业指数: query_calendar_events(country=US, days=16) = 发布2026-11-04 15:00 UTC，前值54.9；市场预测⚠️缺
- 美国10月非农就业人口变动: query_calendar_events(country=US, days=16) = 发布2026-11-06 13:30 UTC，前值+2.9万（9月私营+4.6万、制造业+0.9万）；市场预测⚠️缺
- 美国10月失业率: query_calendar_events(country=US, days=16) = 2026-11-06 13:30 UTC，前值4.2%（时薪同比3.0%、环比0.1%、劳动参与率61.8%、平均周工时34.4小时）
- 美国9月JOLTS职位空缺: query_calendar_events(country=US, days=16) = 2026-11-03 15:00 UTC，前值707.9万
- 美国10月31日当周初请失业金人数: query_calendar_events(country=US, days=16) = 2026-11-05 13:30 UTC（前周19.4万口径见10-22条目）
- 美国11月中期选举: query_calendar_events(country=US, days=16) = 2026-11-03（importance medium，日历条目"美国 11 月 3 日中期选举"）
- FOMC利率决议（周外前置）: query_calendar_events(country=US, days=16) = 2026-10-28 18:00 UTC，下限3.75%/上限4.00%，前值与共识均3.75/4.00；18:30 美联储主席沃什新闻发布会
- 美国三季度GDP年化季环比初值: query_calendar_events(country=US, days=16) = 2026-10-29 12:30 UTC，前值2.2%，共识3.0%（另一条目3.2%，⚠️共识口径冲突）
- 英国央行政策利率: query_calendar_events(country=, days=14...全量) = 2026-11-05 12:00 UTC，前值3.75%；市场预测⚠️缺
- 中国10月RatingDog制造业PMI: query_calendar_events(country=CN, days=14, importance=high,medium) = 2026-11-02 01:45 UTC，前值52.1
- 中国10月RatingDog服务业/综合PMI: query_calendar_events(country=CN, days=14) = 2026-11-04 01:45 UTC，前值51.6/52.4
- 中国10月外汇储备: query_calendar_events(country=CN, days=14) = 前值34002.5亿美元（11-06 16:00 UTC与11-07 08:00 UTC两条重复条目）；11-07含黄金储备前值7747万盎司
- 欧元区10月制造业PMI终值: query_calendar_events(days=14, lookback=7, importance=high,medium 全量) = 2026-11-02 09:00 UTC，初值52.4（前值52.9，初值于10-23公布）
- 英国9月CPI同比: query_calendar_events(全量) = 3.5%（预期3.4、前值3.1，2026-10-21公布；核心2.8%、输入PPI 8.3%）
- 韩国10月CPI同比: query_calendar_events(全量) = 2026-11-02 23:00 UTC，前值2.9%
- 韩国10月前20天出口同比: query_calendar_events(全量) = +105.4%（前值78.3%，2026-10-21）
- 中国10月官方制造业PMI: query_calendar_events(country=CN) = 2026-10-31 01:30 UTC公布（周前，前值50.1，写作时actual未返回）
- 美国10月标普全球制造业PMI终值: query_calendar_events(country=US, days=16) = 2026-11-02 14:45 UTC

## 新闻（query_raw_items）
- 周末中东无军事行动、美股期货走高、原油走低: query_raw_items(limit=50, source=telegram:Financial_Express, published_after=2026-10-24)[id:535293] = 标普500股指期货周一早盘走高，原油价格走低，原因是周末中东没有发生军事行动；特朗普称对伊朗"快要到做决定的时候了"
- 布伦特自六个月高点回落、伊朗准备围绕美国11月3日中期选举前后新一轮轰炸: query_raw_items(...)[id:535292] = 布伦特低于116美元、上周涨超6%，WTI接近102美元；华盛顿下令扩大中东撤离；伊朗准备应对11月3日前后新轰炸并拟打击以色列与阿联酋
- CME美联储观察定价: query_raw_items(...)[id:535274] = 本周维持不变概率90%、加息25bp概率10%；12月维持23.8%、累计+25bp 68.9%、+50bp 7.3%
- 伊朗革命卫队向霍尔木兹海峡方向发射导弹: query_raw_items(...)[id:535266] = 当地时间周一凌晨从霍尔木兹甘省向霍尔木兹海峡方向发射导弹
- 美国财政部将科技投资限制扩大至生物技术、中国警告反制: query_raw_items(limit=50)[id:535255] = China warns of countermeasures as US Treasury widens tech investment curbs to biotech
- 欧洲天然气价格升至2022年以来最高: query_raw_items(...)[id:535283] = 欧洲天然气价格在周一亚市盘初升至2022年以来的最高水平
- 富时世界国债指数中国权重升至11.9%: query_raw_items(...)[id:535298] = WGBI 9月指数概况中国权重11.9%，为仅次于美国的第二大国债市场
- 美加贸易协议即将达成: query_raw_items(limit=50)[id:535217] = Trump: Deal with Canada Imminent
- 特朗普称伊朗冲突将很快结束、中期选举后发放5000美元分红: query_raw_items(...)[id:535291] = 你们很快就会看到伊朗冲突以某种方式结束；中期选举结束后不久将发放5000美元分红
- 内塔尼亚胡称已指示推翻伊朗政权: query_raw_items(...)[id:535270] = 已指示摩萨德和以色列国防军推翻该政权
- SpaceX完成400亿美元债务融资购买GPU: query_raw_items(limit=50)[id:535219] = Musk says SpaceX raised $40 billion in debt for GPUs
- AWS云容量预订至2027年: query_raw_items(limit=50)[id:535184] = AWS CEO称AI需求激增使云容量已全额预订至2027年

2026-10-26 世界确认：美联储主席为沃什（Warsh，10-28 FOMC由其主持发布会），联邦基金利率目标区间3.75-4.00%，美国9月CPI同比3.7%，市场处于"再加息"讨论中（CME：12月累计+25bp概率68.9%）。我的训练数据（鲍威尔任内、降息周期）已过时——涉及美联储人事与政策方向必须先查日历/新闻再下判断。

2026-10-26 数据坑：指标库 openbb dollar_index=121.4048（2026-10-16）与 Yahoo Finance DXY=101.75（2026-10-23）严重冲突；用 EURUSD=1.1216（2026-10-25）交叉验证后，101.75 为真值，121.40 不可用。判断：涉及美元指数，先用外汇对（EURUSD）交叉验证再引用 | 禁忌：别把指标库 dollar_index 单点直接写进报告 | 出处：2026-11-02周报行情快照。

2026-10-26 观察：美国调查数据与就业硬数据连续背离——ISM制造业54.5、芝加哥PMI 58.8 vs 9月非农仅+2.9万、ADP 9.0万；同期韩国10月前20天出口同比+105.4%、AWS云容量订满至2027、SpaceX举债400亿美元买GPU。判断：AI资本开支高度集中于少数部门，使PMI类调查指标系统性高估就业扩散面 | 禁忌：别用ISM单点外推劳动力市场，非农/时薪/失业率必须交叉验证 | 出处：2026-11-02当周forecast。

appendreference.md0.8535292伊朗围绕11-03美国中期选举的攻击窗口+布伦特110-116美元区间，直接决定本周油价、通胀与12月加息定价P00.85535274CME 12月累计加息25bp概率68.9%是本周所有就业数据情景分析的基准坐标P00.7535293周末无战事+期货走高，确立周初单向乐观定价基线，是反身性分析的起点P10.7535266IRGC向霍尔木兹海峡方向发射导弹，海峡通航与油轮风险未出清P10.7535255美国对华投资限制扩至生物技术且中方警告反制，中美摩擦升级线索P10.75535283欧洲天然气创2022年以来新高，推升欧通胀与成本压力，影响ECB路径P20.7535298WGBI中国权重11.9%，外资配置中国债的结构性资金流线索，支撑人民币资产叙事P30.7535291特朗普把伊朗冲突收尾与选后5000美元分红绑定，政策与地缘事件窗口集中在美国中期选举后P10.7535270以色列总理下令推翻伊朗政权，冲突升级尾部风险上升，油价风险溢价未出清P10.8["美联储", "沃什", "加息", "通胀", "知识时效"]长期0.7["数据质量", "美元指数", "交叉验证"]长期0.6["背离", "AI资本开支", "就业", "PMI"]3个月