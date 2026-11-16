# 数据来源（fed 报告 · 2026-11-16 轮）

- 联邦基金目标区间 3.75–4.00%（2026-10-28 决议维持，生效 10-29）: query_fomc(lookback_days=120,lookahead_days=365) = target_range 3.75–4.00%, source FOMC statement
- 2026-10-28 FOMC 投票 10–2，Cook 与 Hammack 反对、倾向加息: query_fomc(lookback_days=120) = vote 10–2, dissenters Lisa D. Cook, Beth M. Hammack (prefer to raise)
- 2026-09-16 FOMC 加息 25bp 至 3.75–4.00%，12–0 全票，SEP 联邦基金中值 4.1%: query_fomc(lookback_days=120) = vote 12–0, sep_fed_funds_median 4.1, SEP 文件 fomcprojtabl20260916.pdf
- 2026-07-29 FOMC 维持 3.50–3.75%，9–3（Hammack/Kashkari/Logan 倾向加息）: query_fomc(lookback_days=120) = vote 9–3
- 下次 FOMC：2026-12-08/09（SEP 会议，含点阵图+发布会）: query_fomc(lookahead_days=365) = next_meeting 2026-12-08, sep_meeting true
- 10 月 FOMC 纪要发布时间 2026-11-18: query_calendar_events(country=US,days=120,lookback_days=30) = 美联储公布货币政策会议纪要 2026-11-18T19:00
- 10 月 CPI 环比 +0.4%（前值 0.6、预期 0.3）、核心 CPI 环比 +0.3%（前值 0.3、预期 0.2）: query_calendar_events(country=US,days=120) = CPI All items Chg P/P actual 0.4, core Chg P/P actual 0.3 (2026-11-10)
- 10 月 CPI 同比/核心同比实际值: query_calendar_events(country=US,days=120) = 工具未返回 actual（前值 3.7 / 2.6）
- 10 月 PPI 同比 +6.5%（前值 6.3、预期 6.6）: query_calendar_events(country=US,days=120) = actual 6.5 (2026-11-13)
- 9 月 PCE 同比 3.6%、核心 PCE 同比 3.1%: query_raw_items(keyword='PCE OR 独立性 OR 解雇 OR Cook')[id:781467] = Schmid 引述 September PCE 3.6% YoY, core 3.1%
- 10 月非农 +16.5 万（前值 2.9 万、预期 6.5 万）、失业率 4.1%、时薪环比 +0.4%/同比 3.1%: query_calendar_events(country=US,days=120) = 2026-11-06 数据
- 11 月 3 日 JOLTS 职位空缺 752.3 万（前值 707.9 万、预期 710 万）: query_calendar_events(country=US,days=120) = actual 7.523M
- Q3 GDP 年化环比初值 +3.4%（前值 2.2、预期 3.2）: query_calendar_events(country=US,days=120) = 2026-10-29
- Q3 就业成本指数 ECI 环比 +0.8%（前值 0.9、预期 0.8）: query_calendar_events(country=US,days=120) = 2026-10-30
- 10 月 ISM 制造业 55.5 / 非制造业 54.5: query_calendar_events(country=US,days=120) = 2026-11-02 / 2026-11-04
- 11 月 12 日当周初请 20.0 万（前值 18.9 万、预期 19.4 万）: query_calendar_events(country=US,days=120) = actual 20.0万
- 密歇根 1 年通胀预期初值 4.3%（前值 4.7%）、10 月终值 1Y 4.7%/5Y 3.5%: query_calendar_events(country=US,days=120) = 2026-11-06 preliminary / 2026-10-23 final
- 10 月零售销售环比将于 2026-11-17 公布（前值 0.8、预期 0.2）: query_calendar_events(country=US,days=120) = upcoming
- CME FedWatch：12 月加息 25bp 概率 95%: query_raw_items(keyword='Fed OR 美联储 OR FOMC')[id:781351] = TMT Post, 2026-11-16
- 美债官员密集讲话锁定 12 月加息预期、开启 2023 年以来首次连续加息可能: query_raw_items(keyword='CPI')[id:780937] = 2026-11-15, Williams/Goolsbee/Logan 表态
- 10Y 收益率 5.1352%（11-13 纽约尾盘，周涨 27.78bp）、2Y 4.8419%（周涨 33.04bp）: query_raw_items(keyword='收益率 OR yield OR 美债')[id:780943] = 2026-11-15
- 沃勒放风 12 月可能加息 50bp、高盛将明年 3 月加息纳入基准: query_raw_items(keyword='收益率 OR yield OR 美债')[id:781618] = 中金财富期货 2026-11-16
- 摩根士丹利：美联储 3 月前加息至 4.375% 中值并全年维持，10Y 2027Q4 升至 5.00%: query_raw_items(keyword='收益率 OR yield OR 美债')[id:781514] / [id:782736] = 2026-11-16
- 民主党中期选举大胜、10 月 CPI 超预期、数据中心监管收紧压制市场情绪: query_raw_items(keyword='CPI')[id:781379] = 2026-11-16
- 沃什 11-17 北京时间 01:00 旧金山联储生产率与就业工作组听证会开幕词: query_raw_items(keyword='收益率 OR yield OR 美债')[id:782729] = 金十 2026-11-16
- 11-25 PCE 报告为关键数据日: query_raw_items(keyword='PCE OR 独立性 OR 解雇 OR Cook')[id:779305] = 2026-11-14
- CPI/PPI 为 PCE 定调，牛津经济研究院预计 10 月 PCE 年率上行: query_raw_items(keyword='PCE OR 独立性 OR 解雇 OR Cook')[id:775518] = 金十 2026-11-13
- 黄金跌至 3830 美元/盎司附近（-1.3%，2025 年 10 月以来最低）、周跌 4.6%: query_raw_items(keyword='CPI 同比 OR 通胀 OR inflation')[id:782762] / [id:782191] = 2026-11-16
- 波士顿联储 Collins 支持渐进加息: query_raw_items(keyword='Fed OR 美联储 OR FOMC')[id:781586] = longbridge 2026-11-16
- 堪萨斯城联储 Schmid：通胀仍过热、9 月 PCE 3.6%/核心 3.1%、Fed 仍有工作要做: query_raw_items(keyword='Fed OR 美联储 OR FOMC')[id:781467]/[id:781156] = longbridge 2026-11-16
- 2026-11-10 季度再融资规模 1250 亿美元（11-09 至 11-11 拍卖）: query_calendar_events(country=US,days=120) = 2026-11-08 条目
- 11-10 10Y 拍卖：得标收益率 5.02%（前次 5.30%）、投标倍数 2.46（前次 2.77）、中标总额 420 亿美元: query_calendar_events(country=US,days=120) = Auction Results 10 Year 2026-11-10
- 美联储资产负债表规模 6.81 万亿美元（10-22 当周）: query_calendar_events(country=US,days=120) = 2026-10-22
- QT 缩表具体速度/剩余路径: query_fomc / query_calendar_events = 数据缺失（工具未返回）
- FOMC 成员名单与 2027-2029 票委轮换表: ReadThemeDocsTool(themes/fed/FOMC_MEMBERS.md) = 官方 federalreserve.gov 抓取，2026-11-16
- 成员近期言论（Warsh/Williams/Barr/Bowman/Hammack/Jefferson/Logan/Paulson/Waller/Daly/Goolsbee/Barkin 等 11-06 至 11-14）: 系统预采集注入（FOMC 成员近期言论节，来源 longbridge / telegram:Financial_Express）
- 报告结构模板: ReadThemeDocsTool(themes/fed/template.md) = v2 2026-08-09 修订

12月8-9日FOMC基准路径：加息25bp至4.00-4.25%（概率80%），若落地为2023年以来首次连续加息；尾部为50bp（12%，Waller路线）或跳过（8%）。CME FedWatch定价25bp概率95%，我们比市场低15pp——市场把数据依赖的跳过尾部几乎清零了。触发变量：11-17零售、11-18纪要、11-25 PCE、会前非农。核心PCE 9月3.1%、10月CPI连续第三个月超预期，通胀是唯一主导权重；就业（非农16.5万、失业率4.1%）暂不构成阻碍。

themes/fed/_history/2026-11-16_1415__manual__12_fomc_fomc_readthemedocstool_themes_fed_template_md_v2_9_q/reference.mdfalsenick_timiraos0.8成员言论几乎单边偏鹰（Waller 50bp、Williams/Bowman/Hammack/Paulson/Daly/Goolsbee均要求进一步加息），10月CPI/PPI超预期、9月核心PCE 3.1%远高于2%；但去前瞻指引regime下单月数据可往返，且11-25 PCE在会前落地，留8%跳过尾部。policy_regulation