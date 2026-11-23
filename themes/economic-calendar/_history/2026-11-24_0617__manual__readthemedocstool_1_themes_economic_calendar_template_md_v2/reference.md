# 数据来源溯源 — economic-calendar 圆桌 · 目标周 2026-11-30~12-06

> 记录时间 2026-11-23 22:17 UTC · Lead ackman · 本轮为周度预读（forecast）
> 格式：`- {数据点}: {来源工具}({关键参数}) = {值}`

## A. 目标周关键事件（前值/共识）
- 美国 11 月非农就业人口变动: query_calendar_events(days=14, importance=high,medium, lookback_days=7) = 前值 16.5 万，共识 10.1 万（2026-12-04 13:30 UTC）
- 美国 11 月失业率: query_calendar_events(days=14) = 前值 4.1%，共识 4.1%（2026-12-04）
- 美国 11 月 ISM 制造业指数: query_calendar_events(days=14) = 前值 55.5（2026-12-01 15:00 UTC）
- 美国 11 月 ISM 非制造业指数: query_calendar_events(days=14) = 前值 54.5（2026-12-03 15:00 UTC）
- 美国 11 月 ADP 就业人数变动: query_calendar_events(days=14) = 前值 8.6 万（2026-12-02 13:15 UTC）
- 美国 11 月 28 日当周初请失业救济: query_calendar_events(days=14) = 前值字段空 ⚠️（2026-12-03）
- 中国 11 月官方制造业 PMI: query_calendar_events(days=14) = 前值 49.3（2026-11-30 01:30 UTC）
- 中国 11 月 RatingDog 制造业 PMI: query_calendar_events(days=14) = 前值 52.0（2026-12-01 01:45 UTC）
- 欧元区 11 月制造业 PMI 终值: query_calendar_events(days=14) = 前值字段空 ⚠️（2026-12-01 09:00 UTC）
- 韩国 11 月 CPI 同比: query_calendar_events(days=14) = 前值 2.8（2026-12-01 23:00 UTC）
- 鸿海 11 月营收: query_calendar_events(days=14) = 无前值/共识（2026-12-04）

## B. 行情快照
- 10Y UST: query_indicators(category=us) = 5.15%（openbb, 2026-11-13, 10天前）
- 2Y UST: query_indicators(category=us) = 4.88%（openbb, 2026-11-13, 10天前）
- 2s10s 利差: query_indicators(category=us) = 0.29（akshare, 2026-11-16）
- DXY: query_indicators(category=us) = 122.6503（openbb, 2026-11-13, 10天前）
- VIX: query_indicators(category=us) = 19.3（openbb, 2026-11-13）
- 高收益债利差: query_indicators(category=us) = 3.23（openbb, 2026-11-13）
- 联邦基金利率: query_indicators(category=us) = 3.88（openbb, 2026-10-01）
- 中国 10Y 国债: query_indicators(country=china) = 1.5861%（akshare, 2026-11-23, 0天前）
- 中国 2Y 国债: query_indicators(country=china) = 1.2351%（akshare, 2026-11-23, 0天前）
- 中国 10Y-2Y 利差: query_indicators(country=china) = 0.351（akshare, 2026-11-23）
- S&P 500 ETF (SPY): market_quote(SPY.US) = 722.29（+4.71%, 2026-11-23）
- Gold ETF (GLD): market_quote(GLD.US) = 333.02（+3.14%, 2026-11-23）
- 原油 ETF (USO): market_quote(USO.US) = 133.36（-4.49%, 2026-11-23）
- USDCNH: query_indicators(country=china) = None ⚠️ 缺失

## C. 政策与新闻（含 id 溯源）
- 美联储 12 月加息 25bp 概率 95.9%（50bp 4.1%）: query_raw_items(keyword="非农 OR 美联储 OR 加息 OR 就业")[id:813379] = CME FedWatch 2026-11-23 22:05 定价
- 美联储 12 月加息 25bp 概率 96.1%: query_raw_items(keyword="非农 OR 美联储 OR 加息 OR 就业")[id:813364] = CME FedWatch 2026-11-23 22:00 定价
- 威廉姆斯：需逐步行动将通胀拉回 2%，"仍有工作要做"，价格压力持续: query_raw_items(keyword="非农 OR 美联储 OR 加息 OR 就业")[id:813291] = 纽约联储行长 2026-11-23 讲话
- 标普500 收 7237.17（+4.73%），等权重指数 -2.04%: query_raw_items(keyword="非农 OR ISM OR PMI")[id:813365] = 2026-11-23 收盘，宽度背离
- 英伟达 +31% 带动纳指 +6.51%，黄仁勋复任 CEO: query_raw_items(keyword="非农 OR ISM OR PMI")[id:813374] = 2026-11-23，一年来最佳单日
- FOMC 10 月决议: query_fomc(lookback_days=60, lookahead_days=60) = 目标区间 3.75-4.00%，10-2 投票，Cook/Hammack 主张加息；下次 12-08（含 SEP 点阵图）

## D. FactPack 锚点核对
- FedWatch 9月 维持59.9%/加息40.1%/降息0.0%（CME FedWatch 2026-08-26）为历史快照；当前 12 月加息定价已演进至 95.9%（2026-11-23，id:813379），两者为不同时点/不同会议定价，无溯源矛盾，以最新数据为准，Lead 确认放行。

## E. 上周承接（供 forecast §7「日历外的已知未知」使用）
- [承接] 美联储 12 月加息路径（上周 forecast 观察项）—— 本周已明确：加息 25bp 概率 95.9%（id:813379），转为"加息幅度 25 vs 50bp + 非农验证"的新观察
- [承接] 2026-11-10 美国 10 年期国债拍卖收益率双口径矛盾（5.02% vs 2.46%）—— 未解，继续挂账
- [承接] 美股感恩节休市日期偏差（源标 11-24/11-25，实际 11-26）—— 已过，归档
- [承接] 中美人工智能对话（约定 11 月底前）—— 目标周内可能落地，继续观察
- [承接] 俄美乌阿布扎比会谈后续（船舶通行量/战争险保费）—— 继续观察原油风险溢价
- [新增] 市场宽度背离（11-23 权重股驱动反弹 vs 等权重下跌）—— 触发条件：等权重指数是否补涨；影响方向：反弹质量与 AI 板块脆弱性

## F. 成绩单校准说明
- 上周 forecast（11-23~11-29）关键预测（PCE/GDP/PMI/工企利润）多在 11-25 及之后发布，截至 2026-11-23 22:17 UTC 尚未到期，无法验证；本周置信度沿用上周中档（50-60%），不因未验证而上调。


## G. 第 1/3 位接力（soros）新增溯源

- Polymarket 12-08 加息 25bp 概率 93.5%（normalized 93.08%）、加息 50bp 3.35%、维持 3.2%、expected_bps 24.8；异议 0 人 64.5%、1 人 25.8%；加息 25bp 1d +3.0pp / 7d +6.0pp: query_fomc_market(meeting="", days=30, source=polymarket) = 2026-11-23 定价
- 威廉姆斯：企业有招聘意愿但态度谨慎: query_raw_items(keyword="非农 OR 美联储 OR 加息 OR 就业 OR ISM")[id:813318] = 2026-11-23 讲话
- 威廉姆斯：关税对通胀影响基本消退，伊朗战争导致能源价格高位前景高度不确定: query_raw_items(keyword="非农 OR 美联储 OR 加息 OR 就业 OR ISM")[id:813264] = 2026-11-23 讲话
- 威廉姆斯：AI 基础设施建设热潮已反映在芯片和半导体价格上: query_raw_items(keyword="非农 OR 美联储 OR 加息 OR 就业 OR ISM")[id:813258] = 2026-11-23 讲话
- 威廉姆斯：预计美国经济 2026 和 2027 年均增长 2.75%: query_raw_items(keyword="非农 OR 美联储 OR 加息 OR 就业 OR ISM")[id:813215] = 2026-11-23 讲话
- 美联储理事鲍曼遭内部调查，涉嫌违反缄默期规定（6 月美银私人晚宴）: query_raw_items(keyword="非农 OR 美联储 OR 加息 OR 就业 OR ISM")[id:813281] = 2026-11-23 报道
- 中国 10 月社零同比 0.4%、FAI 同比 -17.84%（口径存疑，与上周 -7.2% 不符）、M2 同比 7.1%、新增贷款同比 -3696 亿元: query_indicators(country=china) = akshare 2026年10月
- 中国 10Y / 2Y 国债 1.5861% / 1.2351%、10Y-2Y 利差 0.351: query_indicators(country=china) = akshare 2026-11-23
- 美国 initial_claims 20.0 万: query_indicators(country=us) = openbb 2026-11-07
- 中国 11 月官方制造业 PMI 前值 49.3、RatingDog 前值 52.0、美国 ISM 制造业前值 55.5 / 非制造业 54.5、ADP 前值 8.6 万、非农前值 16.5 万/共识 10.1 万、失业率前值/共识 4.1%: query_calendar_events(days=14, lookback_days=3, importance=high,medium) = 2026-11-30~12-04



## H. 第 2/3 位接力（dalio）新增溯源

- Fed 资产负债表 6.76 万亿美元（6758867 百万美元，2026-11-11，12天前）: query_indicators(country=us) = openbb 6758867.0
- 9 月 SEP 联邦基金利率中值 4.1%（2026-09-16 SEP 会议）: query_fomc(lookback_days=120, lookahead_days=60) = sep_fed_funds_median 4.1
- 7 月 FOMC 决议 9-3 投票、Hammack/Kashkari/Logan 主张加息、目标区间 3.50-3.75%: query_fomc(lookback_days=120, lookahead_days=60) = 2026-07-29
- 中国 2026 年地方债累计发行 9.98 万亿元、新增专项债 4.13 万亿元、发行进度 93%、2027 年限额提前下达: query_raw_items(keyword="美联储 OR 加息 OR 债务 OR 赤字 OR 非农")[id:813395] = 上证报 2026-11-23
- 威廉姆斯：经济强劲且展现出韧性: query_raw_items(keyword="美联储 OR 加息 OR 债务 OR 赤字 OR 非农")[id:813216] = 2026-11-23 讲话
- 威廉姆斯：强劲增长的基础面临一些挑战: query_raw_items(keyword="美联储 OR 加息 OR 债务 OR 赤字 OR 非农")[id:813290] = 2026-11-23 讲话
- 威廉姆斯：没有证据显示存在工资压力、住房服务通胀放缓、通胀预期与 2% 目标一致: query_raw_items(keyword="美联储 OR 加息 OR 债务 OR 赤字 OR 非农")[id:813258] = 2026-11-23 讲话
- 威廉姆斯：关税对通胀影响基本消退、伊朗战争导致能源价格高位前景高度不确定: query_raw_items(keyword="美联储 OR 加息 OR 债务 OR 赤字 OR 非农")[id:813264] = 2026-11-23 讲话
- 威廉姆斯：2027 年将是通胀率较低的一年: query_raw_items(keyword="美联储 OR 加息 OR 债务 OR 赤字 OR 非农")[id:813315] = 2026-11-23 讲话
- 美联储理事鲍曼遭内部调查（涉嫌违反缄默期规定，6 月美银私人晚宴）: query_raw_items(keyword="美联储 OR 加息 OR 债务 OR 赤字 OR 非农")[id:813281] = 2026-11-23 报道



## I. 第 3/3 位接力（ackman）新增溯源

- 长久期美债 ETF (TLT): market_quote(TLT.US) = 81.69（+0.29%, 2026-11-23）
- 美元 ETF (UUP): market_quote(UUP.US) = 29.78（+0.54%, 2026-11-23）
- Polymarket 2027-01-26 会议：加息 25bp 54.5%（normalized 54.36%）、维持 43%（42.89%）、expected_bps 13.5；2027-03-16 会议：加息 25bp 49.5%（49.11%）、维持 44%（43.65%）、expected_bps 10.7: query_fomc_market(meeting="", days=30, source=polymarket) = 2026-11-23 定价（零售事件合约，仅作"最后一次加息"叙事对照）
- 威廉姆斯：预计美国经济 2026 和 2027 年均增长 2.75%: query_raw_items(keyword="美联储 OR 加息 OR 非农 OR 沃什 OR Warsh OR 鲍威尔")[id:813215] = 2026-11-23 讲话
