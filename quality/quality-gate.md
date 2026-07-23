# Quality Gate — General

適用於任何交付物類型的通用最低關卡。彙整自 `docs/00`、`docs/02`、`docs/03`、`docs/13`、`docs/14`。

## Brand & Message
- [ ] 品牌目的明確，訊息可在 5 秒內理解（`00-brand-philosophy.md`）
- [ ] 每個畫面只有一個第一視覺焦點，最多兩個次焦點（`02-design-language.md`）
- [ ] 未使用未核准的 Logo、人物或品牌名稱（`01-brand-guide.md`）
- [ ] 沒有混用超過三種視覺風格（`02-design-language.md`）

## Tokens & Components
- [ ] 色彩、字體、間距皆引用 `tokens/`，沒有另外散落的 Hex 值或任意數值
- [ ] 使用的元件存在於 `components/`，狀態與變體符合對應規格
- [ ] 若 `tokens/`／`components/` 仍為 Draft 狀態，交付物已標註為草稿

## Accessibility
- [ ] 文字與背景對比達標（一般文字 4.5:1，大字 3:1）
- [ ] 顏色不是唯一的資訊或狀態傳達方式
- [ ] 可鍵盤操作，Focus 順序合理清楚
- [ ] 圖片有適切替代文字，影片有字幕

## Content Integrity
- [ ] 繁體中文逐字校對，沒有簡繁混排或錯字
- [ ] 數字、單位、來源一致且可追溯
- [ ] 沒有將相關性描述為因果
- [ ] 沒有虛構的品牌背書、數據或事實

## Governance
- [ ] 版本已標註，重大變更已同步 `CHANGELOG.md`
- [ ] 若使用 Draft 資產／Token，交付物已標明「草稿，待核准」
- [ ] 正式發布前已有 Approver 核准（`14-brand-governance.md`）

## Related Documents
`../docs/00-brand-philosophy.md`、`../docs/02-design-language.md`、`../docs/13-accessibility-standard.md`、`../docs/14-brand-governance.md`

## Version
Version: 0.1.0 (Draft)
