# Checklist — HTML Page

先過 `quality-gate.md`，再檢查以下項目（彙整自 `docs/10`、`docs/13`）。

- [ ] 使用語意化 HTML（`header`/`nav`/`main`/`section`/`article`/`footer`），每頁只有一個 `h1`，標題層級不跳躍
- [ ] 主要內容沒有只放在 Canvas 或圖片內
- [ ] 所有重要圖片都有替代文字
- [ ] CSS 值優先引用 `tokens/`，元件優先引用 `components/`
- [ ] 支援桌面、平板、手機三種寬度，且已實際檢查（非只靠 flex/grid 假設）
- [ ] 支援亮／暗兩種主題，Token 在兩種主題下都經過對比確認
- [ ] 鍵盤可操作，Focus 樣式清楚可見
- [ ] 沒有敏感金鑰寫在前端程式碼
- [ ] 圖片使用適當格式、尺寸與 lazy loading，沒有不必要的大型套件或自動播放影片
- [ ] 若部署到 GitHub Pages，已包含清楚 README 與相對路徑

## Related Documents
`../docs/10-html-design-standard.md`、`../docs/13-accessibility-standard.md`

## Version
Version: 0.1.0 (Draft)
