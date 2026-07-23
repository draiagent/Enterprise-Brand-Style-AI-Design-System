# 05 — Layout and Grid

## Purpose
建立一致、可縮放且能跨比例轉換的版面系統。

## Scope
適用於 1:1、3:4、4:5、9:16、16:9、A4、網頁與儀表板。

## Principles
版面應先建立資訊層級，再分配網格；響應式轉換是重新編排，不是等比例縮小。

## Standards
### Grid
使用一致欄數、外距與間距 Token。網頁優先採 12 欄；簡報與海報可依內容採 4、6、8 或 12 欄。

### Spacing
所有間距由基準單位形成級距，禁止大量任意數值。相同關係使用相同間距，不同區塊以更大間距區隔。

### Safe Area
標題、Logo、頁碼、CTA 與重要數據不得貼近裁切區或裝置介面遮蔽區。

### Responsive Reflow
- 先保留標題、核心訊息、主圖與 CTA。
- 表格在窄版轉為卡片或摘要，不直接縮小至不可讀。
- 橫式流程在直式版可改為分段階梯或時間軸。

## Rules
- 禁止以空白不足為由縮小字體至不可讀。
- 不在同頁使用多套不相容網格。
- 重要元素需對齊共同基準線。
- 視覺重量需平衡，不要求機械式左右對稱。

## Validation
檢查對齊、間距級距、安全區、比例轉換與資訊保留順序。

## Related Documents
`04-typography.md`、`06-component-system.md`、`12-presentation-standard.md`

## Version
Version: 1.0.0