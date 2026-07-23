# Workflow Template

## Metadata
- Workflow Name:
- Owner:
- Version: 1.0.0
- Trigger:
- Status: Draft

## Purpose
定義可重複、可驗證、可交接的工作流程。

## Inputs
- 啟動條件：
- 輸入資料：
- 角色與權限：
- 使用工具：

## Outputs
- 主要交付物：
- 日誌：
- 品質報告：

## Required Sections
1. Trigger
2. Input Validation
3. Processing Steps
4. Review Gate
5. Output Delivery
6. Logging and Archive

## Optional Sections
- 人工核准
- 失敗重試
- 回滾程序
- 通知機制

## Validation Rules
- 每一步皆有輸入、動作、輸出與責任人。
- 失敗條件與停止條件明確。
- 涉及品牌產出時引用 `../docs/` 與 `../quality/`。

## Example
```text
需求輸入 → 品牌資料檢查 → 內容生成 → 視覺生成 → 品質閘門 → 人工核准 → 發布
```
