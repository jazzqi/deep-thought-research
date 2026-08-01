# 数据来源记录 — PDD Holdings Theme Update

## 宏观指标（通过 query_indicators 验证）

- 社会消费品零售总额同比增速 1.0%（2026年06月）: query_indicators(category='macro', country='china', time_range='7d', limit=15) = retail_sales_yoy: 1.0
- 消费者信心指数 89.4（2026年06月）: query_indicators(category='macro', country='china', time_range='7d', limit=15) = consumer_confidence: 89.4
- 制造业PMI 49.2（2026年07月）: query_indicators(category='macro', country='china', time_range='7d', limit=15) = manufacturing_pmi: 49.2
- 非制造业PMI 49.0（2026年07月）: query_indicators(category='macro', country='china', time_range='7d', limit=15) = non_manufacturing_pmi: 49.0
- GDP同比 4.7%（2026年第1-2季度）: query_indicators(category='macro', country='china', time_range='7d', limit=15) = gdp_quarterly: 4.7

## 新闻搜索

- PDD相关新闻: query_raw_items(limit=30, source='PDD', status='processed') = 无结果
- 综合新闻搜索: query_raw_items(limit=50, source=None, status='pending') = 50条结果中无PDD相关

## 数据缺失声明

以下数据在当前工具中无法获取，未编入分析：
- PDD 市值、股价、P/E、P/B 等估值数据
- PDD 现金及等价物精确数字
- Temu 季度运营亏损规模
- PDD 最新季度营收/净利润
- 美国/中国汇率数据（query_indicators 返回 None）
