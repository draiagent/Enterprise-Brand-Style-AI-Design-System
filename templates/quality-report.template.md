# Quality Report Template

## Metadata
- Report ID:
- Asset or Project:
- Reviewer:
- Version: 1.0.0
- Review Date:
- Result: Pass / Conditional Pass / Fail

## Purpose
記錄品牌、內容、視覺、技術與治理檢查結果，作為核准、修訂與發布依據。

## Inputs
- 待檢查產出：
- 對應規範：
- 測試工具：
- 風險等級：

## Outputs
- 檢查結果
- 缺陷清單
- 修正責任與期限
- 最終核准紀錄

## Required Sections
1. Scope
2. Criteria
3. Findings
4. Severity
5. Required Actions
6. Evidence
7. Final Decision

## Optional Sections
- 自動測試輸出
- 前後版本比較
- 例外核准

## Validation Rules
- 每項缺陷必須指出位置、規則與修正方式。
- 嚴重度使用 Critical、High、Medium、Low。
- Critical 或 High 未關閉前不得發布。
- 引用 `../quality/` 與相關 `../docs/` 文件。

## Example
```yaml
result: Conditional Pass
critical: 0
high: 0
medium: 2
release_allowed: true after fixes
```
