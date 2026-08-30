# 数据溯源 — fed 主题更新（2026-08-30_0955__manual__theme_update）

## soros relay 新增 / 核验来源

- 7月实际个人消费支出环比 0.0%: query_calendar_events(country=US, importance=high,medium, lookback_days=7)[2026-08-26 实际个人消费支出环比] = 0.0%（前值 0.4%）
- 7月扣除飞机非国防资本耐用品订单环比 +0.2%: query_calendar_events(2026-08-26)[扣除飞机非国防资本耐用品订单环比初值] = 0.2%（前值 1.2%）
- 8月22日当周贸易逆差 -118.8: query_calendar_events(2026-08-27)[US Adv Goods Trade Balance] = -118.8（前值 -101.41）
- 6月S&P/CS20房价同比 2.1% / 环比 0.24%: query_calendar_events(2026-08-25)[S&P Case-Shiller Composite-20] = 2.1% / 0.24%（前值 1.6% / 0.15%）
- 2年期国债拍卖 high yield 4.204: query_calendar_events(2026-08-25)[2 Year Official Auction] = 4.204%（前值 4.315）
- 2Y–30Y利差收窄 >9bp: query_raw_items(keyword='Walsh OR Warsh OR Treasury')[id:189435] = "After Walsh struck a hawkish tone at the Jackson Hole meeting... spread between 2-year and 30-year Treasury yields to narrow by more than 9 basis points"
- 加密市场24h爆仓4.81亿美元(多头3.6亿) + 9月加息概率35.4%→55.7%: query_raw_items(keyword='加息 OR Warsh')[id:190956] = "CME FedWatch 数据显示，9月加息概率由前一日的35.4%升至55.7%...过去24小时全市场爆仓约4.81亿美元，其中多头爆仓超过3.6亿美元"
- 9月加息概率30%→50% + 非农CPI最后裁判: query_raw_items(keyword='沃什 OR 加息')[id:191226] = "美联储加息25个基点的概率从30%跃升至约50%...非农与CPI成最后裁判"
- Warsh被误标为Waller(系统性): query_raw_items(keyword='Waller OR Warsh')[id:191916][id:191451][id:191397][id:189797] = 多条longbridge标题将"Federal Reserve Chairman Waller/Walsh"误作主席释放鹰派信号，实际主席为Kevin Warsh

## 既有来源（前稿沿用）

- 目标区间 3.50–3.75%: query_fomc（FRED DFEDTARU/DFEDTARL，2026-07-28）
- 资产负债表 6.731 万亿: query_indicators（openbb，2026-08-26）
- 7月PCE 3.7% / 核心PCE 3.34%: query_calendar_events（2026-08-26）
- Q2 GDP平减 6.4% / 核心PCE 3.6% / 实际GDP 1.5%: query_calendar_events（2026-08-26）
- 8月芝加哥PMI 47.1 / 谘商会信心 89.4: query_calendar_events（2026-08-28 / 08-25）
- 30年收益率 5.311% / 10年 4.724%: query_calendar_events（2026-08-17）
- CME FedWatch 9月 59.9%/40.1%/0.0%: FactPack 锚点（2026-08-26）
- 9月加息概率 35%→60%: query_raw_items[id:192438]
- 沃什"迟到的鹰派、信誉修复": query_raw_items[id:191189]
- Anna Wong非农或负警告: query_raw_items[id:191814]（P1）
- 12月加息概率近90%: query_raw_items[id:191377]
- 高通/iPhone涨价、财政回购翻倍: query_calendar_events（2026-08-28 / 09-07）
