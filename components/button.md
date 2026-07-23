# Component: Button / CTA

## Purpose
觸發主要或次要行動（前往下一步、送出表單、切換頁面）。CTA 變體用於資訊圖與網頁的主要行動呼籲。

## Required Content
- 動詞開頭的明確文字（例如「查看完整方法論」，不用「更多」）

## Optional Content
- 方向或動作 icon（例如箭頭），僅在強化「這是導覽性行動」時使用

## Sizes / Variants
| 變體 | 用途 | Tokens |
|---|---|---|
| `button--primary` | 頁面唯一主要行動，漸層底 | `--button-cta-bg`、`--button-cta-text` |
| `button--secondary` | 次要行動 | `--color-surface` 底、`--color-brand-primary` 邊框與文字 |
| `button--ghost` | 低強調行動（例如「稍後再說」） | 無底色，僅文字 + `--color-text-secondary` |

一個畫面只能有一個 `button--primary`（對應 `../docs/02-design-language.md` 的「每一畫面只設一個第一視覺焦點」）。

## States
`default`、`hover`、`focus`、`active`、`disabled`、`loading`

```css
.button--primary {
  background: var(--button-cta-bg);
  color: var(--button-cta-text);
  border-radius: var(--radius-pill);
  box-shadow: var(--shadow-2);
  padding: var(--space-2) var(--space-4);
}
.button--primary:hover  { box-shadow: var(--shadow-3); }
.button--primary:disabled { opacity: 0.5; cursor: not-allowed; box-shadow: none; }
```

## Accessibility
- 必須是 `<button>` 或 `<a>`，鍵盤可達且有清楚 focus 樣式（不得 `outline: none` 而不提供替代焦點樣式）。
- `disabled` 狀態需同時反映在視覺與 `aria-disabled`／原生 `disabled` 屬性。
- 文案本身要說明會發生什麼事，不用「確定」「送出」這種需要靠上下文才懂的字（見 `../docs/00-brand-philosophy.md` Clarity First）。

## Prohibited Usage
- 不得一個畫面出現兩個以上的 `button--primary`。
- 不得用顏色以外沒有任何提示就把可點擊與不可點擊按鈕做成一樣的樣子。

## Example
```html
<button class="button--primary">Swipe for Knowledge Hub →</button>
```

## Related Documents
`../docs/02-design-language.md`、`../docs/13-accessibility-standard.md`、`../tokens/color.tokens.md`

## Version
Version: 0.1.0 (Draft)
