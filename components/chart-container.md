# Component: Chart Container

## Purpose
包裹一個圖表並附上圖表本身無法傳達的中繼資訊（單位、期間、來源、更新時間），確保圖表不會脫離資料脈絡被誤讀。依 `../docs/11-dashboard-design-standard.md`：資料需顯示期間、單位、來源、更新時間與缺漏狀態。

## Required Content
- 圖表標題
- 資料期間或時間戳
- 圖表本體
- 資料來源

## Optional Content
- 單位說明
- 與目標值／基準的比較
- 文字摘要或替代表格（見無障礙需求）

## Sizes / Variants
| 變體 | 適用圖表類型 |
|---|---|
| `chart--trend` | 折線圖，時間趨勢 |
| `chart--comparison` | 排序長條圖，類別比較 |
| `chart--distribution` | 直方圖／箱型圖 |
| `chart--relationship` | 散點圖 |

依 `../docs/11-dashboard-design-standard.md`：避免 3D 圖、裝飾性儀表與難以比較的多個圓餅圖；類別過多時改用 `../components/table.md`。

## States
- `loading`（資料載入中，需明確的載入指示，不得顯示空白或誤導性的零值圖表）
- `empty`（無資料，需明確文字說明，不得留白讓使用者誤以為是零）
- `error`（資料取得失敗，需說明原因與下一步）

## Tokens Used
`--chart-categorical-1` ~ `--chart-categorical-5`（見 `../tokens/color.tokens.md`，同類資料固定同一色彩映射）

## Accessibility
- 互動圖表需提供文字摘要或表格替代（見 `../docs/13-accessibility-standard.md`）。
- 顏色不得是唯一的資料區分方式，需搭配線型、標記或直接標籤。
- 軸線截斷需要明確標示，不得暗示未截斷的比例。

## Prohibited Usage
- 不得省略資料期間、單位或來源。
- 不得把相關性圖表的標題寫成因果關係陳述（見 `../docs/11-dashboard-design-standard.md` Rules）。

## Example
```html
<figure class="chart--trend">
  <figcaption>
    <h3>週活躍使用者</h3>
    <p>期間：2026-06-01 – 2026-06-30・單位：人次・來源：內部分析後台・更新於 2026-07-01</p>
  </figcaption>
  <!-- 圖表本體 -->
  <table class="sr-only">
    <caption>週活躍使用者文字替代表格</caption>
    <!-- 對應資料列 -->
  </table>
</figure>
```

## Related Documents
`../docs/11-dashboard-design-standard.md`、`../docs/13-accessibility-standard.md`、`../tokens/color.tokens.md`

## Version
Version: 0.1.0 (Draft)
