# AGENT — Decision Policy

## Purpose
定義 AI 代理（例如 Claude）在使用這套設計系統產出內容時，遇到規範衝突、資訊不足或風險情境時該如何決策，而不是每次都停下來問使用者。

## Scope
適用於任何依 `SKILL.md` 路由後、實際執行 Pipeline 產出交付物的 AI 代理行為。

## Principles
延續 `00-brand-philosophy.md` 的 Human-Governed AI 原則：AI 負責加速與一致性執行，人員負責核准、風險判斷與最終品牌責任。代理應該「照規範做決定」，而不是「照喜好做決定」。

## Decision Rules

### 規範衝突時
依 `docs/README.md` 的 Document Contract：治理文件（`14-brand-governance.md`）> 設計 Token（`tokens/`）> 版本較新的正式規範 > 一般 docs 說明。同層級衝突時，優先滿足 Accessibility（`13`）與 Brand Governance（`14`），其次才是視覺偏好。

### 資訊不足時
- 缺「內容」（標題、資料、CTA 文字等）：必須向使用者收集，不得代替使用者發明品牌訊息、數據或事實。
- 缺「風格細節」（色彩、字體、圓角、間距等）：不用問，直接套用 `tokens/`、`components/`；若 `tokens/` 尚未有對應值，使用其 Draft 值並在產出中標註「草稿色彩，待核准」。
- 缺「品牌資產」（Logo、角色、核准圖片）：查 `assets/`；找不到已登錄資產時停止使用該資產，改用純文字或幾何佔位，並告知使用者需要補登錄，不得自行生成替代 Logo。

### 品質與風險
- 任何要對外發布、公開分享或用於正式場合的交付物，先過 `quality/` 對應 checklist；沒有專屬 checklist 就用 `quality/quality-gate.md`。
- Token、元件、資產仍是 Draft（v0.x）狀態時，交付物需標註「草稿／待核准」，不得包裝成最終正式版本對外發布。
- 涉及真人肖像、未授權品牌、精確數字或事實主張時，代理不得自行假設或美化，需要求使用者提供正式來源。

### 何時要暫停詢問使用者
- 交付物類型無法對應到 `SKILL.md` 的 Routing Table，且沒有近似項目可比照。
- 使用者要求的內容明顯違反 `01-brand-guide.md`（例如要求偽造 Logo、混用未授權品牌）。
- 需要對已發布資產做 Major 等級變更（依 `14-brand-governance.md` 的 Change Classes）。
- 其餘情況（風格細節、Token 套用方式、元件挑選）代理應自行依規範決定，不需要每次都回頭確認。

## Rules
- 代理決策需可追蹤：重大選擇（例如選用哪個 Pipeline、跳過哪個 Optional Section）應在交付物或 PR 說明中留下理由。
- 不得為了加快產出而略過 `quality/` 檢查或 `assets/` 登錄查核。
- 代理不因為「自動化」而免除品牌責任，最終正式發布仍需人員核准（`14-brand-governance.md` 的 Approver 角色）。

## Related Documents
`SKILL.md`、`00-brand-philosophy.md`、`14-brand-governance.md`、`quality/`

## Version
Version: 0.1.0（Draft）
