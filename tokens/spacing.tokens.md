# Spacing, Radius & Shadow Tokens

Status: **Draft — v0.1.0**（結構性數值，風險低於色彩／字體，但仍待 Owner 核准列入正式規範）。

依 `../docs/05-layout-grid.md`：所有間距由基準單位形成級距，禁止大量任意數值；依 `../docs/02-design-language.md`：主要容器採一致圓角級距，陰影僅表示層級或可操作性，不得多重堆疊。

## Spacing（8pt 基準）

```css
:root {
  --space-1: 8px;
  --space-2: 16px;
  --space-3: 24px;
  --space-4: 32px;
  --space-5: 40px;
  --space-6: 48px;
  --space-7: 64px;
  --space-8: 80px;
}
```

用法：同一關係用同一級距（例如卡片內部 padding 一律 `--space-3`），不同區塊之間用更大級距區隔（例如區塊間距用 `--space-5` 以上），不得為了「看起來剛好」插入級距以外的任意數值。

## Radius

```css
:root {
  --radius-sm:   10px;  /* 小型元件：badge 內部圖示、tag */
  --radius-md:   14px;  /* icon box */
  --radius-lg:   20px;  /* 卡片、對話框 */
  --radius-pill: 999px; /* CTA 按鈕、狀態 badge */
}
```

同層級容器（例如同一頁面裡的所有資訊卡）必須使用同一個 radius token，不得任意混用 `--radius-md` 與 `--radius-lg`。

## Shadow（層級表達，不堆疊多重效果）

```css
:root {
  --shadow-1: 0 1px 4px rgba(15, 23, 42, 0.06);   /* 靜態元件，如 badge */
  --shadow-2: 0 4px 20px rgba(15, 23, 42, 0.08);  /* 預設卡片 */
  --shadow-3: 0 10px 28px rgba(15, 23, 42, 0.13); /* hover / 可操作狀態 */
}
```

依 `02-design-language.md` 的 Rules：禁止多重強烈陰影、玻璃效果與發光同時堆疊——一個元件同一時間只使用一個 shadow token。

## Grid

- 網頁優先採 12 欄；簡報／海報依內容採 4、6、8 或 12 欄（見 `05-layout-grid.md`）。
- 支援的輸出比例：`1:1`、`3:4`、`4:5`、`9:16`、`16:9`、A4、網頁／儀表板（自由高度、固定欄寬）。

## Related Documents
`../docs/02-design-language.md`、`../docs/05-layout-grid.md`、`../components/README.md`

## Version
Version: 0.1.0 (Draft)
