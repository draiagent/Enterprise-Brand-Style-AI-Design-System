# Component: Card

## Purpose
承載一組相關資訊（工具介紹、功能重點、資料摘要）的獨立容器，是資訊圖、HTML 頁面與儀表板最基本的組成單位。

## Required Content
- 一個主要識別（icon 或短標籤）
- 標題（一行）

## Optional Content
- 說明文字（一至兩行）
- 次要資訊（連結、狀態、數字）
- 頁尾動作（連結、按鈕）

## Sizes / Variants
| 變體 | 用途 |
|---|---|
| `card--list-row` | 橫向清單列（icon + 標題 + 說明，見 `../examples/`） |
| `card--grid` | Grid 排列的功能卡（icon 置頂或置左，標題 + 說明） |
| `card--stat` | 承載單一數字／KPI 的卡片，數字需用 `tabular-nums`（見 `../tokens/typography.tokens.md`） |

差異只在排列方式與內容密度，不透過另外配色製造變體。

## States
- `default`
- `hover`（僅在卡片本身可點擊／可操作時才需要，純展示卡不需要 hover 效果）
- `focus`（可點擊卡片需要清楚的 focus outline）

## Tokens Used
`--card-bg`、`--card-border`、`--card-shadow`、`--card-shadow-hover`、`--radius-lg`、`--space-3`

```css
.card {
  background: var(--card-bg);
  border: 1px solid var(--card-border);
  border-radius: var(--radius-lg);
  box-shadow: var(--card-shadow);
  padding: var(--space-3);
}
.card:hover { box-shadow: var(--card-shadow-hover); }
```

## Accessibility
- 可點擊卡片必須是語意化的 `<a>` 或 `<button>`，不得只用 `div` + `onclick`（見 `../docs/13-accessibility-standard.md` Robust 原則）。
- 卡片內圖片需有替代文字；純裝飾性 icon 用 `aria-hidden="true"`。

## Prohibited Usage
- 不得在同一頁面混用超過兩種圓角級距（見 `spacing.tokens.md`）。
- 不得堆疊多重陰影或同時使用發光效果（見 `../docs/02-design-language.md`）。

## Example
```html
<div class="card card--list-row">
  <div class="tool-icon" aria-hidden="true">C</div>
  <div>
    <div class="tool-name">ChatGPT</div>
    <div class="tool-use">General-purpose chat</div>
  </div>
</div>
```

## Related Documents
`../docs/06-component-system.md`、`../tokens/color.tokens.md`、`../tokens/spacing.tokens.md`

## Version
Version: 0.1.0 (Draft)
