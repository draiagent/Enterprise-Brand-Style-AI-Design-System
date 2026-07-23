# Example: AI Assistants Card

## Status
**Draft — 尚未經 Owner 核准，不視為正式品牌交付物。**

## What This Demonstrates
同一份內容（「AI Assistants」資訊卡：頁碼、標題、副標、工具清單、Best uses、CTA）分別用兩條 Pipeline 產出，證明 `tokens/` 與 `components/` 可以同時支撐圖片與網頁兩種輸出媒介：

| 檔案 | 對應 Pipeline | 說明 |
|---|---|---|
| `ai-assistants-1of8.png` | `../../pipelines/ai-image.pipeline.md` | 用 `prompt-used.txt` 的 Prompt 交給 gpt-image-2 生成的 PNG |
| `ai-assistants-card.html` | `../../pipelines/html-page.pipeline.md` | 用 `../../tokens/` 的 CSS 變數直接刻出的網頁版本 |
| `prompt-used.txt` | — | 實際用來生圖的完整 Prompt（依 `../../prompts/ai-image-prompt-contract.md` 組成） |

## Known Gaps（核准前不應忽略）
- 色彩為估值，未跑過 `../../docs/13-accessibility-standard.md` 的正式對比檢查。
- PNG 版本裡的機器人吉祥物是模型自行加上的細節，未登錄於 `../../assets/`，不應視為核准角色。
- 兩個版本沒有跑過 `../../quality/checklist-ai-image.md` 與 `checklist-html-page.md` 的正式簽核，只做過目視比對。

## Related Documents
`../../pipelines/ai-image.pipeline.md`、`../../pipelines/html-page.pipeline.md`、`../../prompts/ai-image-prompt-contract.md`

## Version
Version: 0.1.0 (Draft)
