# Pipeline: HTML Page

## Requirement
向使用者確認：頁面目標、內容架構、CTA、資料來源、是否需要深色模式、是否需要響應式（通常皆需要，見 `../docs/10-html-design-standard.md`）。

## Planning
判斷頁面屬於 Landing Page、工具型頁面、或儀表板性質，決定要用哪些 `components/` 組合（Nav、Card、Callout、Button、Table、Chart Container）。

## Pipeline Selection
本流程。

## Prompt
若部分內容（文案、CTA 措辭）需要 AI 輔助草擬，依 `../docs/00-brand-philosophy.md` Clarity First 原則撰寫，不套用 AI 圖像的 Prompt Contract（那是給生圖用的）。

## Template
對照 `../templates/html-page.template.md` 的 Required Sections：Header/Nav、Hero、Core Value、Main Content、Evidence/Cases、CTA、Footer。

## Components
組裝 `../components/nav.md`、`card.md`、`button.md`、`callout.md`、`table.md`、`chart-container.md` 中符合需求的元件，不重新設計已有規格的元件。

## Tokens
`<style>` 或 `:root` 直接引用 `../tokens/color.tokens.md`、`typography.tokens.md`、`spacing.tokens.md` 的 CSS 變數，包含深色模式段落。

## Assets
若頁面需要 Logo 或品牌圖片，查 `../assets/`；查無登錄資產時先用文字或幾何佔位。

## Generation
產出 HTML／CSS（必要時含少量 JS），遵循 `../docs/10-html-design-standard.md` 的 Structure／Design／Interaction／Performance 標準。

## Quality Review
對照 `../quality/quality-gate.md` 與 `../quality/checklist-html-page.md` 逐項確認，包含鍵盤操作與雙主題對比。

## Revision
依 Quality Review 的具體項目修正，優先修結構與可存取性問題，其次才是視覺細節。

## Release
- 部署前確認相對路徑正確（尤其 GitHub Pages 情境）。
- 標記 Token／元件是否仍為 Draft 狀態，若是，頁面應包含或旁註「草稿」標示。
- 正式對外發布前需要 Approver 核准（`../docs/14-brand-governance.md`）。

## Related Documents
`../templates/html-page.template.md`、`../docs/10-html-design-standard.md`、`../quality/checklist-html-page.md`

## Version
Version: 0.1.0 (Draft)
