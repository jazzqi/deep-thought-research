# 数据来源（2026-10-04 主题更新轮）

## 股价与估值（【新增】2026-10-02 数据）
- PDD 收盘价 $75.38（2026-10-02，-1.46%），盘后 $75.52: fetch_url(finance.yahoo.com/quote/PDD/) = 75.38, at close October 2
- PE TTM 8.12x，EPS TTM $9.28: fetch_url(finance.yahoo.com/quote/PDD/) = PE Ratio (TTM) 8.12, EPS (TTM) 9.28
- 市值 $107.296B: fetch_url(finance.yahoo.com/quote/PDD/) = Market Cap (intraday) 107.296B
- 52 周区间 $71.94-$139.41: fetch_url(finance.yahoo.com/quote/PDD/) = 52 Week Range 71.94 - 139.41
- YTD -33.78%，1Y -43.85%，6M -25.27%: fetch_url(finance.yahoo.com/quote/PDD/) = chart range labels
- 分析师 1Y 目标价 $114.60（基线 $116.74，下调 1.8%）: fetch_url(finance.yahoo.com/quote/PDD/) = 1y Target Est 114.60
- 下次财报预估 2026-11-18: fetch_url(finance.yahoo.com/quote/PDD/) = Earnings Date (est.) Nov 18, 2026
- 基线收盘价 $87.75（2026-08-25）: FactPack 只读锚点 / 上期 index.md
- 39 天区间跌幅 -14.1%（$87.75→$75.38）: 上述两项计算

## 宏观与市场环境（【新增】）
- 10Y 美债收益率 5.28%、WTI 原油 $91.11、VIX 15.31（2026-10-02 页面快照）: fetch_url(finance.yahoo.com/quote/PDD/) = 10-Yr Bond 5.28 / Crude Oil Nov 26 91.11 / VIX 15.31
- 美国 10/2 非农新增就业 29k（前值 162k）: fetch_url(finance.yahoo.com/quote/PDD/) = Non-Farm Payrolls Oct 2 Prior: 162 New: 29（Yahoo 日历组件，数据源单一，采用时降权）
- 澳财长：美国对伊战争推高全球通胀与利率、拖累增长: query_raw_items(keyword='Temu OR EU OR 欧盟 OR 关税 OR de minimis', limit=30)[id:459620] = 查尔默斯称中东战争给通胀带来巨大上行压力，全球利率上升
- 胡塞武装称袭击沙特阿美利雅得炼油厂，沙特计划大规模反攻: query_raw_items(...)[id:459626] = 霍尔木兹/曼德海峡地缘风险升级
- 伊朗革命卫队 5 天内针对至少 7 艘"违规"油轮采取行动（霍尔木兹海峡）: query_raw_items(...)[id:459608] = 能源运输通道风险
- 金龙中国指数 9 月累跌 6.24%、Q3 累跌 2.59%，8/10 高点 6734.78 后持续走低: query_raw_items(keyword='PDD OR 拼多多 OR Temu', limit=40)[id:456562] = 9/30 收 5696.06
- 金龙指数 10/1 收跌 1.03% 报 5637.25，逼近 2024/8 低点: query_raw_items(...)[id:458570] = 拼多多当日跌 1.85%
- 金龙指数 9/29 收跌 1.55% 报 5662.29，拼多多跌 1.26%: query_raw_items(...)[id:453102]

## 中国宏观（【新增】）
- 9 月官方制造业 PMI 50.1（前值 49.8，预期 50.1）: query_calendar_events(country=CN) actual=50.1
- 9 月官方非制造业 PMI 50.2（前值 49.0）: query_calendar_events(country=CN) actual=50.2
- 9 月官方综合 PMI 50.7（前值 49.5）: query_calendar_events(country=CN) actual=50.7
- 9 月 RatingDog 制造业 PMI 52.1（前值 51.5）: query_calendar_events(country=CN) actual=52.1
- 8 月规模以上工业企业利润单月同比 +4.2%（前值 11.2%），1-8 月累计 +15.7%（前值 17.6%）: query_calendar_events(country=CN) actual=4.2 / 15.7
- 9 月 CPI 同比前值 0.8、PPI 前值 3.8，10/14 公布: query_calendar_events(country=CN) previous=0.8 / 3.8
- 9 月 1Y/5Y LPR 维持 3.0%/3.5%: query_calendar_events(country=CN) previous=forecast=3.0/3.5
- 基线宏观锚点（1-7 月社零 +1.2%、7 月制造业 PMI 49.2）: 上期 index.md【基线】

## Temu/竞争/监管（【新增】2026-08-26 后）
- 法国通过反快时尚法，对 Shein/Temu 销售廉价服装罚款: query_raw_items(keyword='Temu', limit=15, published_after='2026-08-26')[id:227818] = 2026-09-01
- 法国修法被评"假环保真保护主义"，主要针对中国品牌: query_raw_items(...)[id:286774] = 2026-09-04
- Temu 悄然推出自营品牌 BEMUVO，商标主体指向 PDD 关联公司: query_raw_items(...)[id:310612] = 2026-09-08，官方渠道直接供货
- Temu 与罗马尼亚邮政（Poșta Română）签物流 MoU: query_raw_items(...)[id:242855] = 2026-09-02
- Temu 与塞浦路斯 CITEA 签 MoU 支持数字商业社区: query_raw_items(...)[id:411788] = 2026-09-16
- 免税红利消失，全托管商家"分流迁移"半托管/Y2 模式: query_raw_items(...)[id:228526] = 2026-09-01，Temu 类平台价格优势减弱
- Fortune：Temu 在 Meta 投放高达 $9.62 亿"AI slop"广告: query_raw_items(...)[id:236620] = 2026-09-02
- SHEIN 港股上市推进（恒指点名/竞争分流）: query_raw_items(...)[id:248364][id:249083] = 2026-09-02
- SHEIN 预计 9/28 收盘后公布财报: query_calendar_events(country=CN) = 2026-09-28
- DBS 因 Shopee 支出拖累下调 Sea 目标价: fetch_url(finance.yahoo.com/quote/PDD/) 新闻列表 = Investing.com 1d ago（行业利润率承压佐证）
- 拼多多雄安公司员工突破 5000 人，3 个多月完成全年招聘: query_raw_items(keyword='拼多多', limit=25)[id:438605][id:438469] = 2026-09-23
- 上海网信办召集 17 家平台（含拼多多）部署未成年人保护: query_raw_items(...)[id:454989] = 2026-09-30，平台监管常态化非针对性打压
- A 股"拼多多概念"板块涨幅居前: query_raw_items(...)[id:433200] = 2026-09-22

## 基线数据（沿用 2026-08-26 定版，未过时部分）
- Q2 2026 营收 1,124 亿元（Miss 2.4%）、调整后每 ADS 收益 19.33 元（Beat 4.4%）: 上期 reference.md【基线】
- FY2025 Revenue $60.53B / Net Income $13.71B / OCF $14.99B / FCF $12.00B: 上期 reference.md【基线】
- FY2025 营收 +10.6%、净利 -12.2% YoY: 上期 index.md【基线】
- 管理层电话会：陈磊"欧盟关税短期重大影响""不改全球化方向"；赵佳臻"品牌自营需更长时间": 上期 index.md【基线】
- 速卖通巴西大促首日超越 Temu: 上期 reference.md【基线】[id:140665]

## 工具失败记录（透明度）
- market_quote / market_kline（PDD.US）: OpenApiException 401003 token expired（2026-10-04 执行时）
- query_longbridge_by_route news/company（PDD.US）: 同上 token expired
- query_longbridge_by_route fundamental/consensus（PDD.US）: 返回空数组 []
- query_indicators(country=china): 仅 cn_exports/cn_imports，且数据超 90 天已标过时，未采用
- FedWatch 最新数据: 当前工具集无对应查询能力，8/26 锚点视为过时

# 数据来源（2026-10-04 session · buffett）

## 行情与估值（2026-10-02 收盘基准）

- PDD 收盘价 $75.38、盘后 $75.52: fetch_url(finance.yahoo.com/quote/PDD/) = 2026-10-02 close -1.46%
- PDD 市值 $107.296B、PE TTM 8.12x、EPS TTM $9.28: fetch_url(finance.yahoo.com/quote/PDD/)
- PDD 52周区间 $71.94–$139.41、1Y一致目标价 $114.60、Beta -0.01: fetch_url(finance.yahoo.com/quote/PDD/)
- PDD YTD -33.78%、1Y -43.85%、5D -3.96%、1M -7.66%: fetch_url(finance.yahoo.com/quote/PDD/)
- Q3 财报预估日期 2026-11-18: fetch_url(finance.yahoo.com/quote/PDD/) = Earnings Date (est.)
- 长桥 fundamental/valuation/pe、valuation/history、consensus、analyst/forecast_eps 对 PDD.US 均返回空: query_longbridge_by_route = 数据缺失，以 Yahoo 为准

## 美国宏观与货币政策

- FOMC 2026-09-16 加息 25bp 至 3.75–4.00%（12-0 全票，声明称通胀仍高企）: fetch_url(federalreserve.gov/newsevents/pressreleases/monetary20260916a.htm) = 声明全文
- 10Y 美债 5.28%、WTI 原油 $91.11、VIX 15.31、黄金 $4,162.30: fetch_url(finance.yahoo.com/quote/PDD/) = 页首市场横幅（10/2 盘后）
- 9月美国失业率 4.2%（前值 4.1%）: query_calendar_events(country=US, lookback_days=14) = actual 4.2
- 9月 ISM 制造业 54.5（预期 55.0）: query_calendar_events(country=US) = actual 54.5
- Q2 实际GDP年化季环比终值 +2.2%: query_calendar_events(country=US) = actual 2.2
- 8月 PCE 物价指数同比 +3.4%（前值 3.7%）: query_calendar_events(country=US) = actual 3.4
- 9月 ADP 就业 +9.0万: query_calendar_events(country=US) = actual 9.0
- 9月美国非农新增仅 2.9万（前值 16.2万）: 前次 theme_update 核证（记忆注入 2026-10-04）= 本轮未重新取数，沿用
- 美国 9月 CPI 同比（前值 3.4%）、核心 CPI（前值 2.4%）将于 2026-10-14 公布: query_calendar_events(country=US)
- FOMC 下次会议 2026-10-27/28: query_fomc(lookahead_days=120)

## 中国宏观

- 9月官方制造业 PMI 50.1、非制造业 PMI 50.2: query_indicators(category=pmi, country=china) = akshare 2026年09月
- 8月 CPI 同比 +0.8%、PPI 同比 +3.8%、能源分项 CPI +12.4%、食品 +4.8%: query_indicators(category=inflation, country=china) = akshare 2026年08月
- 9月 RatingDog 制造业 PMI 52.1（前值 51.5）: query_calendar_events(country=CN) = actual 52.1
- 9月 LPR 1Y=3.0%、5Y=3.5% 不变: query_calendar_events(country=CN)
- 中国 9月 CPI/PPI 将于 2026-10-14 公布: query_calendar_events(country=CN)

## 新闻事件（query_raw_items）

- 10/1 金龙中国指数收跌 1.03% 至 5637.25，逼近 2024/8/28 收盘位 5399.48，拼多多跌 1.85%: query_raw_items(keyword='拼多多', published_after='2026-09-10')[id:458570]
- 金龙指数 9月累跌 6.24%、Q3 累跌 2.59%，8/10 高点 6734.78 后持续走低: query_raw_items(keyword='拼多多', published_after='2026-09-10')[id:456562]
- 9/28 大盘（标普 -0.8%）中拼多多逆势涨 1.1%: query_raw_items(keyword='PDD OR Temu OR 拼多多', published_after='2026-09-20')[id:449400]
- 9/23 拼多多雄安公司员工突破 5000 人，3个多月完成全年招聘: query_raw_items(keyword='拼多多', published_after='2026-09-10')[id:438605][id:438469]
- 关税下 8月大促 Temu 欧盟订单下滑约一半，速卖通 Brand+ 逆势 +97%: query_raw_items(keyword='Temu', published_after='2026-08-20')[id:164108][id:162975]
- 法国通过超快时尚法罚款 SHEIN/Temu，2030 年每件罚款或达 €20: query_raw_items(keyword='Temu', published_after='2026-08-20')[id:231994][id:227818]
- Temu 上线自营品牌 BEMUVO，商标主体指向 PDD 关联公司: query_raw_items(keyword='Temu', published_after='2026-08-20')[id:310612]
- Temu Meta 广告投入最高 $962M，73% 合作创作者疑似假账号: query_raw_items(keyword='Temu', published_after='2026-08-20')[id:236620][id:208384]
- Shein 港股上市估值较峰值折损约 70%: query_raw_items(keyword='Temu', published_after='2026-08-20')[id:200649]
- PDD 8/27 跌 3.37%，分析师称营收增速降至约 3%，重资产转型执行风险为核心担忧: query_raw_items(keyword='Temu', published_after='2026-08-20')[id:172908]
- 9/30 上海网信办约谈 17 家平台（含拼多多），部署未成年人保护: query_raw_items(keyword='拼多多', published_after='2026-09-10')[id:454989]

## 沿用前次 session（2026-08-26 及更早，本轮未重新取数）

- FY2025 Revenue $60.53B、Net Income $13.71B、EPS $9.25、Operating CF $14.99B、FCF $12.00B、D/E 0.52: 前次 theme 数据来源节
- Q1 2026 Revenue $15.37B（miss -2.9%）、Net Income $1.82B（miss -43.2%）: 前次 theme 数据来源节
- Q2 2026 营收 1124亿元（miss 2.4%）、调整后 EPS 19.33元（beat 4.4%）、研发 43亿元（+40%）: query_raw_items[id:138951][id:138881]（前次 session）
- Temu 主管回撤做多多买菜（年营收或超 4000亿）: query_raw_items[id:139132]（前次 session）


# 数据来源（2026-10-04 session · lynch 接力第2棒）

## 行情复核（本轮重新抓取，与buffett轮一致）

- PDD 收盘价 $75.38（2026-10-02，-1.46%）、盘后 $75.52: fetch_url(finance.yahoo.com/quote/PDD/) = At close October 2
- PE(TTM) 8.12x、EPS(TTM) $9.28、市值 $107.296B、Beta(5Y) -0.01: fetch_url(finance.yahoo.com/quote/PDD/)
- 52周区间 $71.94–$139.41；距低点 = 75.38-71.94 = +$3.44（+4.8%）——修正前稿"仅3.4%"（系将美元差额误写为百分比）
- 1Y一致目标价 $114.60、财报预估日 2026-11-18: fetch_url(finance.yahoo.com/quote/PDD/)
- 10Y美债 5.28%、WTI $91.11、黄金 $4,162.30、VIX 15.31（10/2页面快照）: fetch_url(finance.yahoo.com/quote/PDD/)
- Yahoo新闻列表头条（2026-10-02后）: "PDD vs BABA/JD: Value Play or Trap at Its 52-Week Low?"（Insider Monkey, 2d ago）、"DBS cuts Sea target as Shopee spending weighs on profit growth"（Investing.com, 1d ago）: fetch_url(finance.yahoo.com/quote/PDD/)

## 新闻条目（本轮 lynch 亲自查询 query_raw_items）

- 9/16美联储宣布加息25bp、点阵图暗示今年还将加息，主席沃什发布会后指数收复部分失地；拼多多当日逆势+0.87%: query_raw_items(keyword='拼多多 OR Temu OR PDD', published_after='2026-09-15')[id:416622]
- 9/28标普500收跌0.8%当天拼多多逆势+1.1%: query_raw_items(keyword='拼多多 OR Temu OR PDD', published_after='2026-09-15')[id:449400]
- A股"拼多多概念"板块涨幅居前（9/22午评）: query_raw_items(keyword='拼多多 OR Temu OR PDD', published_after='2026-09-15')[id:433200]
- 金龙指数9月累跌6.24%（9/30收5696.06）、10/1收跌1.03%至5637.25逼近2024年8月低点: query_raw_items(keyword='拼多多 OR Temu OR PDD', published_after='2026-09-15')[id:456562][id:458570][id:453102]（本轮复核命中）

## 沿用 buffett/soros 轮引用（同 session，本轮未重新取数）

- Temu欧盟订单在关税下近乎腰斩、速卖通Brand+欧盟逆势+97%: query_raw_items[ id:164108]（buffett轮）
- Temu一二级主管回撤国内做多多买菜（年营收或超4000亿、利润超百亿）: query_raw_items[id:139132]（前轮session）
- 拼多多雄安公司员工突破5000人: query_raw_items[id:438605]（buffett轮）
- Temu上线自营品牌BEMUVO: query_raw_items[id:310612]（buffett轮）
- 法国反快时尚法、2030年每件罚款或达€20: query_raw_items[id:231994][id:227818]（buffett轮）
- Shein港股上市估值较峰值折损约70%: query_raw_items[id:200649]（buffett轮，本轮lynch复用）
- 上海网信办约谈17家平台含拼多多: query_raw_items[id:454989]（buffett轮）
- Temu Meta广告$9.62亿、73%合作创作者疑假账号: query_raw_items[id:236620]（buffett轮）
- 分析师称PDD营收增速降至约3%、重资产转型执行风险为核心担忧: query_raw_items[id:172908]（buffett轮引用，本轮lynch复用）
- 市场共识转向"10月按兵不动、12月或再加"（华泰）: query_raw_items[id:459349]（soros轮引用，本轮复用）；RSM[id:459341]、白宫CEA费兰[id:459257]同为soros轮引用
- Q2 GAAP净利润272亿元（-12% YoY）、Benchmark目标价$127→$114、Goldman $134、共识Hold: roundtable/discussion_log.md（buffett第1轮分析记录）
- 近八个季度六次营收miss、Q3三条件验证框架、证伪条件: roundtable/discussion_log.md（lynch第1轮分析记录）
- FY2025/Q1 2026财务、管理层电话会、中国宏观（PMI/CPI/PPI/LPR/社零）: 见本文件前两节（buffett轮与前次session归档）

## 工具失败记录（本轮）

- market_quote(PDD.US): OpenApiException 401003 token expired
- query_longbridge_by_route news/company(PDD.US): OpenApiException 401003 token expired（分析师预期/公司新闻以Yahoo及raw_items替代）

## 口径修正记录（本轮）

- "距52周低点3.4%"→修正为"+$3.44（+4.8%）"：原稿将美元差额误作百分比
- 预测时间线中"鲍威尔"→修正为"沃什"：[id:416622] 明确美联储主席为沃什（Warsh）

- 2026-10-04 审查轮（buffett）核证来源：
- PDD 10/1 盘中跌1.85%、金龙指数10/1收跌1.03%报5637.25点: query_raw_items(拼多多,2026-10-01)[id:458570] = 逼近2024年8月低点
- 金龙指数9月累跌6.24%、Q3累跌2.59%: query_raw_items(拼多多,2026-10-01)[id:456562] = 收涨0.60%报5696.06点
- 9/28标普-0.8%普跌日拼多多逆势+1.1%: query_raw_items(拼多多,2026-09-28)[id:449400] = 标普初步收跌0.8%，拼多多涨1.1%
- 9/16美联储宣布加息、点阵图暗示年内还将加息，主席沃什发布会后收复部分失地；拼多多当日+0.87%: query_raw_items(美联储,2026-09-16)[id:416622] = 金龙指数收跌0.55%报5734.17点
- 9/17有快讯误写"美联储宣布降息"，与[id:416622]及加息周期报道矛盾（单一来源笔误）: query_raw_items(拼多多,2026-09-17)[id:423939] = 脱离9/16所创收盘最低位5734.17点
- 白宫CEA主席费兰：美联储9月份加息缺乏合理性，通胀回落速度足够快: query_raw_items(美联储,2026-10-02)[id:459257] = 政府公开质疑9月加息
- 华泰：9月非农不及预期，美联储难以10月连续加息，基准情形12月再加息（3个月均值+5.1万）: query_raw_items(美联储,2026-10-03)[id:459349] = 支撑10月pause判断
- RBC将美联储加息预期推迟至12月与3月隔次加息: query_raw_items(美联储,2026-10-02)[id:459027] = 终端利率定价高于2-2.8次合理区间
- 现货黄金10/2跌近1%至4137.85美元/盎司: query_raw_items(美联储,2026-10-02)[id:458961] = 文中$4,162或为更早时点
- 鲍威尔为"前美联储主席"（现任为沃什）: query_raw_items(美联储,2026-10-02)[id:459261] = 司法部不重启对鲍威尔刑事调查
- 上海市委网信办约谈17家平台含拼多多（9/30）: query_raw_items(拼多多,2026-09-30)[id:454989] = 涉未成年人保护专项行动
- 拼多多雄安公司员工突破5000人（9/23）: query_raw_items(拼多多,2026-09-23)[id:438605] = 3个多月完成全年招聘
- 9/22午评A股"拼多多概念"板块涨幅居前: query_raw_items(拼多多,2026-09-22)[id:433200] = 文化传媒、拼多多概念、生物制品领涨
- 9/15拼多多关联公司上海寻梦因虚假广告被罚54万元、年内多次被罚: query_raw_items(拼多多,2026-09-15)[id:389157] = 审查发现，稿件未覆盖（金额不重大）
- 中国9月制造业PMI 50.1、非制造业PMI 50.2: query_indicators(pmi,china,7d) = akshare 2026年09月份
- 中国8月CPI同比+0.8%、PPI同比+3.8%: query_indicators(inflation,china,7d) = akshare 2026年08月份
- 中国8月能源类商品价格同比+12.4%、农产品+4.8%: query_indicators(inflation,china,7d) = akshare 2026年08月份
- FOMC 9/15-9/16会议已决议（含SEP/发布会），下次会议2026-10-27/28，12/8-9：query_fomc(lookback=60,lookahead=120) = 官方日历，决议文本未入库
- 长桥行情/新闻路由 token 过期（401003）: market_quote(PDD.US)+news/company 均失败，PDD报价/一致预期无法独立核验


# 数据来源（2026-10-04 session · soros 交叉审查）

## 独立核验（D82，审查人亲自查询）
- 30天窗口 PDD/拼多多/Temu 重大新闻全量复核（最新条目止于10/1，无遗漏重大事件）: query_raw_items(keyword='拼多多 OR PDD OR Temu', published_after='2026-09-04', limit=50) = 50条，管理层变动/监管裁决/财报/股价异动均已覆盖
- 10/1后增量新闻复核（无新增公司层面事件）: query_raw_items(keyword='PDD OR 拼多多 OR Temu', published_after='2026-10-01', limit=20) = 最新为[id:458570]
- 中国8月 CPI同比 +0.8%、PPI同比 +3.8%、能源分项 +12.4%、食品 +4.8%（复核草稿"成本推升型"定性成立）: query_indicators(category=inflation, country=china) = akshare 2026年08月
- FOMC 9/15-16 会议有决议/声明/SEP点阵图；下次会议 2026-10-27/28（与草稿预测表一致）: query_fomc(lookback_days=60, lookahead_days=60)
- 金龙指数 9/23 -1.43%报5763.01（PDD同日-1.43%）、9/28 +1.12%报5751.39（PDD +1.19%）、9/29 -1.55%报5662.29（PDD -1.26%）、9/30 +0.60%报5696.06（PDD +0.57%）、10/1 -1.03%报5637.25（PDD -1.85%）: query_raw_items[same queries][id:439799][id:449526][id:453102][id:456562][id:458570]
- 9/16加息日PDD +0.87%（金龙同日-0.55%，确为独立逆势）: query_raw_items[same][id:416622]
- 9/17金龙快讯文本含"美联储宣布降息"表述，与[id:416622]矛盾，系源文本笔误（草稿采信"加息"正确）: query_raw_items[same][id:423939]
- Binance 8/28上线PDD永续合约（20x杠杆）（草稿未提，次要）: query_raw_items(keyword='Temu', published_after='2026-08-20')[id:178509]
- 嘉友时代2026半年报：Temu收入显著收缩（供应商侧第二信源，草稿未提，可选补充）: query_raw_items(keyword='Temu', published_after='2026-08-20')[id:165695]
- 距52周低点复算：75.38-71.94=+$3.44，3.44/71.94=+4.8%（草稿修正正确）: 本人算术复核
- PMI前值口径矛盾记录：草稿共识#4写"前值49.2"，reference.md写前值49.8（预期50.1）；49.2系7月值——审查意见：前值应为49.8
- 长桥 token 过期独立复现（401003）: query_longbridge_by_route(news/company, PDD.US) = OpenApiException 401003（与草稿披露一致，非草稿错误）


# 数据来源（2026-10-04 session · 审查人 lynch 独立核验）

## 独立核验通过（与草稿一致）
- 美联储主席为凯文·沃什（非鲍威尔）: query_raw_items(keyword='沃什')[id:457481][id:458135][id:456341][id:459261] = 特朗普"不怪凯文（凯文沃什，美联储主席）"；卡什卡利"美联储主席沃什将采取行动抑制通胀"；鲍威尔已称"前美联储主席"
- FOMC 9/15-16会议存在、声明URL monetary20260916a.htm、下次会议10/27-28: query_fomc(lookahead_days=120, lookback_days=120) = federalreserve.gov
- 多多买菜今年营收有望超4000亿元、创造上百亿元利润，多位Temu一二级主管转回国内: query_raw_items(keyword='多多买菜')[id:139132] = 晚点LatePost 2026-08-24
- 法国反快时尚法2030年每件罚款或近€20: query_raw_items(keyword='Temu')[id:231994] = bbc_world 2026-09-01
- 法国通过超快时尚法对Shein/Temu罚款: query_raw_items(keyword='Temu')[id:227818] = 2026-09-01
- Temu自营品牌BEMUVO、商标主体指向PDD关联公司: query_raw_items(keyword='Temu')[id:310612] = 2026-09-08
- Temu Meta广告最高$9.62亿、73%合作创作者疑假账号: query_raw_items(keyword='Temu')[id:236620][id:208384] = Fortune/longbridge 2026-08-31~09-02
- Shein港股上市估值较峰值折损70%: query_raw_items(keyword='Temu')[id:200649] = 2026-08-31
- 拼多多雄安公司员工突破5000人、3个多月完成全年招聘: query_raw_items(keyword='拼多多 OR PDD OR Temu')[id:438605][id:438469] = 2026-09-23
- 上海市委网信办召集17家平台（含拼多多）部署未成年人保护: query_raw_items(...)[id:454989] = 2026-09-30
- 金龙指数9月累跌6.24%、Q3累跌2.59%、8/10高点6734.78后走低: query_raw_items(...)[id:456562] = 2026-10-01
- 金龙指数10/1收跌1.03%报5637.25、拼多多跌1.85%、逼近2024/8低点: query_raw_items(...)[id:458570] = 2026-10-01
- 金龙指数9/29收跌1.55%报5662.29、拼多多跌1.26%: query_raw_items(...)[id:453102] = 2026-09-29
- 9/28标普500初步收跌0.8%、拼多多涨1.1%（金龙同日收涨1.12%、拼多多涨1.19%）: query_raw_items(...)[id:449400][id:449526] = 2026-09-28
- 华泰：美联储难以10月连续加息、基准情形12月再次加息、3个月均值非农5.1万: query_raw_items(keyword='美联储')[id:459349] = 2026-10-03
- RSM布鲁苏埃拉斯：维持10月不加息、12月加息判断: query_raw_items(...)[id:459341] = 2026-10-03
- 白宫CEA主席费兰：9月加息缺乏合理性、通胀回落足够快: query_raw_items(...)[id:459257] = 2026-10-02
- TD证券预计12月与3月加息；RBC推迟加息周期至12月与3月隔次加息: query_raw_items(...)[id:458943][id:459027] = 2026-10-02
- 美联储会议纪要下周公布、10月加息门槛很高: query_raw_items(...)[id:459561] = 2026-10-03
- 卡什卡利：可能需超出市场预期的加息、9月预测今年再加一次2027年再加一次: query_raw_items(keyword='沃什')[id:458148] = 2026-10-01
- 古尔斯比：10月加息或暂停均有充分理由: query_raw_items(...)[id:459149] = 2026-10-02
- PDD 8/27跌3.37%、分析师称营收增速降至约3%、重资产转型执行风险为核心担忧: query_raw_items(keyword='Temu')[id:172908] = 2026-08-28
- 9/16 FOMC当日金龙收跌0.5%呈V形反弹、PDD逆势上涨: query_raw_items(keyword='PDD')[id:416214] = 2026-09-17
- Temu与罗马尼亚邮政Poșta Română签物流MoU: query_raw_items(keyword='Temu')[id:242855] = 2026-09-02
- Temu与塞浦路斯CITEA签MoU: query_raw_items(keyword='Temu')[id:411788] = 2026-09-16
- 9月中国官方制造业PMI 50.1、非制造业PMI 50.2: query_indicators(category=pmi, country=china) = akshare 2026年09月
- 8月中国CPI同比+0.8%、PPI同比+3.8%、能源分项+12.45%、农业分项+4.80%、CPI环比+0.4%: query_indicators(category=inflation, country=china) = akshare 2026年08月
- 8月CPI同比实际+0.8%（前值+0.5%，9/9发布）: query_calendar_events(country=CN, lookback_days=30) = actual 0.8
- 9月1Y/5Y LPR实际值维持3.0%/3.5%: query_calendar_events(country=CN, lookback_days=30) = actual 3.0/3.5
- 长桥token过期（审查人复验属实）: query_longbridge_by_route('news/company', PDD.US) 与 market_quote(['PDD.US']) 均 OpenApiException code=401003

## 审查中新发现（草稿未覆盖，见审查意见）
- PDD平台白酒专营店被罚688.78万元、"低价冲量模式面临挑战": query_raw_items(keyword='PDD')[id:395890] = 2026-09-15
- PDD关联公司上海寻梦信息因虚假广告被罚54万元: query_raw_items(keyword='PDD')[id:389540] = 2026-09-15
- 在岸、离岸人民币兑美元升破6.7: query_raw_items(keyword='拼多多 OR PDD OR Temu')[id:429288] = 2026-09-20（草稿宏观章节无FX维度）
