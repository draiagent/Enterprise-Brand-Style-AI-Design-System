# Component: Callout

## Purpose
凸顯一組重點（例如「Best uses」「Pro tip」「注意事項」），比一般段落更醒目，但比 Card 更輕量、通常出現在 Card 或內文之間。

## Required Content
- 標題（一個詞或短語，例如「Best uses」）
- 至少一項重點內容（條列或短段落）

## Optional Content
- 圖示（標題左側）
- 補充連結

## Sizes / Variants
| 變體 | 用途 | Tokens |
|---|---|---|
| `callout--tip` | 建議、最佳實踐 | `--color-brand-primary` 系淺底 |
| `callout--warning` | 需要注意的限制或風險 | `--color-warning` 系淺底 |
| `callout--info` | 中性補充資訊 | `--color-info` 系淺底 |

## States
`default` only。

```css
.callout {
  background: color-mix(in srgb, var(--color-brand-primary) 8%, var(--color-surface));
  border: 1px solid var(--card-border);
  border-radius: var(--radius-lg);
  padding: var(--space-4);
}
.callout h3 { color: var(--color-brand-primary); font-size: var(--text-h4); font-weight: 800; }
```

## Accessibility
- 條列內容使用語意化 `<ul>`/`<li>`，不要用純換行模擬清單。
- `callout--warning` 不得只靠顏色傳達警示，標題文字本身要說明是警告（例如「注意」而不只是換個顏色）。

## Prohibited Usage
- 不得把 Callout 當成主要內容容器使用——它只用來凸顯重點，不是頁面的主結構。
- 一個畫面內同時出現多個 Callout 時，種類不得混雜超過兩種變體，避免視覺競爭。

## Example
```html
<div class="callout callout--tip">
  <h3>Best uses</h3>
  <ul>
    <li>Ask questions</li>
    <li>Draft faster</li>
    <li>Compare ideas</li>
  </ul>
</div>
```

## Related Documents
`../docs/02-design-language.md`、`../tokens/color.tokens.md`

## Version
Version: 0.1.0 (Draft)
