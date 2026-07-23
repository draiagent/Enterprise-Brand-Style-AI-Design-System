# Checklist — AI Image

先過 `quality-gate.md`，再檢查以下項目（彙整自 `docs/07`、`docs/08`、`docs/09`）。

- [ ] Prompt 依 `prompts/ai-image-prompt-contract.md` 八段式結構組成，且已保存版本、模型與參考圖紀錄
- [ ] 圖中沒有生成或模擬真實 Logo、真人肖像
- [ ] 圖中若有精確繁體中文，已後製排版校對，不依賴模型一次生成正確
- [ ] Icon／插畫風格與系列內其他圖像一致（同一系列、同一透視角、同一光源、同一陰影）
- [ ] 沒有使用表情符號取代正式企業圖示
- [ ] 圖片比例與實際輸出尺寸符合 Canvas 需求（見 `tokens/spacing.tokens.md` Grid 段落）
- [ ] 沒有多餘、未要求的人物、浮水印或 QR Code
- [ ] 若圖中出現新的角色／視覺元素且會重複使用，已規劃登錄到 `assets/`

## Related Documents
`../prompts/ai-image-prompt-contract.md`、`../docs/08-illustration-system.md`、`../docs/09-image-prompt-system.md`

## Version
Version: 0.1.0 (Draft)
