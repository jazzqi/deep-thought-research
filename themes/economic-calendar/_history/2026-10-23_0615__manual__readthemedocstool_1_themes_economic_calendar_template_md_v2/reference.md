# W42 (2026-10-12~10-18) 增量补丁 · 数据溯源

## 目标周事件实际值（query_calendar_events, days=14, lookback_days=10, importance=high/medium）
- 美国9月CPI同比: query_calendar_events(importance=high,lookback_days=10) = 实际3.7（前值3.4，共识3.6，10-14公布）
- 美国9月核心CPI同比: query_calendar_events(importance=high) = 实际2.6（前值2.4，共识2.5）
- 美国9月CPI环比: query_calendar_events(importance=medium) = 实际0.6（共识0.6，前值0.4）；核心环比0.3（共识0.2，前值0.3）
- 美国9月PPI同比: query_calendar_events(importance=medium) = 实际6.3（前值5.6，共识5.3~5.4）；核心PPI同比5.0（前值4.6，共识4.4）
- 美国9月PPI环比: query_calendar_events(importance=medium) = 实际1.3（共识0.6）；核心环比0.7（共识0.3）
- 美国9月零售销售环比: query_calendar_events(importance=high) = 实际+0.8（共识+0.3，前值+1.2/+1.3）；控制组+0.1（共识+0.3，前值+1.2）
- 美国10/10当周初请: query_calendar_events(importance=high) = 实际19.9万（共识20.0万，前值19.8万）；续请171.0万
- 美国10月纽约联储制造业指数: query_calendar_events(importance=medium) = 实际25.5（共识10.25~12.0，前值7.6）
- 美国10月费城联储制造业指数: query_calendar_events(importance=medium) = 实际20.9（共识28.0~28.4，前值37.8）
- 美国9月工业产出环比: query_calendar_events(importance=medium) = 实际+0.7（共识+0.4，前值0.0）；产能利用率76.9
- 美国9月进口价格指数: query_calendar_events(importance=medium) = 环比+1.1（共识+0.8~1.0）、同比+8.1（前值+7.0）
- 美国10/9当周EIA原油库存: query_calendar_events(importance=medium) = -855.7万桶（预期+15万桶）；汽油+351.8万桶
- 美国9月NFIB中小企业乐观指数: query_calendar_events(importance=medium) = 97.9（共识98.0，前值98.7）
- 美国9月成屋销售年化: query_calendar_events(importance=medium) = 399万户（共识395万，前值393~398万，多源前值不一致）
- 中国9月M2同比: query_calendar_events(importance=high) = 实际7.2（前值7.5，共识7.4）；M1同比3.2（前值4.1）
- 中国1-9月新增人民币贷款: query_calendar_events(importance=high) = 115,200亿（前值104,400亿）
- 中国1-9月社融增量: query_calendar_events(importance=high) = 274,600亿（前值239,100亿）
- 中国9月出口(美元计): query_calendar_events(importance=medium) = 同比+36.3%（共识+25.3%，前值+25.0%）；进口+31.0%；贸易帐1,335.3亿美元（共识1,181亿）
- 中国9月CPI/PPI: query_calendar_events(importance=medium) = CPI同比0.9（共识1.0，前值0.8）；PPI同比5.0（共识4.5，前值3.8）
- 欧元区9月HICP终值: query_calendar_events(importance=medium) = 同比3.8、核心2.2（均持平前值/共识）
- 英国8月GDP环比: query_calendar_events(importance=medium) = +0.1%（共识-0.1%，前值+0.4%）；三个月+0.7%
- 日本9月企业商品物价: query_calendar_events(importance=medium) = 同比6.8（共识7.6，前值7.6）、环比-0.3（共识+0.5）
- 澳大利亚9月就业: query_calendar_events(importance=medium) = -3.93万（共识+2.0万）；失业率4.7（共识4.6）
- 德国9月CPI终值: query_calendar_events(importance=medium) = 同比3.3、环比0.6（持平共识）

## 10-22 定版补丁窗口行情（query_raw_items, source=telegram:Financial_Express, published_after=2026-10-18/10-14）
- 美债收益率(10-22收): query_raw_items(keyword='10Y OR 美债...',published_after=2026-10-18)[id:506230] = 10Y 4.9530%(-16.6bp)，2Y 4.6396%(-16.63bp)，30Y 5.2804%
- 10Y跌破5%: query_raw_items(...)[id:505882] = AI概念股大跌避险买盘推动，各期限收益率最多跌16bp，5-30年触及近一个月最低
- 标普500(10-22收): query_raw_items(...)[id:506189] = 7663.43点(-1.21%)，逼近100日均线7603.55；等权指数+0.34%
- 美股收盘: query_raw_items(...)[id:506104] = 道指+0.02%、标普-1.21%、纳指-2.57%；英伟达-4.45%、Meta-7%
- AI叙事动摇: query_raw_items(...)[id:506169] = 纳指创6月以来最大跌幅，资金转向债券避险
- MSCI EM/沙特袭击: query_raw_items(...)[id:506166] = MSCI新兴市场指数-2.5%创7月以来新低；沙特致命袭击后布伦特升破111美元
- 布伦特/WTI(10-22收): query_raw_items(...)[id:506004] = 布伦特12月113.17美元/桶(+4.0%)，WTI 99.47美元(+2.39%)
- 现货黄金(10-22收): query_raw_items(...)[id:506214] = 4028.58美元/盎司(-2.71%)，逼近4000关口；白银-5.87%
- 美元指数(10-22收): query_raw_items(...)[id:506030] = ICE DXY 101.599(-0.18%)；USDJPY 156.78
- CME FedWatch(10-22): query_raw_items(keyword='加息 OR FedWatch...',published_after=2026-10-14)[id:506248] = 10月维持不变92.8%、加息25bp 7.2%；12月累计加息25bp 74.8%、50bp 5.7%、维持5.7%（另一条[id:506237]维持/50bp数值互换，以[id:506248]为准）
- 法国债市: query_raw_items(...)[id:506058] = OAT-Bund利差一度扩至178bp，为2011年欧债危机以来最高
- 韩国KOSPI: query_raw_items(...)[id:503364] = -3.52%报5533.77，芯片领跌，创4月7日以来最低收盘
- 菲律宾央行: query_raw_items(...)[id:503164] = 意外加息50bp至5.5%
- 日本央行10月会议: query_raw_items(...)[id:503258] = 计划10-29/30会议维持1.25%不变，观察9月加息影响
- 韩国央行10-21决议后表态: query_raw_items(...)[id:502630] = 进一步加息时机取决于后续数据评估
- 双线资本长债观点: query_raw_items(...)[id:505870] = 政府举债+需求疲软继续施压长端，低配/做空长端美债

## 承接来源（ReadThemeDocsTool）
- W41预读预测总表: themes/economic-calendar/2026-10-05__2026-10-11/forecast.md = 9月M2预判7.3-7.7%（dalio）；10/3当周初请预判20-21万（dalio）
- W41观察清单: 同上 = 霍尔木兹封锁/柴油出口禁令/MOVE+29.69%/美联储RMP购债加码/银行监管门槛等
- W41 recap: themes/economic-calendar/2026-10-05__2026-10-11/recap.md = 不存在（index.md标注"⏳待补"），承接以W41 forecast替代

## 备注
- FactPack锚点（FedWatch 9月维持59.9%/加息40.1%，CME 2026-08-26）已过时，当前以[id:506248]（10-22）为最新定价；锚点为只读，不改。
- market_quote(SPX.US) 调用失败（longbridge token expired），美股水平改用快讯收盘数据。
- USDCNH 当日水平未检索到 → 报告标⚠️缺行情。

- 10-22 现货黄金 4,028.58 美元/盎司（单日 -2.71%）: query_raw_items(keyword='黄金 OR 金价', published_after=2026-10-16)[id:506214] = 国际金价跌 2.7%，逼近 4000 美元整数位心理关口
- 10-22 离岸人民币 CNH 6.6721（在岸 6.6748）: query_raw_items(keyword='美元指数 OR 人民币', published_after=2026-10-16)[id:506200] = 周四纽约尾盘 CNH 报 6.6721，逼近 2022-06-15 的 6.6687
- 10-22 美元指数收 101.608（-0.17%）: query_raw_items(keyword='美元指数 OR 人民币', published_after=2026-10-16)[id:506032] = 美元指数 22 日下跌，尾市收于 101.608
- 10-22 标普 500 收 7,663.43（-1.21%，逼近 100 日均线 7,603.55）: query_raw_items(keyword='标普 OR 纳指', published_after=2026-10-17)[id:506189] = 标普 500 收跌 93.74 点报 7663.43 点
- 10-22 纳指 -2.6%（6 月以来最大单日跌幅）、Meta -7%、英伟达 -4.45%: query_raw_items(keyword='标普 OR 纳指', published_after=2026-10-17)[id:506169] = 美股市场重新评估 AI 热潮的可持续性，纳指创 6 月以来最大跌幅
- 10-22 美股板块/指数明细（费半 -6.7%、存储芯片指数 -8%、CoreWeave -10%）: query_raw_items(keyword='标普 OR 纳指', published_after=2026-10-17)[id:506101] = 费城半导体指数跌 6.7%、存储芯片指数初步收跌 8%
- 10-22 5Y UST -15bp 报 4.8%、30Y -10bp 报 5.3%: query_raw_items(keyword='标普 OR 纳指', published_after=2026-10-17)[id:505806] = 美国五年期国债收益率跌 15 个基点报 4.8%；30 年期跌 10 个基点报 5.3%
- 伊朗最高领袖罕见露面、军方警告"炸弹之父"、海底电缆或为目标: query_raw_items(keyword='黄金 OR 金价', published_after=2026-10-16)[id:505064] = 美以密谋新一轮打击？伊朗最高领袖罕见露面，军方警告祭出"炸弹之父"
- 10-22 标普 500 板块表现（电信 -3.01%、科技 -3%、公用事业 +1.98%、必选消费 +3.11%）: query_raw_items(keyword='标普 OR 纳指', published_after=2026-10-17)[id:506251] = 标普 500 十一大板块涨跌各异，电信板块收跌 3.01%

- CME FedWatch 10月/12月利率定价（10-21）: query_raw_items(keyword='FedWatch OR 沃什 OR Warsh OR 加息概率', published_after=2026-10-21)[id:502036] = 10月维持83.9%/加息25bp 16.1%；12月维持9.9%/+25bp 76.0%/+50bp 14.2%
- Brent/WTI 10-22 结算价: query_raw_items(keyword='沙特 OR Brent OR 布伦特 OR 油价', published_after=2026-10-21T12:00)[id:506000] = Brent 12月合约113.17美元/桶（+4.0%）、WTI 99.47（+2.39%），布油创5月以来最高
- 密歇根/俄亥俄汽油价格与中期选举压力（10-22）: query_raw_items(keyword='沙特 OR Brent OR 布伦特 OR 油价', published_after=2026-10-21T12:00)[id:506053] = 密歇根普通汽油均价涨17美分至4.61美元/加仑，俄亥俄暂停州级汽柴油消费税，距中期选举约12天
- 瓦莱罗Q3创纪录炼油利润: query_raw_items(keyword='沙特 OR Brent OR 布伦特 OR 油价', published_after=2026-10-21T12:00)[id:506008] = Q3利润创历史纪录并超预期，伊朗/乌克兰战争燃料供应中断推升利润率，柴油价格创历史新高
- 特朗普对伊朗表态/普京愿恢复三方接触（10-22隔夜要闻）: query_raw_items(keyword='伊朗 OR Iran OR 福尔多', published_after=2026-10-20)[id:506284] = 特朗普"可能进一步采取行动"；普京愿恢复俄美乌三方接触
- 霍尔木兹海峡7船被击中: query_raw_items(keyword='伊朗 OR Iran OR 福尔多', published_after=2026-10-20)[id:505958] = 伊朗称霍尔木兹7船被击中并警告更大回应，美方斥为选前抬油价
- 美中央司令部"钢铁之墙"海上封锁第100天: query_raw_items(keyword='伊朗 OR Iran OR 福尔多', published_after=2026-10-20)[id:505929] = 已阻止伊朗出口至少250亿美元原油
- SK海力士终止Solidigm美国IPO（10-22）: query_raw_items(keyword='FedWatch OR 沃什 OR Warsh OR 加息概率', published_after=2026-10-21)[id:506267] = 基于市场环境与股价走势终止IPO审核
- 中国10Y国债收益率历史新低（10-22）: query_raw_items(source=telegram:Financial_Express, published_after=2026-10-22T12:00)[id:506271] = 10-22触及历史低位1.6414%
- 彭博信息科技指数/AI赢家指数 10-22 跌幅: query_raw_items(source=telegram:Financial_Express, published_after=2026-10-22T12:00)[id:506282] = 信息科技指数收跌4.53%，AI赢家指数跌6.27%，COHR/CoreWeave等至少跌10%
- 标普500半导体指数 10-22: query_raw_items(source=telegram:Financial_Express, published_after=2026-10-22T12:00)[id:506276] = 收跌5.45%，10-14已跌破50日/100日均线，逼近200日均线
- 英国10月GfK消费者信心（10-22）: query_raw_items(source=telegram:Financial_Express, published_after=2026-10-22T12:00)[id:506285] = -24，预期-14，前值-13，大额采购指数降至2024年9月以来最低
- MSCI EM指数 10-22: query_raw_items(keyword='沙特 OR Brent OR 布伦特 OR 油价', published_after=2026-10-21T12:00)[id:506166] = 跌2.5%创7月以来新低，净石油进口国货币领跌
- RBC中期选举美债情景（10-22）: query_raw_items(keyword='伊朗 OR Iran OR 福尔多', published_after=2026-10-20)[id:505922] = 民主党横扫→AI监管+避险美债上涨；共和党维持两院→财政扩张延续利空美债
- IMF中东区域经济展望（10-22）: query_raw_items(source=telegram:Financial_Express, published_after=2026-10-22T12:00)[id:506268] = 受美以伊冲突影响，2026年中东/北非/阿富汗/巴基斯坦经济预计萎缩1.3%

- 伊朗局势（10-22 定稿后仍在升级）: query_raw_items(keyword='伊朗 OR 炸弹', published_after=2026-10-14)[id:506149/id:506151/id:506205] = 特朗普 10-22 晚再度威胁对伊朗军事行动"可能还会再进一步"
- "炸弹之父"归属核验: query_raw_items(keyword='炸弹', published_after=2026-10-16)[id:502844/id:505064] = 伊朗革命卫队发言人 10-21 宣布准备推出"炸弹之父"；伊朗最高领袖罕见露面、海底电缆或成反击目标（"炸弹之母"为美方 10-18 前后威胁，id:490944）
- 美方"炸弹之母"威胁: query_raw_items(keyword='炸弹', published_after=2026-10-16)[id:490944] = CNN 报道美方威胁对伊使用"炸弹之母"，伊朗新国防部长称已采取必要措施
- 沙特遭袭+布油破 111-112: query_raw_items(keyword='炸弹', published_after=2026-10-16)[id:505064] = 胡塞称对沙特发动多轮袭击（含国防部、沙特阿美原油设施），布油突破 112 美元
- 沙特致命袭击推升油价: query_raw_items(keyword='沙特', published_after=2026-10-19)[id:505856] = 沙特致命袭击后供应担忧加剧，布伦特升破 111 美元/桶
- 美军"钢铁之墙"海上封锁第 100 天: query_raw_items(keyword='伊朗 OR 炸弹', published_after=2026-10-14)[id:505929] = 美中央司令部称已阻止伊朗出口至少 250 亿美元原油
- 印尼央行按兵不动: query_raw_items(keyword='印尼股市 OR 印尼股指 OR 印尼暴跌', published_after=2026-10-08)[id:499205/id:499143] = 印尼央行维持指标利率不变、上调存款工具利率，MSCI 降级冲击威胁印尼盾
- 印尼主权基金托市+反弹: query_raw_items(keyword='印尼股市 OR 印尼股指 OR 印尼暴跌', published_after=2026-10-08)[id:503124/id:502550] = Danantara 入场买股，雅加达综合指数盘中跌 2.7% 后反弹至 +1.8%，此前上周五（10-16）遭遇近三十年最大跌幅、MSCI 警告新兴市场地位难保
- 淡马锡/GIC 被控"做空印尼后抄底"遭否认: query_raw_items(keyword='印尼股市 OR 印尼股指 OR 印尼暴跌', published_after=2026-10-08)[id:499341] = 印尼前贸易部长指控，两机构否认
- 10-22 费半暴跌与 AI 退潮: query_raw_items(keyword='台积电', published_after=2026-10-14)[id:506067] = 费城半导体指数日内跌 7%，英伟达 -4.61%、台积电 ADR -4.84%、阿斯麦 ADR -6.92%
- MSCI 新兴市场指数创 7 月新低: query_raw_items(keyword='印尼 OR MSCI', published_after=2026-10-05)[id:506166] = MSCI EM 指数跌 2.5%，布油创 5 月新高之际净石油进口国货币领跌
- 10-22 Brent 参照（稿外时点核验）: 个人记忆（2026-10-22 定版时点）= Brent 113.17 美元/桶（沙特致命袭击驱动 +4%，5 月以来最高）
