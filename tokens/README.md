# Tokens

## Purpose
提供 `docs/` 規範對應的具體設計數值（色彩、字體、間距），作為 `components/`、`templates/`、`prompts/` 與 `pipelines/` 的單一數值來源。`docs/03-color-system.md` 明確禁止在文件中散落未登錄 Hex 值——所有正式色碼、字體、間距數值都應該只存在這裡，其他地方用引用。

## Status
**Draft — v0.1.0，尚未經 Owner 核准。**

這批 Token 是從使用者提供的參考視覺（一組 SaaS AI Workflow Carousel 資訊圖）用肉眼估色與量測比例反推出來的近似值，不是正式企業色碼或字體授權清單。依 `docs/14-brand-governance.md`：
- 正式資產必須有來源、擁有者、版本與授權狀態——這份 Token 集目前只滿足「來源」（估色自參考圖），缺「Owner 核准」與「授權狀態」，因此標記 Draft。
- 使用這批 Token 產出的任何交付物，都應該視為草稿，不應包裝成最終正式品牌交付物對外發布。
- 若之後 `.bootstrap/` 套件解壓縮出正式 `tokens/`，或 Owner 提供實際企業色碼／字體授權，需要人工比對合併，並將版本推進到 1.0.0，同步更新 `CHANGELOG.md`。

## Files
| 檔案 | 內容 |
|---|---|
| `color.tokens.md` | Primitive / Semantic / Component 三層色彩 Token |
| `typography.tokens.md` | 字體角色、字級、行高、繁體中文排版規則 |
| `spacing.tokens.md` | 8pt 間距系統、圓角級距、陰影級距 |

## Related Documents
`../docs/03-color-system.md`、`../docs/04-typography.md`、`../docs/05-layout-grid.md`、`../docs/14-brand-governance.md`

## Version
Version: 0.1.0 (Draft)
