# fed 主题数据来源（kahneman relay 2/2 新增/核验）

## 宏观指标与日历（query_calendar_events / query_indicators / query_fomc）

- 9月FOMC会议(SEP): query_fomc(lookahead_days=30) = 2026-09-15至09-16，sep_meeting=True（含点阵图）
- 美联储资产负债表 6.7309万亿美元: query_indicators(fed_balance_sheet, country=us) = 6730912.0（2026-08-26）
- 8月密歇根消费者信心终值 51.7: query_calendar_events(2026-08-28) = 51.7（前值51.0，预期51.0）
- 8月堪萨斯联储制造业综合指数 10.0: query_calendar_events(2026-08-27) = 10.0（前值9.0）
- 7月批发库存环比初值 +1.3%: query_calendar_events(2026-08-27) = 1.3%（前值0.2%）
- 7月商品贸易帐 -1188亿美元: query_calendar_events(2026-08-27) = -1188.0（前值-1015.0）
- 8月28日当周石油钻井数 447: query_calendar_events(2026-08-28) = 447（前值452）
- 2年期国债拍卖 high yield 4.204%: query_calendar_events(2026-08-25) = 4.204%（前值4.315）
- 5年期国债拍卖 high yield 4.393%: query_calendar_events(2026-08-26) = 4.393%（前值4.408）
- 6月S&P/CS20房价同比 2.1%: query_calendar_events(2026-08-25) = 2.1%（前值1.6）

## 新闻流（query_raw_items，保留 [id:N] 便于打分）

- 沃什一句话搅动全球、9月加息概率35%→60%: query_raw_items(keyword='Warsh OR 沃什 OR 加息')[id:192521] = "沃什一句话搅动全球金融市场...9月加息概率一夜之间从35%飙到60%"
- 布林德：拒绝前瞻指引即另一种前瞻指引、暗示加息、35%→60%: query_raw_items(keyword='Warsh OR 沃什')[id:192438] = "前美联储副主席布林德认为，该表态属另一种前瞻指引，或暗示倾向加息...9月加息概率从35%升至约60%"
- 杰克逊霍尔核心要点、全球央行分化: query_raw_items(keyword='Jackson Hole')[id:192154] = "欧元区政策制定者暗示9月有加息必要；英国央行贝利暂无加息紧迫性"
- 韩国央行行长称韩元韧性、美加息不必然跟随: query_raw_items(source=telegram:Financial_Express)[id:192467] = "美国加息并不代表我们就必须紧随其后"
- 彭博Anna Wong：下周非农或疲软、连续负非农无加息先例: query_raw_items(keyword='非农 OR 加息')[id:191814] = "一定概率录得负增长...连续两次负非农数据，现代美联储历史上尚无在这种情况下加息的先例"
- StoneX：非农与CPI为最后裁判、30%→50%: query_raw_items(keyword='沃什 OR 加息')[id:191226] = "沃什拒绝预先承诺九月加息...非农与CPI成最后裁判"
- 12月加息概率近90%: query_raw_items(keyword='加息')[id:191377] = "The probability of the Federal Reserve raising interest rates in December rises to nearly 90%"
- 沃什"迟到的鹰派、信誉修复": query_raw_items(keyword='沃什')[id:191189] = "中金：迟到的鹰派、信誉的修复"
- 黄金讲话后跌超120美元至4480: query_raw_items(keyword='gold OR 黄金')[id:185745] = "现货黄金在沃什讲话后日内跌超120美元至4480"
- 截至3月非农年度基准修正下修7.9万: query_raw_items(keyword='非农')[id:183714] = "截至3月非农年度基准修正初估下修7.9万（预期+18.3万）"
- 2Y-30Y利差收窄>9bp: query_raw_items(keyword='Walsh OR Warsh OR Treasury')[id:189435] = "spread between 2-year and 30-year Treasury yields to narrow by more than 9 basis points"
- 加密24h爆仓4.81亿、加息概率35.4%→55.7%: query_raw_items(keyword='加息 OR Warsh')[id:190956] = "CME FedWatch数据显示，9月加息概率由前一日的35.4%升至55.7%...全市场爆仓约4.81亿美元"


## 审查人 soros 独立核验来源（2026-08-30 02:11 UTC）

- 美联储主席为 Kevin Warsh（非 Powell、非 Waller）: query_raw_items(keyword='Warsh OR 沃什')[id:190064][id:189938][id:189886][id:189810] = "Fed Chair Kevin Warsh..."（longbridge 多源误标为 Waller，见 id:191916/191451/191397/191377/190122）
- 9月FOMC 9/15–16 含SEP点阵图: query_fomc(lookahead_days=60) = 2026-09-15/09-16, sep_meeting=True
- 目标区间 3.50–3.75%: query_fomc = target_range '3.50–3.75%' (as of 2026-07-28, July会议)
- 资产负债表 6.7309 万亿: query_indicators(fed_balance_sheet, country=us) = 6730912.0 (2026-08-26)
- 7月CPI同比 3.4%: query_calendar_events(US, 2026-08-12) = 3.4 (forecast 3.4, prev 3.5)
- 核心PCE同比: query_calendar_events(US, 2026-08-26) = 3.3 (prev 3.3, fcst 3.3)  ← 注：草稿写 3.34%，库值 3.3%
- 谘商会信心 89.4: query_calendar_events(US, 2026-08-25) = 89.4 (prev 90.8, fcst 90.2)
- 7月ISM制造 55.6: query_calendar_events(US, 2026-08-03) = 55.6（即8月ISM前值55.6，与草稿一致）
- 初请 20.3万: query_calendar_events(US, 2026-08-27) = 20.3 (prev 20.6, fcst 20.8)
- 耐用品订单 +1.1%: query_calendar_events(US, 2026-08-26) = 1.1 (prev 0.5)
- 新屋销售 0.607M: query_calendar_events(US, 2026-08-25) = 0.607M (prev 0.628M，隐含MoM -3.3%)  ← 注：草稿写"环比-10.5%"，与库值不符
- 6月S&P/CS20同比 2.1%: query_calendar_events(US, 2026-08-25) = 2.1 (prev 1.6) ✓
- 7月非农实际值: query_calendar_events(US, 2026-08-07) = None（库未填充 actual）  ← 草稿"-2.3万"无法独立核验，且 reference.md 未列出来源
- 8月芝加哥PMI: query_calendar_events(US, lookback30d) 未返回（仅见7月57.6 @2026-07-31）  ← 草稿"47.1"无法独立核验
- 加息概率多源口径: query_raw_items[key:192521]=35%→60%; [key:190956]=35.4%→55.7%; [key:192438]=35%→60%（pre-JH约35%，post-JH 55-60%；与FactPack 8/26锚点40.1%存在~5pp缺口未 reconciles）
- 续请失业金: query_calendar_events(US) 最新可见为 180.1万（8/1当周，2026-08-06）  ← 草稿"177.8万"未在核验窗口内确认
- 7月失业率: query_calendar_events(US, 2026-08-07) = actual None（prev 4.2）  ← 草稿"失业率前值4.1"未确认
