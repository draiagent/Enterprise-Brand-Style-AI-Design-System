# 03 — Color System

## Purpose
定義品牌色、語意色、資料視覺化色彩與可讀性規則。

## Scope
適用於印刷、數位介面、簡報、圖表、海報、AI 圖像與品牌資產。

## Principles
色彩用於品牌辨識、資訊分類、狀態表達與視覺焦點，不以顏色作為唯一訊息載體。

## Standards
### Token Layers
1. Primitive：原始色階。
2. Semantic：`background`、`surface`、`text`、`border`、`success`、`warning`、`danger`、`info`。
3. Component：按鈕、標籤、圖表、卡片等元件專用 Token。

### Usage
- 主品牌色只用於關鍵識別與主要行動。
- 輔助色用於分類，單畫面原則上不超過五個主分類色。
- 危險、警告、成功與資訊色不得交換語意。
- 文字與背景需達可接受對比；一般文字以 4.5:1 為基準，大字至少 3:1。

### Data Visualization
同類資料保持同色系，時間序列保持固定色彩映射；需要比較時優先使用明度、線型、標記與標籤共同區分。

## Rules
- 禁止直接在文件中散落未登錄 Hex 值。
- 禁止只用紅綠辨識狀態。
- 漸層不得承載精確數值判讀。
- 印刷輸出需另行檢查 CMYK 偏色。

## Validation
檢查 Token 來源、對比、色彩語意、色盲辨識與印刷適配。

## Related Documents
`tokens/`、`11-dashboard-design-standard.md`、`13-accessibility-standard.md`

## Version
Version: 1.0.0