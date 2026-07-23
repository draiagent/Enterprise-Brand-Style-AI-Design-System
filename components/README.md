# Components

## Purpose
定義可重用的視覺／介面元件規格，讓 `templates/` 與 `pipelines/` 用引用的方式組合頁面，而不是每次重新設計。依 `../docs/06-component-system.md`：元件由 Token 驅動，具明確用途、輸入、狀態、變體與品質要求。

## Status
**Draft — v0.1.0，待 Owner 核准。** 這批元件是依照 `../docs/06-component-system.md` 列出的元件類型（卡片、按鈕、標籤、導覽、表格、圖表容器、提示、流程節點、人物卡、品牌資訊區）優先建立**最常用的八個**；「人物卡」與「品牌資訊區」留待有實際使用情境（例如角色插畫定案、正式品牌資產登錄）後再補上，避免在沒有真實內容前先發明規格。

## Component Contract
每個元件檔案至少包含：

- **Name** — 功能與角色命名，不以外觀命名（例如用 `callout` 不用 `blue-box`）。
- **Purpose** — 用途與使用時機。
- **Required Content** — 必要輸入。
- **Optional Content** — 選用輸入。
- **Sizes / Variants** — 尺寸與變體，差異需有語意，不只是換色。
- **States** — default / hover / focus / active / disabled / loading / error / success（視元件性質選用）。
- **Tokens Used** — 引用 `../tokens/` 的哪些變數，不得另外寫死數值。
- **Accessibility** — 對應 `../docs/13-accessibility-standard.md` 的具體要求。
- **Prohibited Usage** — 禁止用法。
- **Example** — 一個實際填入內容的範例（HTML 或結構描述）。

## Index

| 元件 | 檔案 | 對應 06 的元件類型 |
|---|---|---|
| Card | `card.md` | 卡片 |
| Button / CTA | `button.md` | 按鈕 |
| Badge / Eyebrow | `badge.md` | 標籤 |
| Callout | `callout.md` | 提示 |
| Nav | `nav.md` | 導覽 |
| Table | `table.md` | 表格 |
| Chart Container | `chart-container.md` | 圖表容器 |
| Process Node | `process-node.md` | 流程節點 |

## Rules
- 不為單次需求新增近似重複元件——先檢查這個索引有沒有可以延伸變體的既有元件。
- AI 生成的一次性元件，若之後會重複使用，需回寫成正式規格檔案後才能被其他 pipeline 引用（見 `../docs/06-component-system.md`）。

## Related Documents
`../docs/06-component-system.md`、`../tokens/`、`../docs/13-accessibility-standard.md`

## Version
Version: 0.1.0 (Draft)
