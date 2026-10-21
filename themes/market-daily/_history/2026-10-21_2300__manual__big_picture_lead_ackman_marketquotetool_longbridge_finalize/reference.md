
## 2026-10-21 数据来源（周度复盘轮）
- 美股盘中（10/21 14:52 UTC）纳指100 +0.9%创盘中新高、标普+0.3%: query_raw_items(source=telegram:Financial_Express, published_after=2026-10-20)[id:501263] = 纳斯达克 100 指数上涨 0.9%，创盘中新高；标普 500 指数上涨 0.3%
- VIX 日内 -3.0% 报 16.79（10/21 14:52 UTC）: query_raw_items(source=telegram:Financial_Express, published_after=2026-10-20)[id:501261] = VIX 日内跌幅达 3.0%，报 16.79
- 费半 +2.03% 报 11512.85（10/21 开盘）: query_raw_items(keyword=芯片/半导体, published_after=2026-10-17)[id:500999] = 费城半导体指数日内涨 2.03%，NVDA+2.36%、MU+3.45%、TSMC+2.01%、ASML+2.95%
- 10/21 开盘个股与财报: query_raw_items(keyword=芯片/半导体, published_after=2026-10-17)[id:501010] = SpaceX +8%（Q3营收145.8亿美元同比+161%，AI收入+830%，净利超预期2.3倍）、超微电脑+11%（Q1初步营收远超预期）、奈飞-6%（Q4指引与广告收入不及预期）、英伟达+2%（柏林GTC新品）
- 新云股盘中逆转（10/21 13:47 UTC）: query_raw_items(keyword=芯片/半导体, published_after=2026-10-17)[id:501055] = Nebius -3.6%、CoreWeave -2.9%
- 10/19 美股收盘（基线后首个交易日）: query_raw_items(keyword=连跌/费城半导体, published_after=2026-10-17)[id:493804] = 标普+0.41%报7690.73；费半+1.61%报11316.34，终结八连跌；等权-0.40%
- 10/19 全景: query_raw_items(keyword=连跌/费城半导体, published_after=2026-10-17)[id:493997] = 纳指涨超1%、道指两连跌、半导体指数+1.6%终结八连跌；法国等欧洲多国股指跌超1%；离岸人民币四年来首次盘中涨破6.68
- 10/20 美股收盘: query_raw_items(keyword=连跌/费城半导体, published_after=2026-10-17)[id:497835] = 标普+0.28%报7712.57、等权-0.34%、费半-0.29%报11283.81、KBW银行+1.45%、罗素2000+1.65%
- 韩股 10/20: query_raw_items(keyword=连跌/费城半导体, published_after=2026-10-17)[id:495059] = KOSPI -3.73%收5552.74，创4月7日以来六个月最低收盘
- AI融资担忧（10/20）: query_raw_items(keyword=连跌/费城半导体, published_after=2026-10-17)[id:496511] = 韩国AI基建商Elice上市首日暴跌32%；澳洲Firmus Grid放弃IPO；CoreWeave盘前-4%
- 英国9月CPI: query_raw_items(keyword=10年期/美债/加息, published_after=2026-10-17)[id:499482] = 9月CPI同比3.5%（预期3.4%、前值3.1%），11个月高位，英央行11月加息25bp预期升温
- 法国国债: query_raw_items(keyword=10年期/美债/加息, published_after=2026-10-17)[id:499890] = 法国10年期国债收益率触及5%创24年新高；[id:499883] OAT-Bund利差扩大6bp至159.4bp创15年最宽
- 加息定价与黄金: query_raw_items(keyword=10年期/美债/加息, published_after=2026-10-17)[id:499538] = 交易员定价年内再加息一次概率约85%；金价自伊冲突爆发以来下跌约五分之一
- 油价（10/21盘前）: query_raw_items(keyword=连跌/费城半导体, published_after=2026-10-17)[id:500805] = WTI +0.68%报98.49美元/桶、布伦特+0.37%报109.19美元/桶；伊朗外长称看不到谈判进展理由
- 贝莱德IG观点: query_raw_items(keyword=10年期/美债/加息, published_after=2026-10-17)[id:499038] = 企业信贷出现"一代人一遇"的高收益水平，多元固收组合收益率超7%、久期<3年
- 谷歌云Rubin部署: query_raw_items(keyword=芯片/半导体, published_after=2026-10-17)[id:500836] = 谷歌云计划多站点部署多达96万块Rubin GPU，A5X实例下月开放
- 美国宏观指标快照: query_indicators(country=us, category=空, time_range=24h) = vix 18.44(2026-10-19)、yield_10y 5.09(2026-10-16)、yield_2y 4.74(2026-10-16)、dollar_index 121.4048(2026-10-16)、corporate_spread 0.87(2026-10-19)、high_yield_spread 3.29(2026-10-19)、yield_spread_2s10s 0.38(2026-10-19)
- 未来事件窗口: query_calendar_events(country=US, days=10, lookback=4, importance=high,medium) = 初请10/22（前值19.9万）、苹果发布会10/26、FOMC利率决策10/28（前值3.75-4.00，预测不变）、三季度GDP初值10/29（前值2.2）

# 2026-10-21 市场每日追踪 数据溯源（tech_generalist 第一棒）

## 原始新闻（query_raw_items，2026-10-21）
- 纳指100 +0.9%盘中新高、标普+0.3%: query_raw_items(published_after=2026-10-20T12:00Z)[id:501263] = 纳斯达克100指数上涨0.9%创盘中新高；标普500涨0.3%
- VIX -3.0%至16.79: query_raw_items(published_after=2026-10-20T12:00Z)[id:501261] = 恐慌指数VIX日内跌幅达3.0%，报16.79
- 费半 +2.03%至11512.85（NVDA+2.36%/AVGO+1.10%/MU+3.45%/INTC+2.48%/AMD+2.72%/TSM+2.01%/ASML+2.95%/QCOM-0.21%）: query_raw_items(keyword=CoreWeave OR NVIDIA...)[id:500999] = 费城半导体指数日内涨2.03%
- 存储板块领涨（SK海力士/闪迪+4%、美光+3%、西数+3.87%、希捷+5.22%）: query_raw_items(keyword=CoreWeave OR NVIDIA...)[id:501006] = 美股存储板块盘初普涨
- 开盘七姐妹（TSLA+2.67%/NVDA+2.45%/META+0.48%/AAPL+0.01%/AMZN-0.47%/MSFT-0.87%/GOOGL-1.66%）: query_raw_items(keyword=CoreWeave OR NVIDIA...)[id:501003] = 美股开盘三大股指齐涨
- 超微电脑Q1初步营收远超预期（盘前+13%、盘初+11%）: query_raw_items[ids:500805, 501010] = 超微电脑盘前涨超13%，Q1初步业绩营收大超预期
- 奈飞Q4指引弱+下调全年广告预期，盘中跌约6%（14:56时-4.8%）: query_raw_items[ids:501010, 501274] = 奈飞第四季度利润指引弱于预期，下调全年广告业务预期
- 苹果盘中涨超1%创盘中新高: query_raw_items[ids:501294, 501291] = 苹果股价上涨逾1%创盘中新高
- SpaceX开盘+8%（盘前+10%，业绩强劲，AI+卫星互联网）: query_raw_items[ids:500998, 500805] = SpaceX(SPCX.O)涨8%
- 谷歌云与英伟达：Vera Rubin NVL72 A5X实例下月开放，谷歌云计划部署最多96万块Rubin GPU: query_raw_items(keyword=CoreWeave OR NVIDIA...)[id:500836] = 谷歌云与英伟达宣布A5X实例下月正式开放
- 黄仁勋：英伟达已能批量造超级计算机，同时为数百个数据中心供货: query_raw_items[ids:500887, 500805] = GTC柏林
- 三星电机与英伟达签署有约束力的多年ABF封装基板供应协议（2026年起交付）: query_raw_items[ids:500663] = 三星电机已与英伟达签署具有约束力的多年供应协议
- 华硕Q4上市搭载HGX Rubin NVL8的服务器: query_raw_items[id:500661] = 华硕准备出货搭载英伟达HGX Rubin NVL8的服务器系统
- Crusoe CEO：A100租金高于2020-21年、H100高于2023年部署时: query_raw_items(keyword=CoreWeave OR NVIDIA...)[id:501071] = 英伟达支持的AI公司Crusoe
- Nebius CRO：算力涨价超预期、无CoreWeave式债务、2027产能将被订满: query_raw_items[ids:501068] = Nebius Group NV高管表示
- 新云股高开逆转：CoreWeave +2.85%→-2.9%、Nebius +3.39%→-3.6%: query_raw_items[ids:501004, 501055] = 新云公司股价走势逆转
- DayOne Data Centers重新评估美国IPO，或缩半至25-30亿美元: query_raw_items(keyword=CoreWeave OR 甲骨文 OR 数据中心 OR 债)[id:501247] = 随着数据中心板块波动加剧
- 长川科技前三季净利+98-110%（半导体测试设备订单充裕）: query_raw_items(keyword=芯片 OR 半导体 OR 存储)[id:500942] = 长川科技预计前三季度净利润同比增长98.17%-109.73%
- 江波龙：UFS4.1/mSSD/ePOP5x商业突破、HLC与AMD/高通联合调优: query_raw_items[ids:501275, 500922] = 江波龙在互动平台表示
- 路透：三星与SK海力士升级中国工厂产更先进NAND: query_raw_items(keyword=芯片 OR 半导体 OR 存储)[id:500725] = 据路透社引述未具名知情人士报道
- 英特尔亚利桑那Fab 62设备安装进行中/俄亥俄首根大型屋顶桁架: query_raw_items[ids:501295, 501289, 501286] = 英特尔官方表态
- 法国10Y收益率触及5%创24年新高: query_raw_items(keyword=CoreWeave OR 甲骨文 OR 数据中心 OR 债)[id:500805] = 美股盘前要闻速递⑥
- 内塔尼亚胡推动恢复对伊朗大规模打击；伊朗外长称无谈判进展理由: query_raw_items[ids:500805] = 美股盘前要闻速递④⑤
- 中国对日稀土出口管制、日本关键稀土储备将尽；欧央行Kazaks鹰派；BOJ下周议息；五中全会/沙盒监管: query_raw_items[ids:500854] = 快讯合集
- 英债10Y -5bp至5.36%: query_raw_items(keyword=CoreWeave OR 甲骨文 OR 数据中心 OR 债)[ids:500996, 500983] = 各期限英债走强
- 英国30Y -6bp至5.7726%（9/23以来最低）: query_raw_items[ids:501095] = 英国30年期国债收益率降至5.7726%
- 英国公共净债务首破3万亿英镑（GDP 94%）: query_raw_items[ids:500870, 500871] = 英国公共债务总额首次突破3万亿英镑
- 白宫与领先AI实验室协调加速PHP漏洞补丁: query_raw_items[ids:501246, 501265] = 白宫声明

## 事件日历（query_calendar_events，days=10, lookback=3, importance=high/medium）
- 韩国10月1-20日出口同比+105.4%（前值+78.3%）: query_calendar_events = KR 2026-10-21 actual 105.4
- 韩国央行利率决议 10/21 16:00 UTC: query_calendar_events
- 初请失业金 10/22（前值19.9万，预期20.0万）: query_calendar_events
- 欧元区10月制造业PMI初值 10/23（前值52.9，预期52.8）: query_calendar_events
- 日本9月CPI 10/23（前值1.9，预期2.1）: query_calendar_events
- 二十届五中全会开幕 10/25-26: query_calendar_events
- 苹果10月第二场发布会（首款触控MacBook+iPad mini）10/26: query_calendar_events
- FOMC利率决议 10/28（预期3.75-4.00%不变）: query_calendar_events
- 腾讯全球数字生态大会 10/28: query_calendar_events
- 美Q3 GDP初值 10/29（前值2.2%年化）+ ECB议息 10/29: query_calendar_events
- 中国Q3 GDP同比4.5%（预期4.4）、9月社零+1.1%、10月LPR 3.0/3.5不变: query_calendar_events

## 个人记忆/前日报告（盘前追踪与主题文档，非本次工具调用）
- TY看跌期权超10万张押注10Y月末>5.3%（当时约5.11%，覆盖FOMC与9月核心PCE）: 个人记忆库(remember, 2026-10-21晨)
- OAT-德债利差159bp（2011年末来最宽）: 个人记忆库(remember, 2026-10-21晨)
- 布伦特冲高2.2%后回落至107.7美元/桶（EIA库存-306万桶超预期）: 个人记忆库(remember, 2026-10-21晨)
- CoreWeave 5Y CDS 1194.5bp历史新高、2031到期9% HY债79.9美分（10/15）: 个人记忆库(remember, 2026-10-16)
- 巴克莱利率路径上调为12月+1月各25bp: themes/market-daily/index.md (2026-10-17版)[id:487944，前一交易日引用]
- 10/16芯片八连跌（2008年来最长）: themes/market-daily/index.md (2026-10-17版)
- 备注：query_longbridge_by_route 行情接口本次返回token expired（401003），盘中价格全部改用快讯口径，无长桥数据

- 纳指100盘中扩大涨幅至1%、标普500 +0.4%（15:15 UTC）: query_raw_items(published_after=2026-10-21T13:00Z)[id:501309] = 纳斯达克100指数涨幅达1%，标普500指数上涨0.4%
- 个股分化：SpaceX +9.8%、Datadog/Strategy +7.1%、谷歌A -2.2%、奈飞 -4.6%、拼多多ADR -3.9%: query_raw_items(published_after=2026-10-21T13:00Z)[id:501313] = 纳斯达克100指数涨幅扩大至1%成分股涨跌明细
- 纳指100 +0.9%创盘中新高、VIX日内-3.0%报16.79: query_raw_items(published_after=2026-10-21T13:00Z)[id:501261] = 纳指涨0.9%刷新日高，VIX跌3%报16.79
- 开盘三大指数与板块明细（超微+10.93%、SpaceX +8.49%、七姐妹分化）: query_raw_items(published_after=2026-10-21T13:00Z)[id:501003] = 美股开盘三大股指齐涨明细
- 广发纳指ETF因溢价15.9%（1.712元 vs 净值1.4768元）10/22停牌: query_raw_items(keyword=VIX OR 纳指 OR 标普)[id:500111] = 纳指ETF广发因二级市场溢价10月22日起临时停牌
- 国泰标普500ETF溢价约7.7%（2.072元 vs 净值1.9236元）: query_raw_items(keyword=VIX OR 纳指 OR 标普)[id:500118] = 标普500ETF国泰二级市场价格大幅溢价提示风险
- 华泰柏瑞纳指ETF 10/22开市起停牌至10:30: query_raw_items(keyword=VIX OR 纳指 OR 标普)[id:500502] = 纳指ETF华泰柏瑞10月22日停牌公告
- 法国10Y-德债利差159bp创2011年末最宽: query_raw_items(keyword=法国 OR OAT OR 法债)[id:500175] = LSEG数据法德10Y利差159bp
- 富兰克林邓普顿警告"欧元区债务危机2.0"，法国债务约3.6万亿欧元为希腊10倍以上: query_raw_items(keyword=法国 OR OAT OR 法债)[id:500132] = Franklin Templeton Desai警告
- 巴黎本周第三次夜间宵禁（共和国广场一带，10/21 23时-22日6时）: query_raw_items(keyword=法国 OR OAT OR 法债)[id:501103] = 巴黎警察总局宣布宵禁
- 法国10Y触及5%创24年新高、内塔尼亚胡推动恢复对伊大规模打击、WTI 98.49/布伦特109.19（盘前）: query_raw_items(keyword=美联储 OR FOMC OR 加息 OR 收益率)[id:500805] = 美股盘前要闻速递
- 内塔尼亚胡："消灭伊朗政权是我对以军的指示": query_raw_items(published_after=2026-10-20T12:00Z)[id:501311] = 以色列总理表态
- EIA原油库存-306万桶（预期-82万桶）: query_raw_items(keyword=黄金 OR 原油 OR 布伦特)[id:501163] = EIA库存周报
- 布伦特日内跌1%至107.70美元/桶: query_raw_items(keyword=黄金 OR 原油 OR 布伦特)[id:500894] = 布伦特报价
- EIA数据公布后油价转涨: query_raw_items(keyword=黄金 OR 原油 OR 布伦特)[id:501225] = EIA库存降幅超预期油价转涨
- 美政府借出东北取暖油储备31.5万桶、柴油均价6.32美元/加仑: query_raw_items(keyword=黄金 OR 原油 OR 布伦特)[id:501207] = 取暖油储备释放
- 谷歌CEO皮查伊："几乎所有企业面临算力短缺"、谷歌云主动放弃短期收入让渡算力给前沿研发: query_raw_items(keyword=CoreWeave OR Nebius OR 算力 OR 存储)[id:500965][id:500956] = Pichai表态
- 新云股逆转：Nebius -3.6%、CoreWeave -2.9%: query_raw_items(keyword=CoreWeave OR Nebius OR 算力 OR 存储)[id:501055] = 新云公司股价走势逆转
- Crusoe CEO称老款GPU租金也高于上轮周期: query_raw_items(keyword=CoreWeave OR Nebius OR 算力 OR 存储)[id:501071] = Crusoe定价表态
- 印度央行副行长：加息周期持续时间与幅度取决于增长与通胀: query_raw_items(keyword=美联储 OR FOMC OR 加息 OR 收益率)[id:500623] = RBI表态
- 欧央行管委Kazaks：收益率上升可能拖慢经济需保持谨慎: query_raw_items(keyword=美联储 OR FOMC OR 加息 OR 收益率)[id:500117] = Kazaks讲话
- 英债10Y -5bp至5.36%、30Y -6bp至5.7726%（9/23以来最低）: query_raw_items(keyword=美联储 OR FOMC OR 加息 OR 收益率)[id:500996][id:501095] = 英债走强
- BTC 24h +2.49%至84456.8美元: binance_get_ticker(BTCUSDT) = price 84456.8, +2.494%
- 韩国10月前20天出口同比+105.4%（前值+78.3%）: query_calendar_events(importance=high,medium, lookback=3) = 2026-10-21 KR出口20天同比
- 韩国央行10/21 16:00 UTC议息、FOMC 10/28 18:00 UTC（预期3.75-4.00%）、美Q3 GDP 10/29、ECB 10/29、初请10/22 12:30 UTC（前值19.9万/预期20.0万）、日CPI 10/22（预期2.1%）、欧PMI 10/23（预期52.8）、苹果发布会10/26、五中全会10/25: query_calendar_events(days=10, importance=high,medium) = 事件列表


## 第三棒（ackman 终稿）新增溯源（2026-10-21 15:27-15:29 UTC）

- BTCUSDT 24h行情: binance_get_ticker(symbol=BTCUSDT) = 最新价 84407.0 USDT，24h +2.413%，最高 84788.0，最低 82308.0（10/21 15:28 UTC）
- market_quote 港美股报价可用性: market_quote(symbols=NVDA/GOOGL/AAPL/NFLX/SMCI.US) = 返回 OpenApiException code 401003 token expired，盘中个股价格继续采用快讯口径
- 纳指100盘中+1%与成分股明细: query_raw_items(source=telegram:Financial_Express, published_after=2026-10-21T12:00:00Z)[id:501313] = 纳指100涨幅扩大至1%，SpaceX +9.8%、Datadog/Strategy +7.1%、谷歌A -2.2%、拼多多ADR -3.9%、奈飞 -4.6%（15:16 UTC）
- 苹果盘中涨幅扩大: query_raw_items(...)[id:501329] = 苹果股价涨幅扩大至1.5%（15:24 UTC）
- 美取暖油储备出借升级: query_raw_items(...)[id:501321] = 美能源部提议出借100万桶应急取暖油储备中近三分之一；柴油价格因伊朗战争导致的中东供应中断已创6.50美元/加仑以上历史新高（15:19 UTC）
- 沙特对法额外柴油供应: query_raw_items(...)[id:501333] = 法国总统府称沙特同意"在必要期间"持续对法额外供应柴油，巴黎预计每月额外获得29.5万吨（15:27 UTC）
- 美俄乌三方会晤: query_raw_items(...)[id:501332] = 美国官员称俄方已接受美方提出的与乌克兰举行三方会晤提议（15:26 UTC）
- 埃及军事介入边界: query_raw_items(...)[id:501324] = 塞西称埃及军事参与严格限于保卫沙特，不涉及对也门进攻（15:21 UTC）
- 白宫PHP漏洞口径: query_raw_items(...)[id:501312][id:501318] = 白宫10/16获悉PHP漏洞，要求AI公司改进检测与整改；美官员强调AI企业是发现漏洞而非制造漏洞（15:16-15:18 UTC）


## taleb 交叉审查独立核验来源（2026-10-21 15:36 UTC）
- 特朗普称AI数据中心应向社区支付"分红"、共和党内反对上升（中期选举前转向）: query_raw_items(keyword='数据中心 OR data centres OR dividends')[id:501335] = Trump says AI data centres should pay 'dividends' in pre-midterm shift; growing opposition from Republicans
- 特朗普"给社区居民发分红+自己发电，数据中心就会大受欢迎"（同日快讯汇总）: query_raw_items(keyword='特朗普 OR tariffs OR 关税')[id:500854] = 多条汇总快讯含该表态
- 特朗普支持率创新低36%（经济/伊朗战事/高油价拖累）: query_raw_items(keyword='特朗普 OR tariffs OR 关税')[id:500849] = 民调显示仅36%认可、59%不认可
- NSA建议无法立即更新则将系统下线（PHP漏洞处置升级）: query_raw_items(keyword='财报 OR 业绩 OR guidance OR 指引')[id:501203] = NSA网络安全部门建议相关机构将系统下线直至缓解风险
- 摩根大通：SpaceX与特斯拉巨型合并预期升温（约2万亿美元、全股票、30-35%溢价）: query_raw_items(keyword='广发纳指 OR 溢价 OR 停牌')[id:500520] = JPM预判SpaceX主导、对特斯拉给出30-35%收购溢价
- CME 10月维持利率不变概率83.9%（10/20，支撑稿中">80%"）: query_raw_items(keyword='美联储观察 OR FedWatch OR 维持利率不变的概率')[id:497896] = 10月维持不变83.9%、12月+25bp 76.1%
- TY Wk5行权价104看跌期权本周累计买入超10万张（10/30到期，覆盖FOMC/9月核心PCE/GDP）: query_raw_items(keyword='看跌期权 OR FedWatch OR 暂停定价')[id:499498] = 交易员赌月末10Y收益率突破5.3%
- CoreWeave债券评级遭交易员下调（10/20）: query_raw_items(keyword='CoreWeave OR CDS OR 垃圾债')[id:497421] = 交易员已下调CoreWeave债券评级
- 派杰投资将CoreWeave目标价153→124美元（10/21）: query_raw_items(keyword='CoreWeave OR CDS OR 垃圾债')[id:498932] = Piper Sandler下调目标价
- Nscale高管内部安抚/新云上周一度大跌近25%: query_raw_items(keyword='CoreWeave OR CDS OR 垃圾债')[id:498995] = AI市场陷入恐慌，Nscale安抚内部员工
- 尾盘油价再挫：WTI 96.37/布伦特105.31美元（15:31 UTC）: query_raw_items(published_after='2026-10-20')[id:501345] = 美布两油短线下挫超1美元
- 标普500最新7746.73（+0.44%）、纳指26691.618（+1.01%）（15:31 UTC）: query_raw_items(published_after='2026-10-20')[id:501343] = 三大指数实时点位
- FOMC会议/日程核对: query_calendar_events(days=14, lookback_days=3, importance='high,medium') = FOMC 10/28 18:00 UTC（前值/预期3.75/4.00）、韩央行10/21 16:00、初请10/22（19.9/20.0）、日CPI 10/22 23:30（1.9/2.1）、欧PMI 10/23（52.9/52.8）、冬令时+五中全会10/25、苹果发布会10/26、腾讯大会10/28、美Q3 GDP+ECB 10/29（GDP前值2.2）
- 中国宏观核对: query_calendar_events(...) = Q3 GDP同比实际4.5/预期4.4、9月社零+1.1、10月LPR 3.0/3.5（均与稿一致）
- 韩国10月前20天出口同比: query_calendar_events(...) = 实际105.4/前值78.3（条目未含"半导体主导"限定）
- QDII溢价停牌批次扩列: query_raw_items(keyword='广发纳指 OR 溢价 OR 停牌')[id:500113][id:500110][id:500502][id:499860][id:499859][id:499858] = 华安/招商/华泰柏瑞停牌，华夏/景顺/标普信息科技LOF提示溢价
- 泽连斯基愿在保留75%领土控制权基础上达成和平协议: query_raw_items(keyword='特朗普 OR tariffs OR 关税')[id:500854] = 央视口径快讯
- 普京、习近平、特朗普准备在APEC峰会期间会晤: query_raw_items(keyword='特朗普 OR tariffs OR 关税')[id:501188] = 俄Ushakov表态
- 马斯克下令对乌使用星盾限速（WSJ 10/20）: query_raw_items(published_after='2026-10-20')[id:501034→误列，实为[id:501304]] = 华尔街日报援引官员称马斯克上周下令限速
- SpaceX作为上市公司首次实现季度盈利并发布强劲业绩展望: query_raw_items(keyword='财报 OR 业绩 OR guidance OR 指引')[id:501038] = 太空股因SpaceX业绩普涨
- 加拿大总理卡尼预计公布针对钢铁和汽车行业关税支持措施: query_raw_items(keyword='特朗普 OR tariffs OR 关税')[id:500954] = 钢铁/汽车关税支持措施


- [订正] 上一行马斯克"星盾"限速条目正确ID为 [id:501304]（来源同为 query_raw_items(published_after='2026-10-20')），501034 为AT&T业绩条目，不作引用。
