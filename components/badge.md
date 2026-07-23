# Component: Badge / Eyebrow

## Purpose
標示頁碼、系列名稱、分類或狀態的小型文字標籤。用於資訊圖頁碼（「1 / 8」）、系列標籤（「YOUR COMPLETE GUIDE」）或狀態提示。

## Required Content
- 簡短文字（建議不超過全形 12 字或半形 24 字元）

## Optional Content
- 小型 icon

## Sizes / Variants
| 變體 | 用途 |
|---|---|
| `badge--page` | 頁碼／序號，中性樣式（邊框無底色） |
| `badge--eyebrow` | 系列／分類標籤，使用 `--color-brand-accent` |
| `badge--status` | 狀態提示，使用語意色（`--color-success` / `--color-warning` / `--color-danger` / `--color-info`），**不得**使用分類色 |

## States
`default` only（純展示元件，一般不具互動性；若做成可篩選的 filter chip，需額外定義 `selected` 狀態）。

```css
.badge {
  display: inline-flex;
  align-items: center;
  gap: 6px;
  padding: 6px 14px;
  border-radius: var(--radius-pill);
  font-size: var(--text-caption);
  font-weight: 700;
  border: 1.5px solid var(--badge-border);
  color: var(--badge-text);
}
```

## Accessibility
- 純狀態提示不得只靠顏色表達（見 `../docs/13-accessibility-standard.md`），文字本身要講清楚狀態（例如「處理中」而不是只用黃色圓點）。

## Prohibited Usage
- 不得用分類色（Automation 紫、Create 橘）表達狀態語意（成功／警告／錯誤），語意色與分類色不得互換（見 `../tokens/color.tokens.md`）。
- 不得塞入完整句子——超過長度需求時應改用 Callout 元件。

## Example
```html
<span class="badge badge--page">1 / 8</span>
<span class="badge badge--eyebrow">YOUR COMPLETE GUIDE</span>
```

## Related Documents
`../docs/03-color-system.md`、`../tokens/color.tokens.md`

## Version
Version: 0.1.0 (Draft)
