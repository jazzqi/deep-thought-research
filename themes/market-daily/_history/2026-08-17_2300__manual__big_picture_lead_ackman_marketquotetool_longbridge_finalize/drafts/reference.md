# 数据来源 Reference

## 美国宏观数据
- 美国7月CPI同比3.4%（前值3.5%）、核心CPI同比2.5%（前值2.6%）、CPI环比+0.1%（前值-0.4%）、核心环比+0.2%（前值0.0%）: query_calendar_events(country="US", days=14, importance="high") = 2026-08-12公布
- 美国7月PPI同比4.7%（前值5.5%）: query_calendar_events(country="US", days=14, importance="high") = 2026-08-13公布
- 美国7月零售销售环比-0.6%（预期+0.1%，前值+0.2%）: query_calendar_events(country="US", days=14, importance="high") = 2026-08-14公布
- 美国8月8日当周初请失业金20.9万人（预期20.2万，前值19.9万）: query_calendar_events(country="US", days=14, importance="high") = 2026-08-13公布
- 美国7月ADP就业+4.4万人（预期+6.5万，前值+9.8万）: query_calendar_events(country="US", days=14, importance="high") = 2026-08-05公布
- 美国6月JOLTS职位空缺735.9万（预期740万，前值759.4万）: query_calendar_events(country="US", days=14, importance="high") = 2026-08-04公布
- 美国7月ISM非制造业指数54.1（预期54.5，前值54.0）: query_calendar_events(country="US", days=14, importance="high") = 2026-08-05公布
- 美国6月贸易帐-733亿美元（预期-730亿，前值-776亿）: query_calendar_events(country="US", days=14, importance="medium") = 2026-08-04公布
- 美国联邦储备资产负债表（2026-08-12）: query_indicators(category="macro", country="us") = 6,759,955.0（百万美元）
- 美国7月NFIB小企业乐观指数99.8（前值97.4）: query_calendar_events(country="US", days=14, importance="high") = 2026-08-11公布
- 美国7月成屋销售406万套（预期405万，前值409万）: query_calendar_events(country="US", days=14, importance="high") = 2026-08-11公布

## 中国宏观数据
- 中国7月CPI同比0.5%: query_indicators(country="china", time_range="7d") = 前版index.md引用
- 中国7月制造业PMI 49.2、非制造业PMI 49.0: query_indicators(country="china", time_range="7d") = 前版index.md引用
- 中国1-7月社会消费品零售总额同比1.2%（前值1.3%）: query_calendar_events(country="CN", days=7, lookback_days=3, importance="high") = 2026-08-17公布
- 中国1-7月城镇固定资产投资同比-6.7%（前值-5.7%）: query_calendar_events(country="CN", days=7, lookback_days=3, importance="high") = 2026-08-17公布

## 美联储/FOMC
- 美联储7月28-29日FOMC会议：维持利率3.50-3.75%: query_fomc(lookback_days=60, lookahead_days=60) = target_range 3.50-3.75%
- 下次FOMC会议：2026年9月15-16日（含SEP点阵图）: query_fomc(lookback_days=60, lookahead_days=60)
- 9月加息概率从7月末75%降至33%: query_raw_items(keyword="Fed OR 加息")[id:125833] = 美股存储巨头盘前普涨…美联储加息预期生变，9月加息概率已降至约33%

## 地缘政治
- 伊朗与美国60天MoU延长协议获批准（沙特媒体报道）: query_raw_items(keyword="伊朗 OR Iran")[id:126023] = 沙特方面消息…伊朗与美国之间60天期限的延长协议已获批准。美、布两油短线下挫逾1美元
- 霍尔木兹海峡8月16日仅3艘次通行（正常118艘次/周）: query_raw_items(keyword="伊朗 OR Iran")[id:126698] = 海事分析机构MarineTraffic：上周霍尔木兹海峡船舶通行量从118艘次降至95艘次
- 伊朗官员：已为美国履行MoU设定数周最后期限，政策"从防御性转向全面进攻性": query_raw_items(keyword="伊朗 OR Iran")[id:126684] = 一名伊朗高级官员17日…
- 伊朗革命卫队否认与美国存在秘密渠道: query_raw_items(keyword="伊朗 OR Iran")[id:126539] = 伊朗革命卫队否认与美有秘密渠道
- 特朗普威胁阿曼、威胁将霍尔木兹海峡变为美国领土: query_raw_items(keyword="伊朗 OR Iran")[id:126681] = Trump threatens to bomb Oman
- 美国宣布对加拿大部分产品加征50%关税: query_calendar_events(country="US", days=14, importance="high") = 2026-08-17
- 加拿大7月CPI同比3.0%（预期2.9%，前值2.8%）: query_raw_items(keyword="关税 OR tariff OR Canada")[id:126366] = 加拿大7月核心CPI年率2.3%，前值2.1%
- 特朗普女婿库什纳访问以色列推动加沙和平: query_raw_items(keyword="war OR 战争")[id:126280] = USS Washington to relieve USS Lincoln. And, Jared Kushner to meet with Netanyahu

## 股市/行情
- 美股开盘（2026-08-17）：道指-0.24%，标普500+0.04%，纳指+0.19%: query_raw_items(keyword="美股")[id:126552] = 美股开盘：三大股指涨跌不一
- 七姐妹涨跌：亚马逊+0.80%，英伟达+0.79%，苹果+0.39%，谷歌+0.20%，Meta-0.70%，特斯拉-1.00%，微软-1.04%: query_raw_items(keyword="美股")[id:126552]
- 存储板块：闪迪+10.5%，美光+5.7%，SK海力士+6.5%: query_raw_items(keyword="美股")[id:126686]
- 半导体设备：AXT+11%，应用材料+5%: query_raw_items(keyword="美股")[id:126599]
- 网络安全走弱：Cloudflare-3%，CrowdStrike-1%: query_raw_items(keyword="美股")[id:126597]
- 耐克跌至2014年以来最低（年内-37%）: query_raw_items(keyword="美股")[id:126671]
- 华住美股开盘+8%（Q2营收+10.8%至71亿元）: query_raw_items(keyword="美股")[id:126567]
- 阿里巴巴+1.6%（以15亿美元出售游戏业务）: query_raw_items(keyword="美股")[id:126551]

## 大宗商品
- 现货黄金突破4,420美元/盎司（日内+1.04%）: query_raw_items(keyword="gold OR 黄金")[id:126640] = 现货黄金突破4420美元/盎司
- 现货黄金15分钟内拉升逾20美元至4,404美元/盎司: query_raw_items(keyword="gold OR 黄金")[id:126596]
- WTI原油81.64美元/桶（+0.48%），布伦特87.23美元/桶（+0.18%）: query_raw_items(keyword="美股")[id:126511]
- 富国下调2026年底黄金目标价至4,900-5,100美元（此前5,300-5,500）: query_raw_items(keyword="gold OR 黄金")[id:126563]
- LME铜14,363.50美元/吨（+1.4%），年初至今+16%: query_raw_items(keyword="关税 OR tariff")[id:125020]
- 国际储备管理机构自2025年4月对等关税以来削减美债持有逾3,000亿美元: query_raw_items(keyword="美债")[id:124761]

## AI/科技
- 英伟达与OpenAI签署俄亥俄州12GW数据中心协议，OpenAI承诺至2030年部署约6,000亿美元英伟达算力: query_raw_items(keyword="英伟达 OR NVDA")[id:126467] = 英伟达公司：OpenAI的相关承诺意味着…6000亿美元的英伟达算力采购规模
- 初始支付义务上限1,050亿美元（SEC文件）: query_raw_items(keyword="英伟达 OR NVDA")[id:126462] = 英伟达：根据提交给SEC的文件，初始承诺的支付义务上限为1050亿美元
- SB Energy将以20年期租约运营数据中心: query_raw_items(keyword="英伟达 OR NVDA")[id:126439] = 英伟达：SB Energy将运营数据中心，向OpenAI提供20年期租约
- Ports-Pike项目每代系统约150万颗GPU: query_raw_items(keyword="英伟达 OR NVDA")[id:126452]
- NVIDIA盘中+0.8%: query_raw_items(keyword="英伟达 OR NVDA")[id:126557] = 英伟达(NVDA.O)上涨0.8%
- Synchrony与OpenAI达成企业合作（部署GPT-5.6 Sol/Terra/Luna）: query_raw_items(keyword="AI")[id:126711] = 美国金融服务公司Synchrony宣布与OpenAI达成企业合作协议
- DeepSeek API涨价（8月17日起峰值价格最高涨至27元）: query_calendar_events(country="CN", days=7, lookback_days=3, importance="high") = 2026-08-15/16
- 阿里巴巴以15亿美元出售游戏业务: query_raw_items(keyword="美股")[id:126551]
- 伯克希尔二季度继续加仓Alphabet: query_raw_items(keyword="美股")[id:126551]
- 桥水二季度持仓增至244亿美元，加仓标普500ETF、减持亚马逊等科技股: query_raw_items(keyword="美股")[id:126051]

## 机构观点
- 高盛：标普500成分股Q2营收同比+6.4%（五年最快），企业盈利同比+50%，收到超1,000亿美元关税退款: query_raw_items(keyword="美股")[id:126520]
- 高盛：市场对Fed政策押注仍太鹰，9月加息"可能性非常小": query_raw_items(keyword="美股")[id:126511]
- 摩根大通：股票买盘群体范围"广泛"，内部指标7月末发出买入信号后标普已涨约5%: query_raw_items(keyword="美股")[id:126580]
- 摩根大通：本周关注周三Fed会议纪要，下周关注英伟达财报和杰克逊霍尔会议: query_raw_items(keyword="美股")[id:126580]
- Evercore ISI：标普500可在12个月内达9000点（+16%）: query_raw_items(keyword="美股")[id:126543]
- 大摩、小摩齐看标普8000点: query_raw_items(keyword="美股")[id:126511]
- 欧洲央行：美股科技股估值处"亢奋"水平，回调"可能产生广泛影响": query_raw_items(keyword="美股")[id:125798]
- 富国投资研究所：预计Fed今年加息25bp、2027年再加25bp至4.00-4.25%: query_raw_items(keyword="鲍威尔 OR Powell OR Fed")[id:126541]
- 富国下调黄金目标价: query_raw_items(keyword="gold OR 黄金")[id:126563]
- 法兴银行：疲软美国数据促使美元看涨押注减少: query_raw_items(keyword="鲍威尔 OR Powell OR Fed")[id:126283]
- 摩根士丹利：外汇低波动性或持续至9月初: query_raw_items(keyword="鲍威尔 OR Powell OR Fed")[id:126248]
- 浦银国际：港股最差阶段或已过去，反弹仍未结束: query_raw_items(keyword="腾讯")[id:125694]

## 新兴市场/外汇
- 美元跌至三个月低点（5月15日以来最低）: query_raw_items(keyword="美元 OR dollar")[id:125957]
- 新兴市场货币指数触及历史新高1906.98: query_raw_items(keyword="鲍威尔 OR Powell OR Fed")[id:125182]
- 美元指数跌至10周低点: query_raw_items(keyword="美元 OR dollar")[id:125719]
