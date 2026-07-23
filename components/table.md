# Component: Table

## Purpose
呈現需要逐項比較或查閱明細的資料。依 `../docs/11-dashboard-design-standard.md`：分類過多（例如超過五類）時，改用表格取代圓餅圖或多重圖表。

## Required Content
- 表頭（每欄一個明確標籤）
- 至少一列資料

## Optional Content
- 排序控制
- 篩選控制
- 摘要列（總計、平均）

## Sizes / Variants
| 變體 | 用途 |
|---|---|
| `table--dense` | Dashboard、報表等高資訊密度情境 |
| `table--comfortable` | 一般文件、說明頁 |

## States
- 欄位可排序時：`sortable`、`sorted-asc`、`sorted-desc`
- 列可互動時：`hover`、`selected`

## Tokens Used
`--color-border`、`--color-text-secondary`、`--space-2`、`font-variant-numeric: tabular-nums`（數字欄位）

## Accessibility
- 使用語意化 `<table>`、`<thead>`、`<tbody>`，欄位標題用 `<th scope="col">`，列標題（如有）用 `<th scope="row">`（見 `../docs/13-accessibility-standard.md`：表格必須有標題與表頭關係）。
- 窄版（手機）情境下，依 `../docs/05-layout-grid.md` 的 Responsive Reflow：表格轉為卡片或摘要，不得直接縮小字體到不可讀。

## Prohibited Usage
- 不得用一堆 `<div>` 模擬表格外觀（破壞語意與螢幕閱讀器可讀性）。
- 數字欄位不得混用不同小數位或千分位規則（見 `../tokens/typography.tokens.md`）。

## Example
```html
<table class="table--dense">
  <thead><tr><th scope="col">工具</th><th scope="col">用途</th></tr></thead>
  <tbody>
    <tr><td>ChatGPT</td><td>一般對話</td></tr>
    <tr><td>Claude</td><td>深度推理與寫作</td></tr>
  </tbody>
</table>
```

## Related Documents
`../docs/11-dashboard-design-standard.md`、`../docs/13-accessibility-standard.md`、`../tokens/typography.tokens.md`

## Version
Version: 0.1.0 (Draft)
