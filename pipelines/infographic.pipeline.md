# Pipeline: Infographic

## Requirement
向使用者確認：核心問題、主要資料、分類方式、關鍵數字、資料來源、是否為系列（Carousel）的一部分（見 `../templates/infographic.template.md` 的 Inputs）。

## Planning
若是系列，先決定整套共用的頁碼／系列標籤格式與固定的視覺結構（Title → Subtitle → Cards → CTA），每一張只換內容，不換風格（見 `../docs/02-design-language.md`）。

## Pipeline Selection
本流程。單張圖像輸出時，本流程與 `ai-image.pipeline.md` 銜接使用。

## Prompt
套用 `../prompts/ai-image-prompt-contract.md`，Content Hierarchy 段落依 `../templates/infographic.template.md` 的 Required Sections（標題與結論、3–7 個資訊群組、圖例／流程／比較關係、來源與版本）填入。

## Template
`../templates/infographic.template.md`。

## Components
資訊群組對應 `../components/card.md`（`card--grid` 或 `card--list-row` 變體），頁碼／系列標籤對應 `../components/badge.md`，重點提示對應 `../components/callout.md`，CTA 對應 `../components/button.md`。

## Tokens
色彩、字體、間距、圓角、陰影全部引用 `../tokens/`，系列中每一張都用同一套值。

## Assets
若需放品牌 Logo，查 `../assets/`；無登錄資產則不生成。

## Generation
依輸出媒介選擇：
- 圖片（PNG）→ 走 `ai-image.pipeline.md` 的 Generation 段落。
- 網頁／Artifact 版本 → 走 `html-page.pipeline.md` 的 Generation 段落，套用相同 Tokens 與 Components。

## Quality Review
對照 `../quality/quality-gate.md` 與 `../quality/checklist-infographic.md`；系列產出需額外檢查「每張是否用同一套 Tokens」。

## Revision
單張有問題只修那一張的內容段落，不重新設計整套系列的風格。

## Release
- 標記草稿／核准狀態。
- 系列產出建議整套一起存放於 `../examples/` 或交付物目錄，方便之後比對一致性。
- 正式對外發布前需要 Approver 核准（`../docs/14-brand-governance.md`）。

## Related Documents
`../templates/infographic.template.md`、`../prompts/ai-image-prompt-contract.md`、`../quality/checklist-infographic.md`

## Version
Version: 0.1.0 (Draft)
