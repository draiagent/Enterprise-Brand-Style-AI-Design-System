# Dashboard Template

## Metadata
- Dashboard Name:
- Owner:
- Version: 1.0.0
- Audience:
- Refresh Frequency:

## Purpose
建立可監控、可判讀、可追蹤行動的企業儀表板。

## Inputs
- 決策問題：
- KPI 與公式：
- 資料來源：
- 更新頻率：
- 權限：

## Outputs
- 儀表板頁面
- KPI 字典
- 異常與行動規則

## Required Sections
1. Summary KPIs
2. Trend Analysis
3. Breakdown
4. Alerts and Exceptions
5. Recommended Actions
6. Data Freshness

## Optional Sections
- 篩選器
- 目標比較
- 預測區間
- 明細表

## Validation Rules
- KPI 名稱、定義、單位與期間一致。
- 顏色不可作為唯一辨識方式。
- 預設畫面先回答最重要的決策問題。
- 遵循 `../docs/11-dashboard-design-standard.md` 與無障礙規範。

## Example
```yaml
primary_kpi: AI 導入任務完成率
comparison: 本期 vs 上期
action_threshold: below 80 percent
```
