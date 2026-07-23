# 10 — HTML Design Standard

## Purpose
定義可部署、響應式、可存取且符合品牌的 HTML 網頁標準。

## Scope
適用於單頁網站、課程網站、成果展示、文件入口、互動資訊圖與 GitHub Pages。

## Principles
內容結構、語意 HTML、可存取性與效能優先於視覺特效。

## Standards
### Structure
使用 `header`、`nav`、`main`、`section`、`article`、`footer` 等語意元素；每頁只有一個主要 `h1`，標題層級不可跳躍。

### Design
CSS 優先引用 Token；元件採可重用 Class 或元件化架構。所有版面需支援桌面、平板與手機。

### Interaction
鍵盤可操作、Focus 清楚、按鈕與連結語意正確；互動圖表需提供文字摘要或表格替代。

### Performance
圖片採適當格式、尺寸與 lazy loading；避免無必要大型套件、影片自動播放與阻塞資源。

## Rules
- 禁止將主要內容只放在 Canvas 或圖片內。
- 禁止使用無替代文字的重要圖片。
- 禁止把敏感金鑰寫入前端程式碼。
- GitHub Pages 部署須包含清楚 README 與相對路徑。

## Validation
檢查 HTML 語意、響應式、鍵盤操作、Lighthouse 指標、連結與部署路徑。

## Related Documents
`04-typography.md`、`05-layout-grid.md`、`06-component-system.md`、`13-accessibility-standard.md`

## Version
Version: 1.0.0