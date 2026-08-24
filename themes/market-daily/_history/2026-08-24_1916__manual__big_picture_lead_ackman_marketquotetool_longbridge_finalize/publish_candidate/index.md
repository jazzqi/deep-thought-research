---
name: 市场每日追踪
slug: market-daily
status: active
lead_agent: ackman
created: 2026-08-01
updated: 2026-08-24T19:33:08+08:00
revision: 2026-08-24
sources:
  - path: 2026-08-24_1916__manual__big_picture_lead_ackman_marketquotetool_longbridge_finalize/reference.md
    agent: theme_update
    summarized: false
actions:
  - type: alert
    priority: P1
    summary: 美伊经济战升级（贝森特伊朗发布会+伊朗地震级报复+霍尔木兹服务费法案），本周最大地缘尾部风险，监控油价冲击与风险偏好
    target_flow: macro_regime
    target_flow_params: {}
  - type: follow_up
    priority: P1
    summary: 8/26 NVDA 盘后财报 + Q2 GDP 修正(前值1.5%年化) + 7月核心PCE(前值3.3% yoy) 验证 AI 估值容错率与滞胀/衰退叙事
    target_flow: thesis_propose
    target_flow_params: {}
    verification_date: 2026-08-26
---

# 市场每日追踪

## Big Picture

本周美股的核心叙事已从 8 月 17 日 index.md 定调的"地缘退潮 + 数据降温"彻底逆转。理解当前一切价格的总纲是：美股是一个由"AI 资本开支叙事 + 美联储路径 + 能源/地缘风险溢价"三脚架支撑的估值体系，而 8 月 23–24 日这三脚架中的"地缘"一脚被抽走——美伊从 MoU 延长式的缓和逆转为"经济战升级"，美加贸易战同步爆发。美财长贝森特 8/24 召开发布会宣布对伊"经济 D-Day"，切断一切经贸联系并威胁制裁其贸易伙伴（query_raw_items id:138553/137840）；伊朗反制推进霍尔木兹"服务费"法案、新设 PGSA 机构对违规船只罚款/扣押（id:136398/137344），霍尔木兹石油流量已降至 670 万桶/日（id:137280）。叠加美对加征 50% 关税、加方对等反制（id:138557/137307）。我们判断，当前风险偏好已从 risk-on 转为防御，核心矛盾从"地缘能否持续缓和"切换为"能源冲击 + 贸易战会否把滞胀叙事坐实、并压垮 AI 高估值资产的容错率"。8/17 基线已失效，后续分析须以升级 regime 为基准。

## 共识

1. 风险偏好已从 8/17 的 risk-on 逆转为防御，美伊经济战升级 + 美加贸易战是本周改变 regime 的最大地缘变量（共识，基于 id:138553/138557/137280）。
2. 8/26 NVDA 财报是 AI 资本开支叙事的"证明责任"节点，指引质量比单季 beat 更关键（共识，ackman/soros）。
3. 长端美债收益率高企（30Y 5.248%、上周 19 年高 5.337%）是成长股估值的硬天花板，沃什 8/28 首秀是下半年关键观察点（共识，基于 id:137141/135539）。
4. 宏观组合正从"降温可降息"滑向"滞胀需紧缩"，能源冲击与贸易战为通胀提供环比燃料（共识，ackman）。
5. 散户借纳指 ETF 溢价追涨（id:138459）与机构借地缘/利率撤离的背离，显示风险尚未充分定价（共识，ackman）。
> 少数派：soros（8/17 基线）曾判断"MoU 延长降低全面升级概率、油价应回落"——该判断已被 8/23–24 现实（贝森特经济战、霍尔木兹 670 万桶/日）证伪，本稿以升级 regime 覆盖之。

## 各维度分析

### 叙事/情绪面

本周美股的核心叙事已从 8 月 17 日 index.md 定调的"地缘退潮 + 数据降温"彻底逆转。理解当前一切价格的总纲是：美股是一个由"AI 资本开支叙事 + 美联储路径 + 能源/地缘风险溢价"三脚架支撑的估值体系，而 8 月 23–24 日这三脚架中的"地缘"一脚被抽走——美伊从 MoU 延长式的缓和逆转为"经济战升级"，美加贸易战同步爆发。美财长贝森特 8/24 召开发布会宣布对伊"经济 D-Day"，切断一切经贸联系并威胁制裁其贸易伙伴（query_raw_items id:138553/137840）；伊朗反制推进霍尔木兹"服务费"法案、新设 PGSA 机构对违规船只罚款/扣押（id:136398/137344），霍尔木兹石油流量已降至 670 万桶/日（id:137280）。叠加美对加征 50% 关税、加方对等反制（id:138557/137307）。我们判断，当前风险偏好已从 risk-on 转为防御，核心矛盾从"地缘能否持续缓和"切换为"能源冲击 + 贸易战会否把滞胀叙事坐实、并压垮 AI 高估值资产的容错率"。8/17 基线已失效，后续分析须以升级 regime 为基准。

### 基本面

本周美股的核心叙事已从 8 月 17 日 index.md 定调的"地缘退潮 + 数据降温"彻底逆转。理解当前一切价格的总纲是：美股是一个由"AI 资本开支叙事 + 美联储路径 + 能源/地缘风险溢价"三脚架支撑的估值体系，而 8 月 23–24 日这三脚架中的"地缘"一脚被抽走——美伊从 MoU 延长式的缓和逆转为"经济战升级"，美加贸易战同步爆发。美财长贝森特 8/24 召开发布会宣布对伊"经济 D-Day"，切断一切经贸联系并威胁制裁其贸易伙伴（query_raw_items id:138553/137840）；伊朗反制推进霍尔木兹"服务费"法案、新设 PGSA 机构对违规船只罚款/扣押（id:136398/137344），霍尔木兹石油流量已降至 670 万桶/日（id:137280）。叠加美对加征 50% 关税、加方对等反制（id:138557/137307）。我们判断，当前风险偏好已从 risk-on 转为防御，核心矛盾从"地缘能否持续缓和"切换为"能源冲击 + 贸易战会否把滞胀叙事坐实、并压垮 AI 高估值资产的容错率"。8/17 基线已失效，后续分析须以升级 regime 为基准。

### 宏观背景

**ackman 视角：** 这种"机构借地缘与利率撤离、散户借 ETF 溢价追涨"的背离，是 regime 切换期最危险的结构——它意味着风险尚未被充分定价。纳指 ETF 的溢价不是信心，而是流动性过剩下的最后追涨；一旦 8/26 NVDA 财报或 8/28 沃什讲话打破 AI 容错率，溢价会迅速回吐并放大下行。我们判断当前情绪面处于"表面平静、底层松动"状态，不是底部。

## 预测时间线

| 时间窗 | 预测 | 置信度 | 提出者 | 提出日期 | 验证 |
|--------|------|--------|--------|----------|------|
| 8月20日（周三） | 美联储7月会议纪要发布（沃什主持的首次会议），市场将寻找是否讨论过加息可能性；若纪要偏鹰，美股短线承压 | 75% | soros | 2026-08-17 | 纪要原文 |
| 8月20日 | 中国8月LPR报价（1年期3.0%、5年期3.5%），大概率维持不变 | 85% | soros | 2026-08-17 | LPR公告 |
| 8月22日 | 美国8月制造业/服务业PMI初值，若制造业PMI跌破50将强化衰退叙事 | 65% | soros | 2026-08-17 | S&P Global |
| 8月22-26日 | Hot Chips 2026学术会议+第二届世界人形机器人运动会（中国），AI/半导体情绪催化 | 70% | soros | 2026-08-17 | 会议日程 |
| 8月26日 | 美国Q2 GDP修正值（初值1.5%年化），若下修将加深"滞胀→衰退"叙事 | 60% | soros | 2026-08-17 | BEA |
| 8月25-31日 | 英伟达Q2财报（预计8月26日后），AI资本开支叙事的核心验证事件 | 90% | soros | 2026-08-17 | NVIDIA IR |
| 8月22-24日 | 杰克逊霍尔全球央行年会，新任Fed主席沃什首次公开讲话 | 95% | soros | 2026-08-17 | Fed |
| 未来1-2周 | 霍尔木兹海峡通行量是否从当前极低水平（8月16日仅3艘次）回升，决定油价和风险偏好方向 | 80% | soros | 2026-08-17 | MarineTraffic |
| 9月15-16日 | FOMC会议（含SEP点阵图），当前市场定价加息概率33% | 90% | soros | 2026-08-17 | Fed |
| 8/24 当周 | 贝森特伊朗"经济 D-Day"发布会落地，制裁清单与贸易伙伴条款决定油价与风险溢价方向 | 85% | ackman | 2026-08-24 | 发布会原文/制裁清单 |
| 8/26 盘后 | NVDA 财报：AI 容错率试金石；指引保守则半导体链与云资本开支叙事承压 | 90% | ackman | 2026-08-24 | NVDA IR |
| 8/26 | Q2 GDP 修正（前值 1.5% 年化）+ 7 月核心 PCE（前值 3.3% yoy）+ 耐用品订单同日公布，定调滞胀/衰退 | 80% | ackman/soros | 2026-08-24/17 | BEA |
| 8/27–29 | Jackson Hole 年会，沃什 8/28 首秀；若转鹰将同时压长端利率与风险偏好 | 85% | ackman | 2026-08-24 | Fed |
| 9/4 | 8 月非农（前值 -2.3 万、失业率 4.1%）；连续为负将坐实就业衰退叙事 | 75% | soros | 2026-08-17 | BLS |
| 未来 1–2 周 | 霍尔木兹流量能否从 670 万桶/日回升，决定油价与风险偏好方向 | 80% | soros | 2026-08-17（regime 已更新） | MarineTraffic |

## 分歧地图

| 维度 | 观点 A | 观点 B | 分歧根因 | 状态 |
|------|--------|--------|---------|------|
| Fed 路径 | 7 月纪要多位官员称需加息（id:132467）；沃什 Jackson Hole 或转鹰 | Kashkari/Daly 淡化债市担忧、称政策"在好位置"（id:136039/135028） | 分歧在于能源/贸易战推升的环比通胀 vs 就业消费走弱——前者要求紧缩，后者支持观望；沃什立场是未知变量 | — |
| AI 估值 | 欧洲央行：科技股估值处"亢奋"水平、政策缓冲有限（index.md 8/17） | Evercore ISI：标普 12 个月看 9000 点（+16%）（index.md 8/17） | 分歧在于 AI 资本开支能否转化为 EPS——8/26 NVDA 财报是试金石；当前 30Y 5.248% 抬高贴现率分母 | — |
| 美伊局势 | 市场交易 8/17 MoU 延长式缓和 | 现实：贝森特"经济 D-Day"、霍尔木兹 670 万桶/日、PGSA 执法（id:138553/137280/137344） | 分歧在于"纸面缓和"vs"实际升级"——海峡流量与制裁条款尚未确认改善，8/17 基线已失效 | — |
| 美加贸易 | 美方：50% 关税施压 | 加方：暂停谈判、对等反制，且预示贸易战延续至中期选举后（id:136353/137307） | 分歧在于"短期谈判筹码"vs"长期结构性脱钩"——若延续至中期选举，将系统性抬升美国输入性通胀 | — |
| Fed路径 | 高盛：市场对Fed政策押注仍太鹰，9月加息"可能性非常小"，弱数据+温和通胀支持观望（2026-08-17） | 富国：预计今年加息25bp、2027年再加25bp至4.00-4.25%，能源通胀可能迫使Fed行动（2026-08-17） | 分歧在于如何权衡"就业消费走弱"vs"能源通胀上行"——前者支持暂停，后者要求继续紧缩；伊朗海峡通行恢复速度是关键变量 | — |
| AI估值 | Evercore ISI：标普500可在12个月内达9000点（+16%），AI热潮+低杠杆+持仓多元化支撑（2026-08-17） | 欧洲央行：美股科技股估值处"亢奋"水平，政策缓冲空间有限，回调"可能产生广泛影响"（2026-08-17） | 分歧在于AI资本开支能否转化为足够的EPS增长来支撑当前估值——乐观方看OpenAI-$6000亿协议锁定了需求，悲观方看盈利验证尚缺完整证据 | — |
| 中国市场 | 浦银国际：港股最差阶段或已过去，反弹仍未结束，AI主题对冲基金清仓后杠杆已部分出清（2026-08-17） | 固定资产投资恶化至-6.7%、零售增速降至1.2%、PMI双收缩，内需尚未触底 | 分歧在于"估值修复驱动"vs"盈利基本面驱动"——前者看风险偏好改善和回购，后者要求广告/消费/企业云实际改善 | — |

> **审查意见**：4 条（详见 _history/review/）

## 数据来源

- BTCUSDT 最新价: binance_get_price(symbol=BTCUSDT) = 77,786.1 USDT (2026-08-24 11:16 UTC)
- ETHUSDT 最新价: binance_get_price(symbol=ETHUSDT) = 2,466.63 USDT (2026-08-24 11:16 UTC)
- 美国CPI同比: query_indicators(category=macro,country=us)[cpi_yoy_us_pct] = 3.4% (数据日2026-07-01, 距今54天偏旧)
- 美联储资产负债表: query_indicators(category=macro,country=us)[fed_balance_sheet] = 6,759,955 百万美元 ≈ 6.76万亿美元 (数据日2026-08-12, 12天前)
- 美国核心CPI: query_indicators(category=macro,country=us)[core_cpi] = 336.789 (数据日2026-07-01)
- 美国消费者信心: query_indicators(category=macro,country=us)[consumer_confidence_us] = 49.5 (数据日2026-06-01, 84天前过时)
- 美国GDP: query_indicators(category=macro,country=us)[gdp] = 32,475.21 (数据日2026-04-01, 145天前过时)
- 美伊最严制裁: query_raw_items(keyword='iran OR Bessent')[id:138432] = aljazeera: US threatens toughest sanctions yet against Iran (2026-08-24 10:48 UTC)
- 伊朗地震级报复: query_raw_items()[id:137840] = npr: Iran warns of 'seismic' retaliation if US follows through (2026-08-24 09:02 UTC)
- 美加关税战: query_raw_items()[id:135487] = npr: Canada retaliatory tariffs starting Sept 8 after US 50% tariffs on ~$20bn (2026-08-23)
- Kashkari谈收益率: query_raw_items()[id:136039] = bloomberg: Kashkari says Treasury market still working 'as it should' (2026-08-23)
- 沃什Jackson Hole: query_raw_items()[id:135539] = bloomberg: Warsh to make first Jackson Hole speech as Fed Chair (2026-08-23)
- 伊朗经济D-Day: query_raw_items(keyword='iran OR Bessent')[id:138000] = aljazeera: US threat of 'economic D-Day' for Iran tests China detente (2026-08-24 09:32 UTC)
- 霍尔木兹服务费: query_raw_items()[id:136398] = aljazeera: Iran parliament advances Hormuz service fees draft law (2026-08-24 00:36 UTC)
- 加拿大对等报复: query_raw_items()[id:135528] = aljazeera: Canada to enact retaliatory US tariffs starting Sept 8 (2026-08-23)
- 美国关键日历: query_calendar_events(country=US,importance=high,medium,days=14) = 8/26 NVDA财报+GDP修正(前值1.5%)+核心PCE(前值3.3% yoy); 8/27-29 Jackson Hole; 9/4 非农(前值-2.3万,失业率4.1%); 7月新屋开工123.9万户(预期134.5,前值142.7)
- 数据缺口: market_quote/longbridge 美股报价失败(Longbridge not configured); query_indicators(sentiment/bond, US)=0条(VIX/美债收益率/美元无数据); 黄金/原油路由 search_routes 未命中


- 霍尔木兹石油流量降至670万桶/日: query_raw_items(keyword=hormuz)[id:137280] = 经过霍尔木兹海峡的石油流量已降至670万桶/日，船只通行量显著减少
- 美财长贝森特对伊"经济D-Day": query_raw_items(keyword=iran OR bessent)[id:138553] = Iran faces 'economic D-Day', US treasury secretary warns (2026-08-24 11:17)
- 美财长发布会加大经济施压: query_raw_items(keyword=iran OR bessent)[id:137840] = 美财长就伊朗问题开发布会加大经济施压；加拿大誓言反制关税 (2026-08-24 09:02)
- 伊朗"地震级"报复警告: query_raw_items(keyword=iran)[id:138432] = US threatens toughest sanctions yet; Iran warns seismic retaliation if US follows through (2026-08-24 10:48)
- 伊朗霍尔木兹"服务费"法案: query_raw_items(keyword=hormuz)[id:136398] = Iranian parliament advances plans for Hormuz service fees (2026-08-24 00:36)
- PGSA对违规船只罚款/扣押: query_raw_items(keyword=PGSA OR hormuz)[id:137344] = 伊朗PGSA警告违反霍尔木兹通行规则的船只将面临限制通行、罚款、扣押或没收 (2026-08-24 07:28)
- 美海军陆战队取消韩演因伊朗战争需求: query_raw_items(keyword=iran OR hormuz)[id:138002] = US Marines cancel drill with South Korea, citing Iran war demands (2026-08-24 09:32)
- 美加贸易战50%关税: query_raw_items(keyword=canada OR tariff)[id:138557] = US-Canada trade war; Canada rare tough stand against Trump tariffs (2026-08-24 11:17)
- 加拿大暂停对美贸易谈判对等反制: query_raw_items(keyword=canada OR tariff)[id:137307] = Canada suspends US trade talks as Trump imposes 50% tariffs, Ottawa vows dollar-for-dollar retaliation
- 美债10Y 4.714%(-2.2bp)/30Y 5.248%(-2.7bp)/30Y上周19年高5.337%: query_raw_items(keyword=美债收益率)[id:137141] = 美债收益率亚洲时段下滑但仍处高位；30Y上周升至19年来高点5.337% (2026-08-24 05:58)
- 金价升至逾三个月高位: query_raw_items(keyword=金价)[id:136692] = 金价升至逾三个月高位，聚焦PCE与沃什讲话 (2026-08-24 02:23)
- 中国A股深证-3.00%/上证-1.03%/创业板-4.28%: query_raw_items(keyword=深证成指)[id:137089] = 深证成指跌3.00%、上证-1.03%、创业板-4.28% (2026-08-24 05:33)
- KOSPI -3%: query_raw_items(keyword=KOSPI)[id:136812] = 韩国综合股价指数下跌3%，报6702.87点 (2026-08-24 03:19)
- 纳指ETF易方达溢价风险: query_raw_items(keyword=纳指 ETF)[id:138459] = 收盘1.998元 vs IOPV 1.8442元，溢价显著 (2026-08-24 10:53)
- BTC现价77803.3美元(+0.78%): binance_get_price(BTCUSDT) = 77803.3; binance_get_ticker(BTCUSDT) = +0.78%, high 78057.6, low 76649.0 (2026-08-24 11:26 UTC)
- NVDA洽谈投资Perplexity(估值>300亿): query_raw_items(keyword=nvda OR perplexity)[id:136806] = 英伟达洽谈投资Perplexity，后者估值或超300亿美元 (2026-08-24 03:13)
- NVDA披露210亿美元SpaceX持仓: query_raw_items(keyword=nvda OR spacex)[id:128533] = Nvidia discloses $21B stake in SpaceX (2026-08-16)
- 穆迪确认NVDA Aa1展望积极: query_raw_items(keyword=穆迪 OR 英伟达)[id:129641] = 穆迪确认英伟达Aa1评级，展望积极 (2026-08-18)
- 标普确认NVDA AA: query_raw_items(keyword=标普 OR 英伟达)[id:129189] = 标普确认英伟达AA发行人信用评级 (2026-08-18)
- 俄无人机用Nvidia芯片: query_raw_items(keyword=nvda OR drone)[id:137919] = 俄AI无人机搭载Nvidia Jetson Orin (2026-08-24 09:17)
- FOMC 7月纪要多位官员称需加息: query_raw_items(keyword=fed OR minutes)[id:132467] = Fed Minutes Show Many Officials Said Rate Hikes May Be Needed (2026-08-19)
- 美债突破40万亿美元: query_raw_items(keyword=debt OR 40万亿)[id:132632] = US debt tops record $40 trillion (2026-08-19)
- Warsh 8/28 Jackson Hole首秀: query_raw_items(keyword=warsh OR jackson hole)[id:135539] = Kevin Warsh to Make First Jackson Hole Speech as Fed Chair (2026-08-23)
- 美7月新屋开工123.9万(-12.4%)/成屋签约-2.3%: query_calendar_events(country=US, lookback=7) = actual 7月新屋开工123.9万(-12.4% MoM)、成屋签约-2.3%
- 8/26 NVDA财报+Q2 GDP修正(1.5%)+核心PCE(3.3%): query_calendar_events(country=US, days=14) = 事件确认
- CPI 3.4% yoy(2026-07-01,54天前偏旧): query_indicators(category=macro, country=us) = cpi_yoy_us 3.4 (data 2026-07-01)
- 美联储资产负债表6759955百万美元(2026-08-12): query_indicators(category=macro, country=us) = fed_balance_sheet 6759955.0 (data 2026-08-12)
- 加拿大预示贸易战延续至中期选举后: query_raw_items(keyword=canada OR tariff)[id:136353] = Canada Sees Long Trade War With US That May Last Beyond Midterms (2026-08-24 00:17)

## 更新日志

| 日期 | 操作者 | 变更摘要 |
|------|--------|---------|
| 2026-08-24 19:33 | theme_publish | 更新（big_picture_lead_ackman_marketquotetool_longbridge_finalize） |
| 2026-08-24 19:29 | theme_publish | 更新（big_picture_lead_ackman_marketquotetool_longbridge_finalize） |
| 2026-08-17 23:19 | theme_publish | 更新（big_picture_lead_ackman_marketquotetool_longbridge_finalize） |
| 2026-08-09 14:24 | theme_publish | 更新（theme_update） |
| 2026-08-01 | 人类 | 创建 theme 骨架 |
