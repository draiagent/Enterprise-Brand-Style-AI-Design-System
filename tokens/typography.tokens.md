# Typography Tokens

Status: **Draft — v0.1.0，待 Owner 核准字族授權**。

依 `../docs/04-typography.md`：單一輸出原則上不超過兩個字族，繁體中文需完整支援、避免簡繁混排。

## Font Families

```css
:root {
  --font-latin: 'Inter', -apple-system, 'Segoe UI', sans-serif;
  --font-tc:    'Noto Sans TC', var(--font-latin);
  --font-mono:  'JetBrains Mono', 'Consolas', monospace;
}
```

`Inter` 與 `Noto Sans TC` 是暫定選擇（免費、支援完整繁體中文、風格與參考視覺的 Sans Serif 現代感相符），尚未經 Owner 核准為正式企業字族；若企業已有指定字體授權，需替換此檔案並將版本推進到 1.0.0。

## Roles（對應 04-typography.md 的 Roles）

| Role | 用途 | 字級 (rem) | 字重 | 行高 |
|---|---|---|---|---|
| Display | 封面／主視覺標題 | 2.75–3.5 | 800 | 1.05 |
| Heading 1 | 主要段落標題 | 2.0 | 800 | 1.15 |
| Heading 2 | 次段落標題 | 1.5 | 700 | 1.2 |
| Heading 3 | 卡片／區塊標題 | 1.15 | 700 | 1.3 |
| Heading 4 | 小標籤標題 | 1.0 | 600 | 1.4 |
| Body | 主要閱讀文字 | 1.0 | 400 | 1.6（繁中建議 1.6–1.8） |
| Caption | 註解、來源、輔助資訊 | 0.85 | 500 | 1.5 |
| Mono | 程式碼、變數、技術識別 | 0.9 | 400 | 1.5 |

```css
:root {
  --text-display:  clamp(2.75rem, 6vw, 3.5rem);
  --text-h1: 2rem;
  --text-h2: 1.5rem;
  --text-h3: 1.15rem;
  --text-h4: 1rem;
  --text-body: 1rem;
  --text-caption: 0.85rem;

  --leading-tc-body: 1.7;     /* 繁體中文內文，落在 04 建議的 1.5–1.8 倍區間 */
  --leading-latin-body: 1.6;
  --leading-heading: 1.15;
}
```

## Numbers（對應 04 的 Numbers 規則）
儀表板與資料類介面數字使用 tabular figures：

```css
.tabular-nums { font-variant-numeric: tabular-nums; }
```

百分比、小數位與千分位規則：同一畫面內固定小數位數，千分位一律使用逗號分隔，不與其他分隔符混用。

## Rules Recap
- 單一交付物最多兩個字族（此處為 `--font-latin` / `--font-tc` 視為一組，`--font-mono` 僅用於程式碼場景，不計入兩族限制）。
- 不使用全大寫英文長段落；英文標籤可用 `text-transform: uppercase` 搭配 `letter-spacing`，但僅限短標籤（如 Badge、Eyebrow），不用於長句。
- 重要繁體中文文字不依賴 AI 圖像模型直接生成，需後製排版（見 `../docs/09-image-prompt-system.md`）。

## Related Documents
`../docs/04-typography.md`、`../docs/05-layout-grid.md`、`../docs/10-html-design-standard.md`

## Version
Version: 0.1.0 (Draft)
