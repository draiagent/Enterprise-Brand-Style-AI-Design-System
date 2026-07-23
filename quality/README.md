# Quality

## Purpose
把 `docs/` 各文件的 Validation 段落轉成可實際勾選的檢查清單，作為交付物發布前的品質關卡。依 `../docs/14-brand-governance.md`：發布前需通過品質 Gate。

## Status
Draft — v0.1.0。目前涵蓋通用關卡與三種已有 Pipeline 的交付物類型（AI Image、HTML Page、Infographic）；其餘交付物類型可先套用 `quality-gate.md` 的通用項目。

## Files
| 檔案 | 用途 |
|---|---|
| `quality-gate.md` | 所有交付物都適用的通用關卡 |
| `checklist-ai-image.md` | AI 圖像專屬檢查項目 |
| `checklist-html-page.md` | HTML 頁面專屬檢查項目 |
| `checklist-infographic.md` | 資訊圖表專屬檢查項目 |

## Usage
1. 先過 `quality-gate.md` 的通用項目。
2. 再過對應交付物類型的專屬 checklist。
3. 有任何一項未通過，交付物標記為「未通過品質關卡」，不得對外發布或包裝成正式版本。
4. 檢查結果可用 `../templates/quality-report.template.md` 記錄。

## Related Documents
`../docs/14-brand-governance.md`、`../templates/quality-report.template.md`

## Version
Version: 0.1.0 (Draft)
