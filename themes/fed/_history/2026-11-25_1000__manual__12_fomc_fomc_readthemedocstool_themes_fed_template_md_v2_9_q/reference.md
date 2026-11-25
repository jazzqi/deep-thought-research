# 本轮（2026-11-25 周度复盘）新增数据来源

> 格式：`- {数据点}: {来源工具}({关键参数}) = {值}`；query_raw_items 条目保留 [id:N]。

## 事件日历（query_calendar_events, country=US, days=180, lookback_days=14, limit=200）

- 10月零售销售环比 +0.2%（前值0.8%、预测0.1~0.2%）、控制组环比 +0.6%（前值0.1%、预测0.4%）、核心零售 +0.6%、同比 +6.82%: query_calendar_events(country=US, days=180, lookback_days=14, limit=200) = 2026-11-17 发布
- 初请 11-14 当周 20.3万（前值20.0、预测19.8）: query_calendar_events = 2026-11-19
- 续请 10-31 当周 169.7万（前值171.8、预测171.0）: query_calendar_events = 2026-11-12
- 密歇根消费者信心 11月终值 51.5（前值51.0、预测51.5）: query_calendar_events = 2026-11-20
- 费城联储制造业 6.3（前值20.9、预测20.0）: query_calendar_events = 2026-11-19
- 10月PPI同比 +6.5%（前值6.3、预测6.6）、核心PPI同比 +5.0%、PPI环比 +0.3%、核心PPI环比 +0.3%: query_calendar_events = 2026-11-13
- 10月工业产出环比 -0.4%（前值0.7、预测0.1）、制造业产出 +0.3%、产能利用率 76.4%: query_calendar_events = 2026-11-17
- 10月新屋开工 130.9万（前值122.1、预测124.5）、营建许可 129.5万（前值139.8、预测137.7）: query_calendar_events = 2026-11-18
- Q3 GDP 修正值待公布（前值3.4%、预测3.5%）、11-25 初请待公布: query_calendar_events = 2026-11-25
- 美联储资产负债表 6.81万亿美元（前值6.8）: query_calendar_events = 2026-11-12（截至11-11）
- 30年房贷利率 7.21%（前值7.30%）11-11、7.35%（前值7.21%）11-18: query_calendar_events = MBA
- 美联储公布货币政策会议纪要（10月会议）: query_calendar_events = 2026-11-18 19:00 UTC
- 美联储公布经济状况褐皮书: query_calendar_events = 2026-11-25 19:00 UTC
- 未来FOMC会议（12/8 SEP、2027/1/26、3/16、4/27、6/8、7/27、9/14、10/26、11/16）: query_calendar_events = country=US

## FOMC 结构化（query_fomc）

- 10-28 决议维持 3.75–4.00%（投票10–2，Cook/Hammack 反对 prefer to raise，生效10-29）: query_fomc(lookback_days=120, lookahead_days=365, limit=20) = federalreserve.gov
- 09-16 决议加息25bp至3.75–4.00%（12–0，SEP中值4.1%，生效09-17）: query_fomc = 官方数据
- 下次 FOMC 2026-12-08/09（sep_meeting=True，发布会/声明链接未填充）: query_fomc = next_meeting
- 2027-01-26/27、03-16/17（sep_meeting=False）、04-27、06-08、07-27、09-14、10-26、11-16: query_fomc(lookahead_days=365) = meetings

## 成员立场（query_fomc_members, include_presidents=true）

- 委员会综合近期 +0.233（投票+0.055/言论+0.545，12票委）、长期 +0.179；data_quality: 19成员，ok=7/thin=12: query_fomc_members = 2026-11-24
- 【新增转边】库克 中性→鹰（Δ+0.48，medium，证据 2026-11-20 telegram:Financial_Express「美国股市或成美联储加息变数」）: query_fomc_members.stance_changes_30d
- 【基线转边】沃勒 鸽→鹰（Δ+1.36，high）、鲍曼 中性→鹰（Δ+0.45，medium）、杰斐逊 中性→鹰（Δ+0.28，medium）: query_fomc_members.stance_changes_30d
- 言行不一7人（哈马克-0.50、洛根-0.70、卡什卡利-0.59、保尔森-0.63、沃什-0.46、巴尔-0.63、威廉姆斯-0.59）: query_fomc_members.divergences
- 威廉姆斯 11-24「未来可能需要进一步加息，节奏取决于数据」鹰（+0.56/1.00）: query_fomc_members.members[Williams].latest_statement[raw_item_id:817939] = longbridge
- 沃什 11-24「AI繁荣让Fed更难，面临抗通胀与保增长双重考验」鹰（+0.54/0.52）: query_fomc_members.members[Warsh].latest_statement[raw_item_id:816744] = longbridge
- 保尔森 11-21「不排除连续加息、强调有节制步伐」鹰（+0.68/1.00）: query_fomc_members.members[Paulson].latest_statement[raw_item_id:806753] = longbridge
- 穆萨莱姆 11-18「四次连续加息？迄今最鹰信号」鹰（+0.90/0.64）: query_fomc_members.members[Musalem].latest_statement[raw_item_id:791736] = longbridge
- 古尔斯比 11-20「通胀数月高企，不排除更大规模加息」鹰（+0.60/1.00）: query_fomc_members.members[Goolsbee].latest_statement[raw_item_id:802925] = longbridge
- 成员名单/票委轮换/主席Warsh: themes/fed/FOMC_MEMBERS.md（生成时间 2026-11-25 02:00 UTC，federalreserve.gov）

## 市场定价（query_fomc_market, source=polymarket, asof=2026-11-24）

- 12月：加息25bp 93.7%（liquidity 50.3万）、加息50bp 2.15%、维持3.75%、降息0.25%；expected_bps 24.4；异议0人69.2%: query_fomc_market(source=polymarket, meeting=2026-12-08) = 事件合约/零售定价，非CME FedWatch/OIS
- 1月：加息25bp 52.9%（7d -7.5pp）、维持44.4%（7d +8pp）、加息50bp 0.9%；expected_bps 13.0: query_fomc_market(meeting=2027-01-26)
- 3月：加息25bp 50.1%（7d -9pp）、维持43.2%（7d +7pp）: query_fomc_market(meeting=2027-03-16)

## 宏观指标（query_indicators, country=us）

- cpi_yoy_us_pct 3.7（2026-09-01，⚠️85天前过时）、core_cpi 339.9（2026-10-01）、cpi_yoy_us 337.476（2026-10-01）、us_ppi 293.921（2026-10-01）、fed_balance_sheet 6,758,867百万美元（2026-11-11）、gdp 33010.036（2026-07-01，⚠️147天前过时）、consumer_confidence_us 48.1（2026-09-01，⚠️过时）: query_indicators(category=macro, country=us, time_range=7d)
- ⚠️ query_indicators(country=us) 未返回 PCE 同比/核心 PCE 指标——系统缺失（已登记 confirmed_missing_indicators）

## 行情（binance_get_price）

- BTCUSDT 59,160.4 美元: binance_get_price(symbol=BTCUSDT) = 2026-11-25 约 02:42 UTC

## 新闻（query_raw_items，引用即打分）

- 10月PCE同比预期3.8%、核心PCE加速，强化12月加息预期: query_raw_items(keyword='核心PCE OR PCE物价')[id:807996] = 2026-11-22
- 10月FOMC纪要：几乎所有官员认为未来几个月需进一步加息，2人认为12月加息可超25bp: query_raw_items(keyword='会议纪要 OR 贴现利率')[id:797053] = 2026-11-19
- 10月贴现利率会议纪要：12家地方联储8家建议上调贴现率4%→4.25%: query_raw_items(keyword='贴现利率')[id:817698] = 2026-11-24
- 威廉姆斯：持续高通胀指向更紧缩政策，节奏取决于数据；黄金跌至3590: query_raw_items(keyword='核心PCE OR PCE物价')[id:817670] = 2026-11-24
- AI平仓暴跌致纳指跌约18%接近熊市、VIX破40、交易员下调12月加息预期涌入美债: query_raw_items(keyword='核心PCE OR PCE物价')[id:808807]/[id:808018] = 2026-11-22
- CTA未来5天预计抛售680亿美元全球股票，机械反馈循环未发出放缓信号: query_raw_items(keyword='PCE OR 纪要 OR 英伟达 OR 空头回补')[id:818225] = 2026-11-25
- 美股收盘纳指跌1.48%、英伟达跌5.8%、AMD跌8.8%、戴尔跌13%: query_raw_items(keyword='PCE OR 纪要 OR 英伟达')[id:817767] = 2026-11-24
- 费城半导体指数日内跌9.02%: query_raw_items(keyword='PCE OR 纪要 OR 英伟达')[id:817222] = 2026-11-24
- 黄金单日跌超2%、现货金3590美元: query_raw_items(keyword='核心PCE OR PCE物价')[id:817176] = 2026-11-24
- 特朗普称必要时愿赦免黄仁勋、不排除政府入股英伟达（产业政策干预，非Fed施压）: query_raw_items(keyword='PCE OR 纪要 OR 英伟达')[id:817968]/[id:817993] = 2026-11-24
- 10月会议纪要：19名官员几乎全部提及AI投资若令投资者失望的后果、复杂不透明融资结构风险: query_raw_items(keyword='会议纪要')[id:814416] = nytimes_chinese 2026-11-24
- 市场押注主要央行继续加息、高利率至少持续到2031年；10月纪要显示AI基建扩张是不容忽视的通胀风险: query_raw_items(keyword='会议纪要')[id:799878] = 2026-11-19
- 黄金自13个月低点反弹或因空头获利了结；FedWatch 12月加息25bp 90%/50bp 10%: query_raw_items(keyword='会议纪要')[id:797823] = 2026-11-19
- 金价暴跌3.2%至2025年9月以来最低、沃勒敦促12月加息50bp: query_raw_items(keyword='会议纪要')[id:796545] = 2026-11-19
- 机构：PCE若证实价格上行强劲将强化FOMC下月及2027收紧理由；GDP上修亦强化加息预期: query_raw_items(keyword='核心PCE OR PCE物价')[id:814776] = 2026-11-24
- 周三财经提醒：21:30 Q3 GDP修正值、10月PCE、初请；次日03:00褐皮书: query_raw_items(keyword='核心PCE OR PCE物价')[id:817918] = 2026-11-24
- 10月PCE物价指数年率今日公布: query_raw_items(keyword='核心PCE OR PCE物价')[id:818057] = 2026-11-24


## 第 1 棒（nick_timiraos）接力补充来源

> 查重后仅追加本轮新引用、reference.md 尚未记录的数据点。

### 市场定价（CME FedWatch，与 Polymarket 交叉核验）

- CME FedWatch 12月加息25bp 97.4%、加息50bp 2.6%；到1月加息25bp 30.3%、累计加息50bp 67.9%、累计加息75bp 1.8%: query_raw_items(keyword='PCE OR 美联储 OR 加息 OR 美债收益率')[id:817878] = 2026-11-24（事件合约口径，非OIS）
- 1年期国债竞拍投标倍数 3.04（前值3.15）: query_raw_items(keyword='PCE OR 美联储 OR 加息 OR 美债收益率')[id:817339] = 2026-11-24

### 流动性 / 财政-货币交互

- 隔夜逆回购RRP使用规模 3.01亿美元（2家对手方，前日3.5亿）: query_raw_items(keyword='PCE OR 美联储 OR 加息 OR 美债收益率')[id:817532] = 2026-11-24
- 30年国债拍卖：投标倍数 2.36（前值2.54）、高收益率 5.441%（前值5.618%）、间接投标比例(High allocation) 21.29%（前值26.77%）: query_calendar_events(country=US, days=180, lookback_days=14, limit=200) = 2026-11-12
- 10月政府预算 -4040.64亿美元（前值-2843、预测-3175）: query_calendar_events = 2026-11-12
- 10月成屋销售环比 -5.5%（前值1.5、预测-3.5）、成屋签约销售同比 -17.1%（前值-12.6、预测-13.7）: query_calendar_events = 2026-11-12 / 2026-11-18
- 10月进口价格环比 +1.1%（前值1.1、预测0.7）、出口价格环比 +1.1%（前值2.2、预测0.5）: query_calendar_events = 2026-11-17
- 11月纽约联储制造业指数 7.8（前值25.5、预测18.0）、未来6个月预期 28.9（前值21.0）: query_calendar_events = 2026-11-16

### 会前关键数据日历（query_calendar_events, country=US）

- 12月4日 11月非农就业预期 10.1万（前值16.5万）、失业率 4.1%（前值4.1、预测4.1）: query_calendar_events = 待公布
- 12月1日 11月ISM制造业（前值55.5）、12月3日 ISM非制造业（前值54.5）、12月2日 ADP就业（前值8.6万）: query_calendar_events = 待公布
- 11月25日 Q3 GDP修正值（前值3.4、预测3.5）、11-21当周初请（前值20.3、预测20.0）: query_calendar_events = 待公布

### 业界看法 / 二阶效应（query_raw_items）

- 华侨银行：现在做空美元仍为时过早，通胀黏性+增长韧性+Fed更鹰，美元到2027上半年末受支撑，2027下半年逐步走低: query_raw_items(keyword='PCE OR 美联储 OR 加息 OR 美债收益率')[id:818280] = 2026-11-25
- Pimco首席投资官Ivascyn：AI颠覆性风险提升债券吸引力，美债处于2022年来首次年度亏损边缘，长债收益率距数十年高点不远: query_raw_items(keyword='PCE OR 美联储 OR 加息 OR 美债收益率')[id:817351] = 2026-11-24
- 摩根大通：预计Fed自2027年一季度起维持利率不变，黄金2027Q4回升至4500美元: query_raw_items(keyword='PCE OR 美联储 OR 加息 OR 美债收益率')[id:817044] = 2026-11-24
- 中金财富期货：美股未企稳或金融条件收紧未改善，黄金难走出泥潭: query_raw_items(keyword='PCE OR 美联储 OR 加息 OR 美债收益率')[id:818170] = 2026-11-25
- 澳大利亚10月截尾均值通胀同比3.8%（预期3.6%）、整体通胀4.9%，全球央行同步收紧背景: query_raw_items(keyword='PCE OR 美联储 OR 加息 OR 美债收益率')[id:818146] = 2026-11-25

- FOMC 会议/决议/SEP/票数: query_fomc(lookback_days=120, lookahead_days=365) = 2026-09-16 加息25bp至3.75-4.00% 12-0 SEP中值4.1%; 2026-10-28 维持3.75-4.00% 10-2 Cook/Hammack反对prefer to raise; 下次2026-12-08/09 SEP会议
- FOMC 市场定价: query_fomc_market(source=polymarket, days=30) = 2026-12-08 加息25bp 93.69% expected_bps 24.4 流动性$503k; 2027-01-26 加息25bp 52.87% 7d -7.5pp 维持44.39% 7d +8pp; 2027-03-16 加息25bp 50.10% 7d -9pp; 异议0人69.22%
- FOMC 成员立场/记分卡: query_fomc_members(include_presidents=true) = 委员会综合+0.233(投票+0.0553/言论+0.5449,12票委); ok=7 thin=12; 30天转边 Waller dovish->hawkish Δ+1.36 high, Cook neutral->hawkish Δ+0.48 medium, Bowman neutral->hawkish Δ+0.45 medium, Jefferson neutral->hawkish Δ+0.28 medium; 7人言行不一
- 美国宏观日历: query_calendar_events(country=US, days=30, lookback_days=14, importance=high,medium, limit=200) = 10月PPI同比6.5%/核心5.0%; 10月零售环比0.2%/控制组0.6%; 纽约联储11月7.8; 费城联储11月6.3; NAHB 25; 初请20.3万; 成屋销售-5.5%; 10月预算赤字-4040.64亿美元; 30Y拍卖高收益率5.441%; Fed资产负债表6.81万亿(11-11); 30Y房贷7.35%; 11-25 GDP修正/初请/PCE待公布
- 美国宏观指标快照: query_indicators(country=us, category=macro, time_range=7d) = fed_balance_sheet 6758867.0 (2026-11-11); cpi_yoy_us_pct 3.7% (2026-09-01, ⚠️85天过时); core_cpi index 339.9 (2026-10-01); us_ppi 293.921 (2026-10-01)
- PCE待公布提醒: query_raw_items(keyword="PCE")[id:818057] = 11-25 美国10月核心PCE物价指数年率公布
- FedWatch定价: query_raw_items(keyword="Fed OR Powell OR Warsh")[id:817878] = CME FedWatch 12月加息25bp 97.4%, 50bp 2.6%; 到1月累计+50bp 67.9%
- Williams鹰派表态: query_raw_items(keyword="Fed OR Powell OR Warsh")[id:817939] = NY Fed Williams暗示未来可能需要进一步加息应对通胀 (2026-11-24)
- Fed贴现率会议纪要: query_raw_items(keyword="Fed OR Powell OR Warsh")[id:817712] = 10月贴现率会议纪要显示8家地区联储建议上调贴现率 (2026-11-24)
- FOMC 10月会议纪要: query_raw_items(keyword="PCE")[id:796087] = 10月FOMC纪要显示9月PCE同比3.6%、核心PCE 3.1% (2026-11-18)
- Powell讲话背景: query_raw_items(keyword="PCE")[id:806239] = Powell称PCE通胀近6年高于2%目标 (2026-11-20)


- FOMC 市场定价(Polymarket, nick_timiraos接力核验): query_fomc_market(source=polymarket, days=30) = 2026-12-08 加息25bp 93.69%/expected_bps 24.4/liquidity $503k; 2027-01-26 加息25bp 52.87% 7d -7.5pp 维持44.39% 7d +8pp/liquidity ~$171k; 2027-03-16 加息25bp 50.10% 7d -9pp 维持43.15% 7d +7pp/liquidity ~$64k; 异议0人69.22%
- 美国日历(接力核验): query_calendar_events(country=US, days=30, lookback_days=7, importance=high,medium, limit=200) = 10月核心PCE同比 前值3.1% 预测3.2% actual待公布(2026-11-25); 10月PCE同比 前值3.6% 预测3.8% actual待公布; 10月JOLTS职位空缺 前值752.3万 预测缺失 actual待公布(2026-12-01); 11月非农预测10.1万 前值16.5万; 11月失业率预测4.1% 前值4.1%; 11月ISM制造业前值55.5 预测缺失; 11月ISM非制造业前值54.5 预测缺失
- CME FedWatch: query_raw_items(keyword="FedWatch CME December FOMC")[id:817878] = 12月加息25bp 97.4%, 加息50bp 2.6%; 到1月累计+50bp 67.9%
- Williams鹰派: query_raw_items(keyword="FedWatch CME December FOMC")[id:817939] = NY Fed Williams暗示未来可能需要进一步加息应对通胀
- 贴现率纪要: query_raw_items(keyword="FedWatch CME December FOMC")[id:817712] = 10月贴现率会议纪要8家地区联储建议上调贴现率
- 贴现率纪要(telegram): query_raw_items(keyword="FedWatch CME December FOMC")[id:817698] = 8家地方联储建议上调贴现率，里士满/堪萨斯城/达拉斯由维持转加息
- PCE待公布: query_raw_items(keyword="PCE")[id:818057] = 11-25 美国10月核心PCE物价指数年率公布
- FOMC纪要PCE: query_raw_items(keyword="PCE")[id:796087] = 10月FOMC纪要显示9月PCE同比3.6%、核心PCE 3.1%
- Powell PCE表述: query_raw_items(keyword="PCE")[id:806239] = Powell称PCE通胀近6年高于2%目标

- 2026-12 FOMC 加息25bp概率93.7%/expected_bps 24.4/liquidity $503k: query_fomc_market(source=polymarket, days=14) = 2026-12-08 meeting, hike_25 0.936874 normalized, delta_7d 0.0
- 2027-01 FOMC 加息25bp概率52.9%/维持44.4%/expected_bps 13.0: query_fomc_market(source=polymarket, days=14) = 2027-01-26 meeting, hike_25 delta_7d -0.075, hold delta_7d +0.08
- 2027-03 FOMC 加息25bp概率50.1%/维持43.2%/expected_bps 11.1: query_fomc_market(source=polymarket, days=14) = 2027-03-16 meeting, hike_25 delta_7d -0.09, hold delta_7d +0.07
- BTCUSDT 最新价 59074.2: binance_get_price(symbol=BTCUSDT) = 2026-11-25
- 美联储资产负债表 6.79万亿美元（11-18当周）: query_calendar_events(country=US, lookback_days=7) = 2026-11-19发布, previous 6.81, actual 6.79
- 11月费城联储制造业指数 6.3（前值20.9，预测20.0）: query_calendar_events(country=US, lookback_days=7) = 2026-11-19
- 11月14日当周初请失业金 20.3万（前值20.0，预测19.8）: query_calendar_events(country=US, lookback_days=7) = 2026-11-19
- 11月7日当周续请失业金 176.3万（前值169.7，预测170.0）: query_calendar_events(country=US, lookback_days=7) = 2026-11-19
- 密歇根消费者信心 51.5（前值51.0，预测51.5）: query_calendar_events(country=US, lookback_days=7) = 2026-11-20
- 20年期美债拍卖高收益率 5.459%/投标倍数2.63/中标160亿: query_calendar_events(country=US, lookback_days=7) = 2026-11-18
- 10年期TIPS拍卖高收益率 2.90%（前值2.65%）: query_calendar_events(country=US, lookback_days=7) = 2026-11-19
- 10月成屋签约销售指数环比 -4.7%（前值-7.3%，预测-2.0%），同比 -17.1%: query_calendar_events(country=US, lookback_days=7) = 2026-11-18
- 10月新屋开工 130.9万户（前值122.1，预测125.0），营建许可 129.5万户（前值139.8，预测137.5）: query_calendar_events(country=US, lookback_days=7) = 2026-11-18
- 11月21日当周初请失业金预测20.0万（前值20.3万）: query_calendar_events(country=US, days=14) = 2026-11-25待公布
- 三季度实际GDP年化季环比修正值预测3.5%（前值3.4%）: query_calendar_events(country=US, days=14) = 2026-11-25待公布
- 美联储褐皮书: query_calendar_events(country=US, days=14) = 2026-11-25 19:00 UTC
- 11月非农预测10.1万/失业率4.1%: query_calendar_events(country=US, days=14) = 2026-12-04
- FOMC 12月会议 2026-12-08/09 SEP: query_fomc(lookback_days=30, lookahead_days=120) = sep_meeting True, has_decision False
- CME FedWatch 12月加息25bp概率97.4%: query_raw_items(keyword='PCE OR Powell OR Waller OR Fed hike')[id:817878] = 2026-11-24
- Williams暗示未来可能需要进一步加息: query_raw_items(keyword='PCE OR Powell OR Waller OR Fed hike')[id:817939] = 2026-11-24
- 今日公布10月核心PCE物价指数年率/初请: query_raw_items(keyword='PCE OR Powell OR Waller OR Fed hike')[id:818057] = 2026-11-24
- RRP 3.01亿美元（2家对手方，前日3.5亿）: query_raw_items(keyword='PCE OR 加息 OR Fed rate hike')[id:817532] = 2026-11-24（沿用前稿溯源）
- 8家地区联储建议上调贴现率: query_raw_items(keyword='PCE OR 加息 OR Fed rate hike')[id:817712] = 2026-11-24（沿用前稿溯源）
