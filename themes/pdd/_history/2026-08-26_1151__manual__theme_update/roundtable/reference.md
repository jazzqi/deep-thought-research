# Reference — buffett 审查核验数据源

## Q2 2026 财报实际值（2026-08-24 发布）
- Q2 2026 营收 ¥1,124 亿 vs 预期 ¥1,152 亿（Miss -2.4%）: query_raw_items(keyword="PDD 拼多多", source="telegram:Financial_Express")[id:138363]
- Q2 2026 调整后每 ADS 收益 ¥19.33 vs 预期 ¥18.51（Beat +4.4%）: query_raw_items(keyword="PDD 拼多多", source="telegram:Financial_Express")[id:138363]
- Q2 2026 交易服务收入同比 +13%: query_raw_items(keyword="PDD 拼多多", source="telegram:Financial_Express")[id:138951]
- Q2 2026 研发投入 ¥43 亿，同比 +40%: query_raw_items(keyword="PDD 拼多多", source="telegram:Financial_Express")[id:138470]
- Q2 2026 股价反应：盘前 -5%，收盘 +2.6%: query_raw_items(keyword="PDD 拼多多", source="telegram:Financial_Express")[id:138362][id:138965]

## Q2 2026 管理层指引/电话会（2026-08-24/25）
- 陈磊：欧盟关税变化短期内将对跨境业务产生重大影响: query_raw_items(keyword="拼多多 陈磊", source="telegram:Financial_Express")[id:138746]
- 管理层确认短期跨境订单面临更低效率和更高成本: query_raw_items(keyword="拼多多 PDD", source="telegram:Financial_Express")[id:138755]
- 陈磊：不会因短期波动改变全球化业务长期方向: query_raw_items(keyword="拼多多 陈磊", source="telegram:Financial_Express")[id:139976]
- 赵佳臻谈自营业务：启动所需时间比预期更长: query_raw_items(keyword="拼多多 赵佳臻", source="telegram:Financial_Express")[id:139983]
- 赵佳臻：推动平台生态治理常态化，6 月落地 50+ 细分领域方案: query_raw_items(keyword="拼多多 赵佳臻", source="telegram:Financial_Express")[id:138725]

## 战略/竞争事件（2026-08-24/25）
- 多位 Temu L1/L2 主管转回国内做多多买菜；多多买菜年营收有望超 ¥4000 亿、利润 ¥100+ 亿: query_raw_items(keyword="拼多多 Temu 多多买菜", source="telegram:Financial_Express")[id:139132]
- 速卖通登顶巴西购物榜，超越 Temu/亚马逊/美客多，8 月首日销售环比 +85%: query_raw_items(keyword="速卖通 Temu 巴西", source="telegram:Financial_Express")[id:140665]

## 中国宏观数据
- 注：query_indicators(category=macro, country=china) 返回数据仅进出口（2026-04-01，已过时 147 天），无法验证 index.md 中引用的 GDP/PMI/零售数据。index.md 中的宏观数据来源追溯至 2026-08-01 session，当前 session 未独立获取最新值。
