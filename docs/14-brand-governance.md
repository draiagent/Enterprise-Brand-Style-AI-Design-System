# 14 — Brand Governance

## Purpose
建立品牌規範的角色、權限、核准、版本、例外與稽核機制。

## Scope
適用於所有品牌資產、Token、元件、Prompt、模板、輸出物及外部合作內容。

## Principles
品牌治理需可追蹤、可核准、可回滾；AI 產出不因自動化而免除責任。

## Roles
- **Owner**：核定品牌方向與重大變更。
- **Maintainer**：維護文件、Token、元件與版本。
- **Contributor**：依規範提交變更。
- **Reviewer**：執行品牌、技術、內容與無障礙審查。
- **Approver**：對正式發布承擔最終核准責任。

## Change Classes
- Patch：錯字、連結與不影響行為的修正。
- Minor：新增相容 Token、元件、模板或規範。
- Major：品牌識別、命名、資料契約或不相容規則變更。

## Rules
- 正式資產必須有來源、擁有者、版本與授權狀態。
- 例外需記錄理由、範圍、期限與核准人。
- 禁止未經審查直接覆寫已發布資產。
- 發布前需通過品質 Gate，並同步 `CHANGELOG.md` 與 `VERSION`。

## Validation
定期檢查孤兒文件、失效連結、未登錄資產、重複 Token、過期例外與品牌偏差。

## Related Documents
`00-brand-philosophy.md`、`01-brand-guide.md`、`quality/`、`pipelines/`

## Version
Version: 1.0.0