# reference.md — 周度财经日历预读 · 目标周 2026-11-09 ~ 2026-11-15（数据溯源）

## 行情快照
- 10Y UST 收益率（11-13 收）: query_indicators(country=us, category 空) = 5.15%（openbb yield_10y）
- 2Y UST 收益率（11-13 收）: query_indicators(country=us, category 空) = 4.88%（openbb yield_2y）
- 2Y 周内变动: query_raw_items(keyword=CPI)[id:768585] = 周内累计 +20bp
- 10Y 盘中（11-12）: query_raw_items(keyword=美债)[id:767626] = 约 5.00%
- 10Y（11-13 PPI 后）: query_raw_items(keyword=黄金)[id:774806] = 5.144%
- 2s10s（11-16）: query_indicators(country=us) = +0.29（openbb）
- VIX（11-13）: query_indicators(country=us) = 19.3
- 美国高收益利差（11-13）: query_indicators(country=us) = 3.23%
- 美国初请（指标库 11-13 数据日）: query_indicators(country=us) = 200,000 人
- 企业-国债利差（11-13）: query_indicators(country=us) = 0.89（corporate_spread）
- 美元指数（指标库，11-13）: query_indicators(country=us) = 122.65 ⚠️与新闻口径冲突，不用于判断
- DXY（11-13 ICE 尾盘、周涨）: query_raw_items(published_after=2026-11-09, keyword=美元指数)[id:777926] = 103.423，本周累涨 1.10%
- DXY 周区间与 19 个月新高: query_raw_items(keyword=美元指数)[id:774215] = 101.488~103.425
- S&P 500 周收盘: query_raw_items(keyword=标普)[id:778790] = 7561.67，本周 +2.51%（道指 +2.07%、纳指 +2.27%）
- Brent（11-14 暗盘）: query_raw_items(keyword=布伦特)[id:780112] = 跌破 93 美元/桶
- Brent 周初（11-08 收）: 上期复盘口径（themes/2026-11-02__2026-11-08/recap） = 98.32 美元/桶
- Brent（11-12 特朗普言论日）: query_raw_items(keyword=布伦特)[id:768407] = 盘中涨近 4%（同条含英伟达黄仁勋辞任消息）
- Gold（11-15）: query_raw_items(keyword=黄金)[id:781395] = 现货突破 3,900 美元/盎司，日内 +0.52%
- Gold（11-13 PPI 后）: query_raw_items(keyword=黄金)[id:774806] = 3,894.95 美元/盎司
- Gold（11-12 盘中）: query_raw_items(keyword=布伦特)[id:768407] = 跌破 3,900、盘中 -3%
- USDCNH（11-13 纽约尾盘）: query_raw_items(keyword=离岸人民币)[id:778823] = 6.6749
- SPDR 黄金持仓（11-13）: 前两棒 query_raw_items / 指标库 = 1,044.41 吨，单日 +3.71 吨
- 比特币（11-15）: query_raw_items(keyword=比特币)[id:781358] = 跌破 7 万美元

## 目标周事件实际值（query_calendar_events(days=14, lookback_days=9~10, importance=high,medium)）
- 美国 10 月 CPI 实际: query_calendar_events(lookback_days=9) = 总体环比 0.4%（预期 0.3、前值 0.6）、核心环比 0.3%（预期 0.2、前值 0.3）；新闻交叉 query_raw_items(keyword=CPI)[id:768585]
- 美国 10 月 PPI 实际: query_calendar_events(lookback_days=9) = 同比 6.5%（预期 6.6、前值 6.3，四年新高）、环比 +0.3%（预期 0.4）、核心同比 5.0%、核心环比 +0.3%
- 美国 11-07 当周初请: query_calendar_events(lookback_days=9) = 20.0 万人（预期 19.4、前值 18.9）；续请 169.7 万
- 美国 10 月成屋销售: query_calendar_events(lookback_days=9) = 375 万户（预期 385、前值 399），环比 -5.5%，30 年按揭利率 7.21%
- 美国 10 月联邦预算: query_calendar_events(lookback_days=9) = 赤字 4,040.64 亿美元（预期 -3,175 亿、前值 -2,843 亿）
- 中国 10 月通胀: query_calendar_events(lookback_days=9) = CPI 同比 0.7%（预期 0.8、前值 0.9）、PPI 同比 5.7%（预期 5.3、前值 5.0）
- 中国 10 月贸易帐: query_calendar_events(lookback_days=9) = 出口 +35.2%（美元计价）、进口 +41.6%、顺差 1,052.8 亿美元
- 中国 10 月金融数据: query_calendar_events(lookback_days=9) = M2 7.1%（预期 7.2）、社融 286,100 亿元、新增贷款 114,200 亿元、10 月单月贷款 -1,000 亿元、M2-M1 剪刀差 4.0→2.7pct
- 日本 10 月 CGPI: query_calendar_events(lookback_days=9) = 同比 7.1%（前值 6.8、预期 6.5）、环比 0.7%
- 日本三季度 GDP: query_calendar_events(lookback_days=9) + query_raw_items(keyword=日本GDP)[id:781387][id:781400] = 季环比 0.0%（预期 0.1、前值 0.4）、年化 -0.1%、私人消费 -0.3%、资本开支 +1.6%、净出口贡献 -0.6pp、平减指数 2.4%
- 英国三季度 GDP: query_calendar_events(lookback_days=9) = 季环比前值 0.5%、同比前值 1.4%（共识 0.7%/1.9%）
- 美债 30Y 拍卖中标: 前两棒 query_calendar_events / 讨论记录 = 5.441%（另有 2.36%/2.54% 冲突序列，见 §11）

## 货币政策与定价
- 12 月加息定价: query_raw_items(keyword=FedWatch)[id:781254] = 25bp 概率 95%、50bp 概率 5%（CME FedWatch，11-13/14 口径）
- 美联储利率状态: query_raw_items[id:781339] + 历史记忆（2026-11-16 标注） = 主席凯文·沃什、基准利率 3.75%-4.00%、10-28 决议维持（Cook/Hammack 两票要求加息）
- 施密德讲话: query_raw_items(keyword=美联储讲话)[id:781177][id:781136] = 「通胀仍过高、当前利率并不具限制性」
- 沃勒「大幅加息」的市场解读: query_raw_items(keyword=美联储)[id:781220] = 摩根大通资管称市场把沃勒当作少数派
- 50bp 讨论传闻: query_raw_items(keyword=美联储)[id:781254] 相关条目 = 12 月更大幅度加息概率 5%

## 日历外重大事件
- 黄仁勋辞任英伟达 CEO: query_raw_items(keyword=英伟达)[id:768407][id:781358] = 11-12 辞任、CFO 代任、启动 CEO 遴选、面对司法部反垄断调查、贝森特称需「重大重组」、复职传闻
- 英伟达周跌幅: query_raw_items(keyword=英伟达)[id:781462] = 周跌 13%、市值蒸发超 5,700 亿美元
- 联储金融稳定报告 AI 警示: query_raw_items(keyword=标普)[id:778700] = 11-13 发布，警示 AI 推升资产估值过高
- 中东航母部署: query_raw_items(keyword=中东)[id:781396] = 罗斯福号 11-15 进入 CENTCOM 责任区
- 韩国央行加息预测: query_raw_items(keyword=韩国)[id:781366] = 摩根士丹利预测 11 月与 2 月各加息 25bp 至 3.5%
- 印度资金回补: query_raw_items(keyword=印度)[id:780378] = AI 交易退潮与油价回落下获资金回补
- 微软服务中断扰动大宗商品定价: query_raw_items(keyword=微软)[id:778765] = 11-13 普氏 22 项生物燃料价格暂停发布
- FAA 全美地面停飞: query_raw_items(keyword=停飞)[id:778727] = 11-13

## 前瞻事件（报告时点 2026-11-17 之后，query_calendar_events(days=6, lookback_days=2, importance=high,medium)）
- 11-16 纽约联储制造业指数: query_calendar_events(days=6, lookback_days=2) = 实际 7.8（前值 25.5、预期 18.0）
- 11-16 中国 10 月宏观: query_calendar_events(days=6, lookback_days=2) = 社零 +0.4%（前值 1.1%、预期 0.8%）、固投累计 -8.1%、地产开发投资 -21.6%（前值 -20.6%）、工业增加值 +4.8%（前值 5.5%）、城镇失业率 5.1%、70 城新房同比 -2.4%
- 11-16 美股 13F: query_calendar_events(days=6, lookback_days=2) = 伯克希尔、桥水、城堡投资等 Q3 持仓集中公布
- 11-17 美国 10 月零售销售: query_calendar_events(days=6, lookback_days=2) = 环比预期 +0.1%、前值 +0.8%
- 11-18 FOMC 纪要: query_calendar_events(days=6, lookback_days=2) = 19:00 UTC 公布
- 11-19 当周初请: query_calendar_events(days=6, lookback_days=2) = 预期 19.7 万、前值 20.0 万
- 11-20 LPR: query_calendar_events(days=6, lookback_days=2) = 1 年期前值 3.0%、5 年期前值 3.5%
- 11-16 中国 MLF 与 70 城房价: query_calendar_events(days=6, lookback_days=2) = 10 月 70 城新房同比 -2.4%（前值 -2.8%）

- 英伟达财报电话会要点（董事会确认黄仁勋不回归、FY2028指引+75%至1300亿美元、盘后+5%）: query_raw_items(keyword=英伟达 OR 黄仁勋 OR NVIDIA, published_after=2026-11-01)[id:791445][id:791473][id:791481] = 黄仁勋离职后首份财报，指引超预期，盘后涨5%
- 黄仁勋11-17声明愿回归但董事会主席称无计划: query_raw_items(keyword=英伟达 OR 黄仁勋 OR NVIDIA)[id:791488][id:791443] = 黄仁勋承认个人错误并愿回归，董事会明确不会重新任命
- 英伟达评估商务部本周新出口管制（新马出口或减收入至多10%）: query_raw_items(keyword=英伟达 OR 黄仁勋 OR NVIDIA)[id:791499] = 临时CEO克雷斯称仍在评估新出口管制影响
- 威廉姆斯11-17表态通胀顽固但无需激进加息: query_raw_items(keyword=美联储 OR CPI OR 加息 OR FedWatch, published_after=2026-11-14)[id:790987][id:791489] = 纽约联储主席称不认为需要采取激烈行动
- CME FedWatch 12月加息25bp概率96.8%、50bp概率3.2%（11-17）: query_raw_items(keyword=美联储 OR CPI OR 加息 OR FedWatch)[id:791324] = 金十援引CME美联储观察

- 美国10月非农就业+16.5万/失业率4.1%/时薪环比+0.4%（11-06发布）: query_calendar_events(days=3, lookback_days=12, importance=high,medium, limit=200) = 预期6.5万/4.2%/+0.3%，实际16.5万/4.1%/+0.4%，大幅超预期
- 美国11月密歇根消费者信心初值（11-06）: query_calendar_events(days=3, lookback_days=12, importance=high,medium, limit=200) = 预期48.0，实际51.0
- 美国10月CPI环比双序列冲突: query_calendar_events(days=3, lookback_days=12, importance=high,medium, limit=200) = 序列A 0.4（前值0.6/预期0.3）与序列B 0.17（前值0.59）并存
- 中国10月贸易帐（美元计价）: query_calendar_events(days=3, lookback_days=12, importance=high,medium, limit=200) = 前值133.53、预测125.8、实际105.28（单位：十亿美元）
- 美国10Y/3Y国债拍卖实际: query_calendar_events(days=3, lookback_days=12, importance=high,medium, limit=200) = 10Y high yield 5.02（前值5.3）/official 2.46（前值2.77）；3Y 4.627（前值4.932）
- 俄美乌三方会谈11-10~11阿布扎比、G7外长会议11-09~10巴黎: query_calendar_events(days=3, lookback_days=12, importance=high,medium, limit=200) = 两场地缘事件均在目标周内、草稿未覆盖
- 日本央行10月审议委员意见摘要（11-09）: query_calendar_events(days=3, lookback_days=12, importance=high,medium, limit=200) = 高重要性日程事件
- NVIDIA财报盘后+5%、销售指引超预期（11-17）: query_raw_items(published_after=2026-11-05T00:00:00Z)[id:791481] = 财报电话会后盘后涨5%，NQ期货亚太盘初+1.9%
- 黄仁勋11-17声明承认个人错误并愿接受复任CEO安排: query_raw_items(published_after=2026-11-05T00:00:00Z)[id:791488] = 声明承诺配合董事会独立调查
- 纽约联储主席Williams（11-17）: query_raw_items(published_after=2026-11-05T00:00:00Z)[id:791489] = 通胀仍须降温但不需要大幅升息
- 英伟达评估美国商务部本周新出口管制（11-17）: query_raw_items(published_after=2026-11-05T00:00:00Z)[id:791499] = 分析师估计新马出口限制或影响英伟达收入最多10%
- 美银Cabana：2Y美债年底或达5%（11-17）: query_raw_items(published_after=2026-11-05T00:00:00Z)[id:791501] = 短端利率未抑制经济则继续上升