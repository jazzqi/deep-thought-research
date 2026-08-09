- SPY现价/日涨幅: market_quote(symbols=["SPY.US"]) = 773.26 / +0.61%
- QQQ现价/日涨幅: market_quote(symbols=["QQQ.US"]) = 723.03 / +1.17%
- GLD现价/日涨幅: market_quote(symbols=["GLD.US"]) = 398.47 / +2.26%
- 腾讯控股现价/日涨幅: market_quote(symbols=["0700.HK"]) = 478.80 HKD / -0.08%
- SPY日线技术状态: market_kline(symbol="SPY.US",period="1d",count=60,secondary_period="1w") = EMA21 752.87>EMA60 745.73；RSI14 65.878；距60日高点-0.5%；布林位置0.9672
- 腾讯日线技术状态: market_kline(symbol="0700.HK",period="1d",count=60,secondary_period="1w") = EMA21 467.62>EMA60 453.24；RSI14 55.73；波动分位11
- 美国初请/续请失业金: query_indicators(country="us") = 199,000（数据2026-08-01）/1,801,000（数据2026-07-25）
- 美国高收益利差/VIX/10年期收益率: query_indicators(country="us") = 2.71（2026-08-06）/15.15（2026-08-06）/4.69%（2026-08-06）
- 中国7月CPI同比/制造业PMI/非制造业PMI: query_indicators(country="china") = 0.5%/49.2/49.0
- 美国7月CPI发布日及市场预期: query_calendar_events(country="US",days=14,importance="high,medium") = 2026-08-12；CPI同比3.5%，核心CPI同比2.5%
- 美国7月PPI发布日: query_calendar_events(country="US",days=14,importance="high,medium") = 2026-08-13
- 上海台风交通影响: query_raw_items(source="telegram:Financial_Express",limit=50) = 2026-08-09上海全域长途客运班次停运、部分轨交线路15时起停运


- 美国7月CPI（8月12日）主条目预期/前值: query_calendar_events(country="US", days=14, importance="high,medium", limit=30) = 3.4% / 3.5%；同一返回含重复CPI同比条目预期3.5%，存在冲突
- 美国7月核心CPI（8月12日）预期/前值: query_calendar_events(country="US", days=14, importance="high,medium", limit=30) = 2.5% / 2.6%
- 美国7月CPI、核心CPI环比预期: query_calendar_events(country="US", days=14, importance="high,medium", limit=30) = 0.2% / 0.2%
- 美国7月PPI、核心PPI同比前值及预期缺口: query_calendar_events(country="US", days=14, importance="high,medium", limit=30) = 5.5% / 4.7%；forecast=null

- 2026-08-09近30日腾讯相关新闻：query_raw_items(keyword="腾讯",limit=30) = Hy ASR 3.0 preview（2026-08-04）、AngelSpec开源（2026-07-29）、TDSQL-C MySQL架构2.0商业化计费（2026-07-27）、预计2026年第四季度部署国产化NPO超级节点（2026-07-21）、WorkBuddy国内PC端AI原生办公智能体6月访问量据报道超2000万（2026-07-20）、腾讯云ADP 4.0海外版发布（2026-07-20）、腾讯与DeepSeek等获宇树科技战略配售（2026-08-06） = 见原始新闻条目
- 2026-08-09美国7月CPI日历：query_calendar_events(country="US",days=14,importance="high,medium",limit=50) = 同比预期3.4%（前值3.5%）、核心同比预期2.5%（前值2.6%）、CPI环比预期0.2%（前值-0.4%）、核心环比预期0.2%（前值0.0%）；另有重复同比预期3.5%条目，存在冲突
- 2026-08-09美国7月PPI日历：query_calendar_events(country="US",days=14,importance="high,medium",limit=50) = PPI同比前值5.5%、核心同比前值4.7%，环比预期0.2%、核心环比预期0.3%
- 2026-08-09美国长债供给及10年期拍卖：query_calendar_events(country="US",days=14,importance="high,medium",limit=50) = 8月11日至13日标售逾千亿美元国债；8月12日10年期国债竞拍总金额390亿美元，前值中标/高收益率4.58%
- 2026-08-09最新宏观与跨资产快照：query_indicators(country="us",time_range="7d") = 10年期美债收益率4.69%（2026-08-06）、高收益利差2.71%（2026-08-06）、VIX 15.15（2026-08-06）；query_indicators(country="china",time_range="7d") = 7月CPI同比0.5%、制造业PMI 49.2、非制造业PMI 49.0
- 2026-08-09市场行情：reference.md既有记录market_quote(SPY.US)=773.26/+0.61%、QQQ.US=723.03/+1.17%、GLD.US=398.47/+2.26%、0700.HK=478.80港元/-0.08%；腾讯日线EMA21 467.62>EMA60 453.24、RSI14 55.73、波动分位11 = market_kline

- 腾讯公司新闻（2026-08-07）：下周将公布腾讯Q2财报，且美国7月CPI/PPI将发布: query_longbridge_by_route(news/company, {"symbol":"700.HK","count":30}) = Longbridge新闻条目295212059
- 腾讯云 Agent Memory 2.0.0上线（2026-08-06）: query_longbridge_by_route(news/company, {"symbol":"700.HK","count":30}) = Longbridge新闻条目295072240
- DeepSeek计划提高API价格、V4即将发布（2026-08-06）: query_longbridge_by_route(news/company, {"symbol":"700.HK","count":30}) = Longbridge新闻条目295054571
- 南向资金2026-08-07分别在沪港通、深港通净卖出腾讯9.05亿港元、12.83亿港元: query_longbridge_by_route(news/company, {"symbol":"700.HK","count":30}) = Longbridge新闻条目295211148
- 美国联邦储备资产负债表（2026-08-05）: query_indicators({"category":"macro","country":"us","limit":20,"time_range":"7d"}) = 6,748,567.0（数据库原始单位）
- 美国7月零售销售（2026-08-14）日历: query_calendar_events({"country":"US","days":30,"importance":"high,medium","limit":100}) = 环比预期0.3%，前值0.2%

- 美国10年期国债收益率（2026-08-06）: query_indicators(country="us",category="bond",time_range="7d") = 4.69%
- 美国2年期国债收益率（2026-08-06）: query_indicators(country="us",category="bond",time_range="7d") = 4.25%
- 美国VIX（2026-08-06）: query_indicators(country="us",category="sentiment",time_range="7d") = 15.15
- 美国高收益债利差（2026-08-06）: query_indicators(country="us",category="bond",time_range="7d") = 2.71%
- 美国投资级公司债利差（2026-08-06）: query_indicators(country="us",category="bond",time_range="7d") = 0.78%
- SPY收盘价及日涨幅: 既有稿件reference.md记录 = 773.26美元、+0.61%
- QQQ收盘价及日涨幅: 既有稿件reference.md记录 = 723.03美元、+1.17%
- GLD收盘价及日涨幅: 既有稿件reference.md记录 = 398.47美元、+2.26%
- 腾讯控股收盘价及日涨幅: 既有稿件reference.md记录 = 478.80港元、-0.08%
- 腾讯21日/60日EMA及RSI14: 既有稿件reference.md记录 = 467.62/453.24、55.73
- 中国7月CPI同比: query_indicators(country="china",time_range="7d") = 0.5%
- 中国制造业PMI、非制造业PMI: query_indicators(country="china",time_range="7d") = 49.2、49.0
- 美国7月CPI日历预期及前值: query_calendar_events(country="US",days=30,importance="high,medium",limit=100) = 同比预期3.4%（另有重复条目3.5%）、前值3.5%；核心同比预期2.5%、前值2.6%；环比预期0.2%、前值-0.4%；核心环比预期0.2%、前值0.0%
- 美国7月PPI日历预期及前值: query_calendar_events(country="US",days=30,importance="high,medium",limit=100) = PPI同比前值5.5%、核心同比前值4.7%；环比预期0.2%、核心环比预期0.3%
- 美国8月12日10年期国债竞拍: query_calendar_events(country="US",days=30,importance="high,medium",limit=100) = 发行390亿美元，前次高收益率4.58%
- 美国7月零售销售日历: query_calendar_events(country="US",days=30,importance="high,medium",limit=100) = 环比预期0.3%、前值0.2%；除汽车与汽油环比预期0.3%、前值0.4%
- 腾讯下周发布第二季度财报: query_longbridge_by_route(path="news/company",params={"symbol":"700.HK","count":30}) = 2026-08-07新闻称下周公布
- 腾讯南向资金净卖出: query_longbridge_by_route(path="news/company",params={"symbol":"700.HK","count":30}) = 2026-08-07沪港通9.05亿港元、深港通12.83亿港元
- 腾讯云Agent Memory 2.0.0: query_longbridge_by_route(path="news/company",params={"symbol":"700.HK","count":30}) = 2026-08-06上线，新增团队记忆能力
- DeepSeek API提价及V4: query_longbridge_by_route(path="news/company",params={"symbol":"700.HK","count":30}) = 2026-08-06报道计划提价并推进V4
- 腾讯Hy3全球可用: query_longbridge_by_route(path="news/company",params={"symbol":"700.HK","count":30}) = 2026-08-05报道，295B参数MoE并接入WorkBuddy、Miora、腾讯云TokenHub
- 美国财政部8月11-13日国债发行: query_calendar_events(country="US",days=30,importance="high,medium",limit=100）= 逾千亿美元
- 伊朗处于“非战非和”僵局: query_raw_items(source="aljazeera",keyword="Iran",limit=100) = 2026-08-09报道


- 2026-08-09 Meta监管裁决：query_longbridge_by_route(path="news/company",params={"symbol":"META.US","count":50}) = 2026-08-09条目称新墨西哥州法院判Meta向该州青少年心理健康基金支付5.67亿美元；条目同时称加此前3.75亿美元，案件合计9.42亿美元（需以法院文件/公司披露复核）
- 2026-08-08 英伟达潜在基础设施投资：query_longbridge_by_route(path="news/company",params={"symbol":"NVDA.US","count":50}) = Reuters转载条目称The Information报道英伟达拟向Blackstone支持的Lancium最高投资30亿美元，首期20亿美元对应20%股权；英伟达与Lancium当时未回应（报道，非公司确认）
- 2026-08-08 Alphabet近期融资与AI业务：query_longbridge_by_route(path="news/company",params={"symbol":"GOOGL.US","count":50}) = 条目称Alphabet Q2 Google Cloud销售额248亿美元、同比+82%，并开始向外部客户销售TPU；另有条目称其拟发行最高250亿美元债券（新闻报道，数值需以公司财报/发行文件复核）
- 2026-08-08 Amazon资本开支/现金流：query_longbridge_by_route(path="news/company",params={"symbol":"AMZN.US","count":50}) = 条目称Amazon将2026年AI资本开支上调至2200亿美元；另一条目称其Q2营收2006亿美元、AWS同比+37%、重资本开支使自由现金流转负（新闻报道，需以财报复核）
- 2026-08-08 Microsoft最新业绩线索：query_longbridge_by_route(path="news/company",params={"symbol":"MSFT.US","count":50}) = 条目称微软最近季度EPS 4.74美元、营收900.1亿美元、超过预期（新闻报道，需以公司财报复核）
- 2026-08-02 腾讯竞争性用户时长信号：query_raw_items(keyword="腾讯",limit=50) = 36kr条目称字节系移动互联网用户时长占比首次超过腾讯系、达40.1%（报道口径，需核验统计方法）

- 2026-08-09 Meta监管裁决: query_longbridge_by_route(path="news/company",params={"symbol":"META.US","count":50}) = 条目称新墨西哥州法院判Meta向该州青少年心理健康基金支付5.67亿美元；条目同时称加此前3.75亿美元，合计9.42亿美元，需以法院文件/公司披露复核
- 2026-08-08 英伟达潜在基础设施投资: query_longbridge_by_route(path="news/company",params={"symbol":"NVDA.US","count":50}) = Reuters转载条目称The Information报道英伟达拟向Blackstone支持的Lancium最高投资30亿美元，首期20亿美元对应20%股权；英伟达与Lancium未回应，属于报道非公司确认
- 2026-08-08 Alphabet近期业务与融资: query_longbridge_by_route(path="news/company",params={"symbol":"GOOGL.US","count":50}) = 条目称Q2 Google Cloud销售额248亿美元、同比+82%，并开始向外部客户销售TPU；另称拟发行最高250亿美元债券，数值需以财报/发行文件复核
- 2026-08-08 Amazon资本开支与现金流: query_longbridge_by_route(path="news/company",params={"symbol":"AMZN.US","count":50}) = 条目称2026年AI资本开支上调至2200亿美元；另称Q2营收2006亿美元、AWS同比+37%、重资本开支使自由现金流转负，需以公司财报复核
- 2026-08-06 Microsoft AI收入集中度线索: query_raw_items(keyword="Microsoft",limit=30) = hackernews条目称微软披露文件显示约70%的AI收入来自OpenAI，属于二手报道，需查原始申报文件复核
- 2026-08-02 腾讯竞争性用户时长: query_raw_items(keyword="腾讯",limit=50) = 36kr条目称字节系移动互联网用户时长占比首次超过腾讯系、达40.1%，统计口径需核验
- 2026-08-09 Meta监管裁决线索: query_longbridge_by_route(path="news/company",params={"symbol":"META.US","count":50}) = 条目称新墨西哥州法院判Meta向该州青少年心理健康基金支付5.67亿美元，另称此前3.75亿美元、合计9.42亿美元；新闻条目，需法院文件/公司披露复核
- 2026-08-08 英伟达潜在基础设施投资: query_longbridge_by_route(path="news/company",params={"symbol":"NVDA.US","count":30}) = Reuters转载条目称The Information报道英伟达拟向Lancium最高投资30亿美元，首期20亿美元对应20%股权；公司当时未回应，属报道非确认
- 2026-08-08 Alphabet AI业务与融资线索: query_longbridge_by_route(path="news/company",params={"symbol":"GOOGL.US","count":50}) = 条目称Q2 Google Cloud销售额248亿美元、同比+82%，并开始向外部客户销售TPU；另称拟发行最高250亿美元债券，均需公司财报/发行文件复核
- 2026-08-08 Amazon AI资本开支与现金流线索: query_longbridge_by_route(path="news/company",params={"symbol":"AMZN.US","count":50}) = 条目称2026年AI资本开支上调至2200亿美元，且Q2营收2006亿美元、AWS同比+37%、重资本开支使自由现金流转负；新闻报道，需公司财报复核
- 2026-08-06 Microsoft AI收入集中度线索: query_raw_items(keyword="Microsoft",limit=20) = hackernews条目称微软披露文件显示约70%的AI收入来自OpenAI；二手报道，需原始申报文件复核
- 2026-08-02 腾讯竞争格局: query_raw_items(keyword="腾讯",limit=50) = 36kr条目称字节系移动互联网用户时长占比首次超过腾讯系、达40.1%；报道口径，需核验统计方法
- 2026-08-04 腾讯音乐与SM娱乐合资: query_raw_items(keyword="腾讯",limit=50) = 36kr条目称腾讯音乐与SM娱乐在北京成立合资公司，注册资本4000万；新闻条目，需公司公告复核