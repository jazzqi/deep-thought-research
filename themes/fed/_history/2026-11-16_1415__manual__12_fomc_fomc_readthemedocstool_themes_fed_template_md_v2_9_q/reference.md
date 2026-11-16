# 数据来源溯源（2026-11-16 本期）

- 政策利率决议历史（7月9-3维持3.50-3.75%反对者Hammack/Kashkari/Logan要求加息；9月16日12-0加息至3.75-4.00%含SEP中值4.1%；10月28日10-2维持反对者Cook/Hammack要求加息）: query_fomc(lookback_days=120, lookahead_days=365, limit=20) = target_range 3.75–4.00% (as of 2026-10-28)
- 未来FOMC会议（12/8-9 SEP会议、2027/1/26、3/16、4/27、6/8、7/27、9/14、10/26、11/16）: query_fomc(lookahead_days=365) = next_meeting 2026-12-08
- 10月CPI环比0.4%（前值0.6%、预测0.3%）/核心CPI环比0.3%（前值0.3%、预测0.2%）/9月CPI同比3.7%: query_calendar_events(country=US, days=180, lookback_days=14, limit=200) = 2026-11-10发布；同比actual工具未返回⚠️（另一行返回0.17与叙事冲突，已标⚠️双口径）
- 10月PPI同比6.5%（前值6.3、预测6.6）、环比0.3%（预测0.4、前值上修1.4）: query_calendar_events + query_raw_items(keyword='10月CPI OR PPI')[id:774908] = 创四年新高
- 10月非农+16.5万（预期+6.5万、前值+2.9万）、失业率4.1%（预期4.2、前值4.2）、平均时薪同比3.1%/环比0.4%、劳动参与率61.9%、U-6 7.9%: query_calendar_events(2026-11-06发布)
- 9月JOLTS职位空缺752.3万（前值707.9、预测710）: query_calendar_events(2026-11-03)
- 初请：11/12当周20.0万（前值18.9、预测19.4）、11/5当周18.9万；续请171.8万（前值170.1）: query_calendar_events(2026-11-12/11-05)
- 10月ISM制造55.5（预测54.6、前值54.5）、非制造54.5（预测54.8、前值54.9）、制造业物价支付75.2（前值77.9）: query_calendar_events(2026-11-02/11-04)
- 11月密歇根信心初值51.0（前值48.0、预期48.2）、1年通胀预期4.3（前值4.7）、现况51.0/预期50.9: query_calendar_events(2026-11-06)
- 10月零售销售（11-17发布，前值+0.8%、预测+0.2%）: query_calendar_events(未来事件)
- 10月PCE未发布/9月PCE超14天窗口未返回→数据缺失；鲍曼预计10月核心PCE同比3.3%: themes/fed/roundtable/fomc_member_news.md（2026-11-10/11讲话）
- CME FedWatch：12月加息25bp概率95%、50bp概率5%；到明年1月累计+25bp 25.2%、+50bp 71.1%、+75bp 3.7%: query_raw_items(keyword='FedWatch OR 加息预期 OR 12月加息')[id:781254][id:781351] = 2026-11-15/16
- 讨论焦点转向明年1月、10月CPI连续第三个月超预期、开启2023年以来首次连续加息可能性: query_raw_items[ id:780937 ] = 2026-11-15
- 10Y美债收益率重返5%以上、高盛将明年3月加息纳入基准: query_raw_items[ id:781618 ] = 2026-11-16
- 桑坦德：12月与明年3月各加息25bp: query_raw_items[ id:777474 ] = 2026-11-13
- 美元指数102.85（2025年4月以来最高）、日元逼近160: query_raw_items[ id:751635 ] = 2026-11-11
- 黄金跌破4000美元、周跌4.6%（6月以来最大单周跌幅）: query_raw_items[ id:752213 ][ id:782189 ] = 2026-11-11/16
- 2027年FOMC暂定8次会议、10月26-27日会议专议货币政策战略（次日不发决议）: query_raw_items[ id:768316 ] = 2026-11-12
- 机构：CPI与PPI定调PCE、整体物价高企强化加息预期: query_raw_items[ id:775518 ] = 2026-11-13
- 策略师：鹰派加息利好美元但易受预期重置冲击: query_raw_items[ id:775065 ] = 2026-11-13
- FOMC成员名单/票委轮换/主席Warsh（官网Last Update 2026-10-28）: themes/fed/FOMC_MEMBERS.md (federalreserve.gov/monetarypolicy/fomc.htm)
- 成员近期言论（Warsh会议机制改革11-06、Williams 11-13、Barr 11-12、Bowman 11-10/11、Hammack 11-12、Jefferson 11-14、Kashkari 10-01/02、Logan 11-13、Paulson 11-10/11、Waller 11-10/11、Barkin 11-09、Daly 11-13、Goolsbee 11-13）: themes/fed/roundtable/fomc_member_news.md (longbridge/telegram:Financial_Express 预采集)
- 美联储资产负债表6.8万亿美元（2026-11-04）: query_calendar_events = "美国截至11月4日美联储资产负债表"
- 30年期房贷利率7.30%（前值7.37）: query_calendar_events(2026-11-04 MBA)
- 10年期国债拍卖中标收益率5.02%（前次5.30%）: query_calendar_events(2026-11-10 auction) ⚠️与另一行2.46口径冲突待核
- 季度再融资1250亿美元（11月9-11日）: query_calendar_events(2026-11-08事件)
- 三季度GDP修正值3.4%（11-25待发布）、单位劳动力成本-0.7%/生产力+3.6%（11-05初值）: query_calendar_events
- FactPack锚点（9月FedWatch维持59.9%/加息40.1%，2026-08-26）: 系统只读锚点


## 本轮（接力第 2 棒 · soros）新增溯源

- 美元指数盘中 103.46（创 2025 年 4 月以来新高）: query_raw_items(keyword='美元 OR DXY')[id:782105] = dalio 第 1 轮引用 2026-11-16
- 美银将未来三次会议连续加息纳入预测: query_raw_items(keyword='Fed OR 美联储 OR FOMC')[id:778263] = taleb 第 1 轮引用 2026-11
- 鲍曼承认股价下跌/收益率上升/美元走强本身已收紧金融条件: query_raw_items[ id:741973 ] = kahneman 第 1 轮引用 2026-11
- Waller：12 月支持加息、若通胀加速应讨论一次性 50bp: query_raw_items[ id:781413 ] = 2026-11-10/11（正文另见 [id:781618]）
- Daly：核心 CPI 连续三个月环比约 0.3%、高于 2% 目标所需 0.2% 或以下: query_raw_items[ id:777208 ] = 2026-11-13
- BTC 跌破 7 万美元、周跌约 13%: query_raw_items[ id:781951 ] = 2026-11-15/16
- BTCUSDT 最新价 64,417.1 美元: binance_get_price(symbol=BTCUSDT) = 2026-11-16 约 07:19 UTC
- 铜价创四个月低点: query_raw_items[ id:782277 ] = taleb 第 1 轮引用 2026-11
- 民主党中期选举大胜、10 月 CPI 超预期压制市场情绪: query_raw_items(keyword='CPI')[id:781379] = 2026-11-16
- 沃什 11-17 北京时间 01:00 旧金山联储生产率与就业工作组听证会开幕词: query_raw_items(keyword='收益率 OR yield OR 美债')[id:782729] = 金十 2026-11-16
- 摩根士丹利：3 月前加息至 4.375% 中值并全年维持、10Y 2027Q4 至 5.00%: query_raw_items(keyword='收益率 OR yield OR 美债')[id:781514]/[id:782736] = 2026-11-16
- 黄金 3830 美元/盎司（-1.3%，2025 年 10 月以来最低）、周跌 4.6%: query_raw_items(keyword='CPI 同比 OR 通胀 OR inflation')[id:782762]/[id:782191] = 2026-11-16
- 波士顿联储 Collins 支持渐进加息: query_raw_items(keyword='Fed OR 美联储 OR FOMC')[id:781586] = longbridge 2026-11-16
- 上轮预测底稿（2026-08-30 版：9 月按兵不动为基准等）与 Cook 罢免案法律状态（最高法院已判其胜诉）: ReadThemeDocsTool(themes/fed/index.md) = revision 2026-08-30


## 审查轮交叉核验来源（soros review, 2026-11-16）
- FOMC 10-28 决议（3.75–4.00%，投票 10–2，Cook/Hammack 反对 prefer to raise，生效 10-29）: query_fomc(lookback_days=90, lookahead_days=120) = 官方 federalreserve.gov 数据
- FOMC 09-16 决议（加息 25bp 至 3.75–4.00%，12–0，SEP 中值 4.1）: query_fomc(lookback_days=90) = 官方数据
- 下次 FOMC 2026-12-08/09（sep_meeting=True；发布会/声明链接未填充）: query_fomc(lookahead_days=120) = next_meeting
- 2027-01-26/27、2027-03-16/17 会议（3 月 sep_meeting=False）: query_fomc(lookahead_days=120) = meetings
- 10月 CPI 环比 0.4（前值0.6 预期0.3）/ 核心环比 0.3（前值0.3 预期0.2）/ 同比 actual 未返回: query_calendar_events(lookback_days=14, importance=high, country=US) = 2026-11-10
- 10月 PPI 同比 6.5（前值6.3 预期6.6）: query_calendar_events(lookback_days=4, importance=high,medium, country=US) = 2026-11-13；PPI 环比 0.3（前值1.3 预期0.4）、核心 PPI 同比 5.0/环比 0.3（前值0.7）同源
- 10月非农 +16.5万 / 失业率 4.1% / 时薪同比 3.1% 环比 0.4%: query_calendar_events(lookback_days=14) = 2026-11-06
- JOLTS 752.3万（前值707.9万 预期710万）: query_calendar_events(lookback_days=14) = 2026-11-03
- 初请 20.0万（前值18.9万 预期19.4万）11-12；10-31当周续请实际 169.7（前值171.8 预期171.0）——稿件续请 171.8 与工具不一致: query_calendar_events(lookback_days=4)
- ISM 制造 55.5 / 非制造 54.5（预期 54.7 或 54.5 / 54.8 多源）: query_calendar_events(lookback_days=14) = 2026-11-02 / 11-04
- 密歇根 1Y 通胀预期 4.3（前值 4.7，11-06 初值）: query_calendar_events(lookback_days=14)
- 10Y 拍卖高得标 5.02（前值5.30）、投标倍数 2.46（前值2.77）、中标 420亿: query_calendar_events(lookback_days=14) = 2026-11-10
- 30Y 拍卖投标倍数 2.36（前值2.54）、高得标 5.441（前值5.618）: query_calendar_events(lookback_days=4) = 2026-11-12
- 联储资产负债表 6.81 万亿美元（截至 11-11，前值 6.8）: query_calendar_events(lookback_days=4) = 2026-11-12
- 10月联邦预算赤字 -4040.64 亿美元（预期 -3175、前值 -2843，11-12 公布）: query_calendar_events(lookback_days=4) = 2026-11-12
- Q3 GDP 修正值前值 3.4（11-25 待发布）: query_calendar_events(lookback_days=4) = 2026-11-25
- 11-17 零售销售环比（前值0.8，high 行预期0.2 / medium 月率行预期0.0）、11-18 FOMC 纪要 19:00 UTC: query_calendar_events(lookback_days=4)
- 票委身份：哈玛克/洛根=2026年FOMC票委、古尔斯比/戴利=2027年票委、柯林斯/穆萨莱姆=2028年票委、威廉姆斯=永久票委: query_calendar_events(lookback_days=4) 事件标题
- 沃什听证会（生产率与就业特别工作组）、11-16 当周官员密集发声: query_calendar_events(lookback_days=4) = 2026-11-15 / 11-14
- 成员言论抽查（Waller 50bp 条件性表态、Hammack/Jefferson/Daly/Paulson/Barkin/Goolsbee/Logan/Kashkari/Bowman/Cook 无 11 月言论）: roundtable/fomc_member_news.md（系统预采集）逐条对照
- Cook 施压事件独立检索: query_raw_items(keyword=Cook, published_after=2026-10-20) = NO_DATA（无新增，与稿件一致）；query_raw_items(keyword=美联储/FedWatch/沃什/PCE) 均 NO_DATA，[id] 类引用本轮无法二次核验


## taleb 交叉审查独立核验（2026-11-16）

- 英伟达Q3财报与电话会日期: query_calendar_events(days=21,country=US,lookback=0) = 2026-11-17 22:00 UTC；同日另有黄仁勋国会听证会(16:00)、Anthropic IPO定价(16:00)，Anthropic 11-19 纳斯达克上市
- 10月PCE发布日独立确认: query_calendar_events(days=21,country=US,importance=high,medium,low) = 2026-11-25 13:30 UTC 发布10月PCE/核心PCE（核心PCE同比前值3.1、环比前值0.3），与稿中证伪器日期一致
- 贝森特公开敦促美联储: query_raw_items(美联储 OR Fed OR 沃什 OR Warsh, published_after=2026-11-09)[id:781081] = Bessent: Expects Significant Decline in Inflation Next Month, Urges Fed to Focus on the Future（2026-11-15）
- BTC周跌13%的非Fed驱动: query_raw_items(美联储 OR Fed OR 沃什 OR Warsh)[id:781951] = Bitcoin Plunges 13% in a Week as Market Retreats to $60,000 Level（来源列明：通胀数据、加息预期、美元走强 + Binance黑客事件 + Anthropic IPO流动性抽血）
- Binance黑客为BTC下跌驱动之一: query_raw_items(美联储 OR Fed OR 沃什 OR Warsh)[id:781472] = 四年周期报告提及 Binance hack incident 致 BTC 低见 62,000 美元
- 美联储警告AI数据中心杠杆风险: query_raw_items(美联储 OR Fed OR 沃什 OR Warsh)[id:781735] = HK Stocks Open… the Federal Reserve warned about leverage risks in AI data centers（2026-11-16）
- 黄仁勋去职与市场冲击: query_raw_items(Cook OR 罢免 OR 独立性, published_after=2026-10-17)[id:769231] = Jensen Huang Resigns Amid Scandal, Trump Downplays US-Iran Talks Prospects…三大股指齐跌（2026-11-13）
- 本周AI链二元事件焦点: query_raw_items(美联储 OR Fed OR 沃什 OR Warsh)[id:781281] = US Stock Market Focus This Week: NVIDIA Earnings, Anthropic IPO（2026-11-16）
- 近30天Lisa Cook独立性新闻检索: query_raw_items(Cook OR 罢免 OR 独立性, published_after=2026-10-17) = 未返回任何 Lisa Cook/Fed 独立性相关条目（命中均为 Tim Cook/英伟达），佐证§9「无新增施压事件」
- 近30天Powell新闻检索: query_raw_items(Powell OR 鲍威尔, published_after=2026-10-17) = 未返回 Jerome Powell 相关条目，稿中「11月无言论、数据缺失」标注与检索一致
- 关键数值交叉核对（日历/新闻 vs 稿）: query_calendar_events = CPI环比0.4(前值0.6/预期0.3)、核心CPI环比0.3、PPI同比6.5、10Y拍卖投标2.46(前值2.77)/中标5.02、初请20.0、GDP初值3.4 → 与稿一致；CPI同比actual日历亦缺失 → 稿标「数据缺失」如实
