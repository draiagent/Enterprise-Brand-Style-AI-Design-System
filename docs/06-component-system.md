# 06 — Component System

## Purpose
定義可重用視覺與介面元件的結構、狀態和組合規則。

## Scope
包含卡片、按鈕、標籤、導覽、表格、圖表容器、提示、流程節點、人物卡與品牌資訊區。

## Principles
元件由 Token 驅動，具明確用途、輸入、狀態、變體及品質要求。

## Standards
每個元件至少定義：名稱、用途、必要內容、選用內容、尺寸、狀態、變體、可存取性、禁止用法與範例。

### States
互動元件應涵蓋 default、hover、focus、active、disabled、loading、error 與 success，視情境選用。

### Composition
頁面或素材由元件組合，不直接複製已失去來源關係的圖層。高階 Pattern 可由多個元件構成，但不得重複定義底層 Token。

## Rules
- 不為單次需求新增近似重複元件。
- 變體差異應有語意，不只為換色。
- 元件名稱使用功能與角色，不以外觀命名。
- AI 生成元件需回寫正式規格後才可重用。

## Validation
檢查元件是否存在於 `components/`、是否使用 Token、狀態是否完整、是否可被模板與 Pipeline 調用。

## Related Documents
`components/`、`tokens/`、`05-layout-grid.md`、`13-accessibility-standard.md`

## Version
Version: 1.0.0