# Component: Nav

## Purpose
提供頁面／工具間的導覽，讓使用者知道自己在哪、能去哪。適用於 HTML 頁面、多頁 Dashboard 與課程網站。

## Required Content
- 首頁／根導覽連結
- 目前可用的頁面／工具清單

## Optional Content
- 目前頁面的高亮標示
- 次要動作（例如登入、切換語言）

## Sizes / Variants
| 變體 | 用途 |
|---|---|
| `nav--topbar` | 桌面／平板頂部導覽列 |
| `nav--tabs` | 頁面內分頁切換（例如同一工具內的「出題／測驗／結果」） |

## States
- `default`
- `current`（標示目前所在頁面／分頁，需同時有視覺與 `aria-current="page"`）
- `focus`

```css
.nav--topbar {
  display: flex;
  flex-wrap: wrap;
  gap: var(--space-2);
  align-items: center;
  padding: var(--space-2) var(--space-3);
  background: var(--primitive-navy-900);
}
.nav--topbar a { color: var(--primitive-white); }
.nav--topbar a[aria-current="page"] { color: var(--color-brand-accent); font-weight: 700; }
```

## Accessibility
- 使用語意化 `<nav>` 包裹，不用一般 `<div>`。
- 目前頁面用 `aria-current="page"` 標示，不只靠顏色。
- 響應式收合（漢堡選單）時，觸發按鈕需要清楚的 `aria-expanded` 狀態。

## Prohibited Usage
- 不得把導覽做成純圖片或純 Canvas（見 `../docs/10-html-design-standard.md`：主要內容不得只放在 Canvas 或圖片內）。

## Example
```html
<nav class="nav--topbar">
  <a href="/">🏠 工具首頁</a>
  <a href="/formative-quiz.html" aria-current="page">形成性測驗</a>
</nav>
```

## Related Documents
`../docs/10-html-design-standard.md`、`../docs/13-accessibility-standard.md`

## Version
Version: 0.1.0 (Draft)
