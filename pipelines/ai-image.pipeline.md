# Pipeline: AI Image

## Requirement
向使用者確認：圖像用途、比例、受眾、內容重點、是否為系列的一部分。

## Planning
判斷這張圖是獨立產出還是系列的一部分（系列需固定使用同一組 Tokens／Visual Direction，見 `../docs/02-design-language.md`：同一系列輸出必須共享 Token、元件與圖像語言）。

## Pipeline Selection
本流程。

## Prompt
套用 `../prompts/ai-image-prompt-contract.md` 的八段式結構，填入 Requirement 階段收集的內容。

## Template
對照 `../templates/ai-image.template.md` 確認 Metadata、Required Sections 是否齊全。

## Components
若圖像需要呈現卡片、按鈕等 UI 元素（例如资訊圖裡的工具清單卡），描述時引用 `../components/card.md`、`../components/button.md` 的視覺定義，維持與網頁版一致的元件語言。

## Tokens
Visual Direction 與 Brand Constraints 段落直接引用 `../tokens/color.tokens.md`、`../tokens/typography.tokens.md`，不自創配色。

## Assets
若需要放入 Logo 或核准角色，查 `../assets/`；查無登錄資產時，不生成替代 Logo，改用純文字或幾何佔位並告知使用者。

## Generation
執行生圖（例如透過 `draw` 類工具呼叫 gpt-image-2 或其他核准的圖像模型），選擇最接近 Canvas 比例的輸出尺寸。

## Quality Review
對照 `../quality/quality-gate.md` 與 `../quality/checklist-ai-image.md` 逐項確認。

## Revision
未通過的項目記錄具體原因，修改 Prompt 對應段落後重新生成，不整段重寫（維持可追蹤性）。

## Release
- 標記輸出狀態（`draft` / `approved`，見 `../prompts/ai-image-prompt-contract.md` 的 Traceability 段落）。
- 若之後會重複使用，存放到 `../examples/` 並附上使用的 Prompt 與版本。
- 正式對外發布前需要 Approver 核准（`../docs/14-brand-governance.md`）。

## Related Documents
`../prompts/ai-image-prompt-contract.md`、`../templates/ai-image.template.md`、`../quality/checklist-ai-image.md`

## Version
Version: 0.1.0 (Draft)
