# Release Note Template

## Metadata
- Release Version:
- Release Date:
- Owner:
- Status: Draft / Released
- Compatibility:

## Purpose
以一致格式記錄版本內容、相容性、升級方式與已知限制。

## Inputs
- 版本範圍：
- Commit 或 PR：
- 新增功能：
- 修正項目：
- 破壞性變更：
- 遷移需求：

## Outputs
- Release Note
- Upgrade Guide
- Known Issues
- Verification Record

## Required Sections
1. Summary
2. Added
3. Changed
4. Fixed
5. Deprecated
6. Removed
7. Security
8. Upgrade Instructions
9. Known Issues

## Optional Sections
- Contributors
- Screenshots
- Rollback Instructions

## Validation Rules
- 版本遵循語意化版本規則。
- 與 `VERSION`、`CHANGELOG.md`、Git Tag 一致。
- 破壞性變更與遷移程序必須清楚標示。
- 安全修正不得揭露可被濫用的敏感細節。

## Example
```markdown
# v1.1.0

## Added
- 新增企業海報與儀表板模板。

## Upgrade Instructions
- 拉取最新版並重新執行品質驗證。
```
