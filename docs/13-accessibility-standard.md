# 13 — Accessibility Standard

## Purpose
確保不同能力、裝置與使用情境的使用者均可理解與操作品牌內容。

## Scope
適用於網頁、文件、簡報、圖表、影片、社群圖片與互動介面。

## Principles
無障礙不是最終檢查，而是設計輸入；內容不得只依賴視覺、顏色、聲音或滑鼠操作。

## Standards
### Perceivable
文字與背景需有足夠對比；圖片提供適切替代文字；影片提供字幕，重要聲音資訊提供文字描述。

### Operable
所有功能可透過鍵盤操作；Focus 順序合理且清楚；點擊區域具有足夠尺寸。

### Understandable
使用清楚語言、一致導覽、可辨識錯誤訊息與修正方式。

### Robust
使用語意標記、有效標籤與必要 ARIA；優先使用原生元素而非模擬控制項。

## Rules
- 顏色不得是唯一狀態提示。
- 不使用快速閃爍或無法停止的動畫。
- 替代文字描述資訊目的，不重複無意義檔名。
- 表格必須有標題與表頭關係。

## Validation
依 WCAG 原則進行自動檢查、鍵盤測試、螢幕閱讀器抽查與人工內容審查。

## Related Documents
`03-color-system.md`、`04-typography.md`、`10-html-design-standard.md`、`11-dashboard-design-standard.md`

## Version
Version: 1.0.0