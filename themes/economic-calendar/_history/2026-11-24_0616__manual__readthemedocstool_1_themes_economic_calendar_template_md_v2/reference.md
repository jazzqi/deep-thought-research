# 数据来源溯源 — 目标周 2026-11-16 ~ 2026-11-22

## 一、美国宏观数据（query_calendar_events, country=US, lookback_days=14, importance=high,medium）
- 11月纽约联储制造业指数: query_calendar_events(country=US, lookback_days=14) = 7.8（前值25.5，预期18.0，2026-11-16发布）
- 11月纽约联储制造业未来6个月预期指数: query_calendar_events(country=US, lookback_days=14) = 28.9（前值21.0）
- 10月零售销售环比: query_calendar_events(country=US, lookback_days=14) = 0.2%（前值0.8%，预期0.2%）
- 10月零售销售控制组环比: query_calendar_events(country=US, lookback_days=14) = 0.6%（前值0.1%，预期0.4%）
- 10月核心零售销售环比: query_calendar_events(country=US, lookback_days=14) = 0.6%（前值0.9%，预期0.4%）
- 10月工业产出环比: query_calendar_events(country=US, lookback_days=14) = -0.4%（前值0.7%，预期0.1%）
- 10月制造业产出环比: query_calendar_events(country=US, lookback_days=14) = 0.3%（前值0.3%，预期0.2%）
- 10月进口价格指数环比: query_calendar_events(country=US, lookback_days=14) = 1.1%（前值1.1%，预期0.7%）
- 11月NAHB房产市场指数: query_calendar_events(country=US, lookback_days=14) = 25.0（前值29.0，预期29.0）
- 10月新屋开工年化总数: query_calendar_events(country=US, lookback_days=14) = 130.9万户（前值122.1万，预期124.5万）
- 10月营建许可年化初值: query_calendar_events(country=US, lookback_days=14) = 129.5万户（前值139.8万，预期137.7万）
- 30年期房贷利率(MBA): query_calendar_events(country=US, lookback_days=14) = 7.35%（前值7.21%，2026-11-18）
- 11-14当周初请失业救济人数: query_calendar_events(country=US, lookback_days=14) = 20.3万人（前值20.0万，预期19.8万，2026-11-19发布）
- 11月费城联储制造业指数: query_calendar_events(country=US, lookback_days=14) = 6.3（前值20.9，预期20.0）
- 11月密歇根大学消费者信心终值: query_calendar_events(country=US, lookback_days=14) = 51.5（前值51.0，预期51.5）
- 美联储公布货币政策会议纪要: query_calendar_events(country=US, lookback_days=14) = 2026-11-18 19:00 UTC 发布
- 美联储理事沃勒发表讲话: query_calendar_events(country=US, lookback_days=14) = 2026-11-20 13:25 UTC
- 美联储官员11-16当周密集发声聚焦12月加息路径: query_calendar_events(country=US, lookback_days=14) = 条目 2026-11-14/15

## 二、中国宏观数据（query_calendar_events, country=CN, lookback_days=14）
- 10月社会消费品零售总额同比: query_calendar_events(country=CN, lookback_days=14) = 0.4%（前值1.1%，预期0.8%，2026-11-16发布）
- 10月规模以上工业增加值同比: query_calendar_events(country=CN, lookback_days=14) = 4.8%（前值5.5%，预期5.3%）
- 1-10月城镇固定资产投资同比: query_calendar_events(country=CN, lookback_days=14) = -8.1%（前值-7.2%，预期-7.0%）
- 1-10月全国房地产开发投资: query_calendar_events(country=CN, lookback_days=14) = -21.6%（前值-20.6%）
- 10月城镇调查失业率: query_calendar_events(country=CN, lookback_days=14) = 5.1%（前值5.2%）
- 10月新建住宅价格同比: query_calendar_events(country=CN, lookback_days=14) = -2.4%（前值-2.8%）
- 11月LPR 1年期/5年期: query_calendar_events(country=CN, lookback_days=14) = 3.0% / 3.5%（均维持，2026-11-20）
- 10月FDI同比: query_calendar_events(country=CN, lookback_days=14) = -2.4%（前值-4.3%）
- 2026 APEC领导人非正式会议18-19日深圳举行: query_calendar_events(country=CN, lookback_days=14) = 条目 2026-11-16/17

## 三、欧元区数据（query_calendar_events, country=EU, lookback_days=14）
- 11月ZEW经济景气指数: query_calendar_events(country=EU, lookback_days=14) = 26.5（前值18.5，2026-11-17）
- 10月调和CPI同比终值: query_calendar_events(country=EU, lookback_days=14) = 4.0%（前值4.0%，预期4.0%）
- 10月核心调和CPI同比终值: query_calendar_events(country=EU, lookback_days=14) = 2.6%（前值2.5%，预期2.5%，超预期）
- 10月调和CPI环比终值: query_calendar_events(country=EU, lookback_days=14) = 0.5%（前值0.4%，预期0.4%）
- 11月消费者信心指数初值: query_calendar_events(country=EU, lookback_days=14) = -16.9（前值-17.9，预期-18.0）

## 四、行情快照（query_indicators, time_range=7d）
- 10年期美债收益率: query_indicators(yield_10y, openbb, 2026-11-13) = 5.15%
- 2年期美债收益率: query_indicators(yield_2y, openbb, 2026-11-13) = 4.88%
- 美债2s10s利差: query_indicators(yield_spread_2s10s, openbb, 2026-11-16) = 0.29个百分点
- 美元指数DXY: query_indicators(dollar_index, openbb, 2026-11-13) = 122.6503
- VIX: query_indicators(vix, openbb, 2026-11-13) = 19.3（⚠️ 旧值，11-20收盘以新闻源35替代）
- 高收益债利差: query_indicators(high_yield_spread, openbb, 2026-11-13) = 3.23个百分点
- 原油(布伦特口径): query_indicators(crude_oil, openbb, 2026-11-11) = 89.62美元/桶
- 中国10年期国债: query_indicators(bond_10y_yield, akshare, 2026-11-23) = 1.5861%
- 中国2年期国债: query_indicators(bond_2y_yield, akshare, 2026-11-23) = 1.2351%
- 有效联邦基金利率: query_indicators(fed_funds_rate, openbb, 2026-10-01) = 3.88%
- S&P500 / Gold / USDCNH: query_indicators(time_range=7d) 返回 None（⚠️缺，S&P500与Gold以新闻源补充，USDCNH不臆造）

## 五、新闻源（query_raw_items，引用即打分）
- 纳指逼近技术性熊市、VIX一度突破40、标普道指进入回调: query_raw_items(keyword='美联储 OR FOMC', published_after=2026-11-16)[id:808018] = 本周美股大幅下挫，纳指逼近技术性熊市，VIX一度突破40，投资者寻求美债避难，下周PCE或进一步清晰反映美联储态度
- 上周五美股全线重挫、纳指-5%、英伟达-14%、VIX破35: query_raw_items(keyword='英伟达 OR 13F', published_after=2026-11-16)[id:808816] = 上周五美股全线重挫，纳指收跌逾5%，英伟达暴跌14%，VIX涨破35；美债五连涨，现货黄金跌近3%；英伟达再遭SEC调查，股价较10月高点腰斩
- 摩根大通：回调由AI交易去杠杆驱动: query_raw_items(keyword='美联储 OR FOMC', published_after=2026-11-16)[id:808853] = 近期风险资产回调主要由AI相关交易去杠杆化所致，同时市场计入美联储更鹰派反应；杠杆下降与持仓改善支撑AI超级周期持续性
- CME 12月加息25bp概率91.4%: query_raw_items(keyword='美联储 OR FOMC', published_after=2026-11-16)[id:808736] = 据CME美联储观察，12月维持利率不变概率8.6%，加息25bp概率91.4%，加息50bp概率0%；到明年1月累计加息50bp概率57.7%
- 机构预测10月PCE同比3.8%: query_raw_items(keyword='美联储 OR FOMC', published_after=2026-11-16)[id:807996] = 彭博调查预计10月实际PCE环比+0.1%，PCE价格指数同比+3.8%，通胀压力或进一步加剧
- 贝森特警告美联储过度紧缩、金融体系脆弱: query_raw_items(keyword='美联储 OR FOMC', published_after=2026-11-16)[id:808550] = 美国财长贝森特警告美联储若针对最新通胀数据过度收紧可能危及经济，指出过去几个月金融环境大幅收紧、金融体系出现脆弱迹象
- 高盛：恐慌抛售或现机会但这次不同: query_raw_items(keyword='美联储 OR FOMC', published_after=2026-11-16)[id:808695] = 高盛称恐慌通常是买入机会，但当前美联储处于加息周期、持仓结构复杂；对冲基金普遍极度悲观且杠杆降至五年低点，其他投资者仓位仍高
- 黄金创3月以来最大单周跌幅: query_raw_items(keyword='美联储 OR FOMC', published_after=2026-11-16)[id:808588] = 黄金连续第五天下跌，创3月以来最大单周跌幅，周五约3500美元/盎司，本周跌近9%，白银五日跌逾15%
- MSCI新兴市场股票指数跌入熊市: query_raw_items(keyword='美联储 OR FOMC', published_after=2026-11-16)[id:808547] = MSCI新兴市场股票指数跌入熊市，AI股下跌重创指数，美联储表示AI推高通胀和利率打击大宗商品与EM货币
- 美银Hartnett：标普6845点是加息变数: query_raw_items(keyword='美联储 OR FOMC', published_after=2026-11-16)[id:807945] = 美银Hartnett称阻止美联储加息最快方式是让标普回吐2026年全部涨幅，对应6845点，上周五收6910点，距离仅65点约1%
- 华泰港股策略：短期密集压力或接近峰值: query_raw_items(keyword='美联储 OR FOMC', published_after=2026-11-16)[id:808880] = 全球AI产业链短期大幅回调，纳指、费半周跌10.0%、17.1%，美联储表态鹰派，大类资产除美元几乎全面调整，呈现流动性紧张迹象
- 中信证券：2027年AI产业链阶段性特征: query_raw_items(keyword='英伟达 OR 13F', published_after=2026-11-16)[id:808157] = 英伟达与Anthropic财报后标普自高点回调11.6%，纳指100陷入熊市，VIX创去年对等关税以来新高；判断2027年AI产业链年初估值承压、年中修复、年末分化


## 六、英伟达重大事件与公司维度（ackman 接力补充，2026-11-23 查询）

- 黄仁勋回归CEO: query_longbridge_by_route(news/company, symbol=NVDA.US) = 董事会一致重新任命黄仁勋为总裁/CEO/董事，此前因针对其的外国情报调查由Colette Kress任临时CEO，美国政府确认无国家安全风险；董事会设立国家安全与出口管制委员会并聘任首席合规官（2026-11-23 05:55 UTC）
- 美股一年多来最佳单日: query_longbridge_by_route(news/company, symbol=NVDA.US) = 标普500 +4.7%、纳指 +7%，为一年多来最佳单日，由黄仁勋回归重燃AI热情驱动（2026-11-23 21:51 UTC）
- NVDA实时报价: market_quote(symbols=[NVDA.US]) = 165.05美元，+39.52（+31.48%），成交额1281.07亿美元（2026-11-23）
- NVDA年初至今: query_longbridge_by_route(news/company) = 尽管单日+31.48%，年初至今仍-11.3%（2026-11-23）
- NVDA FY2027 Q3营收: query_longbridge_by_route(fundamental/consensus, symbol=NVDA.US) = 实际1158.44亿美元 vs 预期1087.11亿美元（Beat，+6.6%）
- NVDA FY2027 Q3净利润/EPS: query_longbridge_by_route(fundamental/consensus) = GAAP净利润652.87亿 vs 预期605.43亿（Beat）；EPS 2.70 vs 预期2.46（Beat）
- NVDA FY2027 Q4一致预期: query_longbridge_by_route(fundamental/consensus) = 营收1308.14亿美元、EPS 2.86（未发布）
- NVDA估值PE: query_longbridge_by_route(fundamental/valuation/pe, symbol=NVDA.US) = 当前28.65x，历史区间28.65~44.68x，中位数34.12x（处于历史低位）
- 消费股成AI反弹资金来源: query_longbridge_by_route(news/company) = 黄仁勋回归当日，Tyson/Kroger/General Mills等防御性消费股领跌，资金从防御转向AI（2026-11-23 17:54 UTC）
