---
name: enterprise-brand-style-ai-design-system
description: 企業級 AI 品牌設計系統（Enterprise Brand Style AI Design System）的能力路由層。當使用者要產出海報、資訊圖表、工作流程圖、企業架構圖、儀表板、簡報、HTML 頁面、GitHub 文件、Markdown 筆記、社群貼文或 AI 圖像，且需要符合品牌一致性時，必須先用這份文件判斷要載入哪些 docs / templates / tokens / components / prompts / quality / pipelines，再進行產出——不要略過規範直接生成。
---

# SKILL — Capability Routing

## Purpose
作為整套設計系統的入口：把「使用者想產出什麼」對應到「該讀哪些規範、套用哪些 Token 與元件、跑哪一條 Pipeline」。這份文件本身不定義視覺細節，細節一律在 `docs/`、`tokens/`、`components/` 中查找。

## Scope
涵蓋 `templates/` 中列出的所有交付物類型：Poster、Infographic、Workflow、Architecture、Dashboard、Presentation、HTML Page、GitHub README、Markdown Note、Social Post、AI Image、Quality Report、Release Note。

## Routing Table

| 使用者想要的交付物 | Template | 對應 Pipeline | 主要 docs |
|---|---|---|---|
| 資訊圖表 / Carousel 圖卡 | `templates/infographic.template.md` | `pipelines/infographic.pipeline.md` | `03` `05` `07` `09` |
| AI 圖像 / 生圖 Prompt | `templates/ai-image.template.md` | `pipelines/ai-image.pipeline.md` | `08` `09` |
| HTML 頁面 / Artifact / Landing Page | `templates/html-page.template.md` | `pipelines/html-page.pipeline.md` | `05` `06` `10` `13` |
| 儀表板 | `templates/dashboard.template.md` | 待建（見 `15-design-roadmap.md` Phase 2） | `03` `11` `13` |
| 簡報 | `templates/presentation.template.md` | 待建 | `04` `05` `12` |
| 海報 | `templates/poster.template.md` | 待建 | `03` `05` `08` `09` |
| 其餘（Workflow、Architecture、GitHub README、Markdown Note、Social Post、Quality Report、Release Note） | 見 `templates/README.md` | 待建 | 依 `docs/README.md` 對照表 |

「待建」代表目前只有 docs + template，尚未有專屬 pipeline；照 `docs/` 規範與對應 template 手動執行仍然有效，只是還沒有固定好的端到端腳本化流程。

## Standard Routing Procedure

1. **判斷交付物類型**，對照上表找到 template 與 pipeline。
2. **讀取該交付物的 template**（`templates/*.template.md`），依 Metadata / Inputs 向使用者收集內容。
3. **讀取對應 docs**，確認 Principles / Standards / Rules。
4. **套用 `tokens/`**（色彩、字體、間距）與 `components/`（卡片、按鈕、標籤等），不得自行另外配色或發明元件。
5. **若有現成 pipeline**，照 `pipelines/*.pipeline.md` 逐步執行；若「待建」，至少手動走過 Requirement → Template → Tokens/Components → Generation → Quality Review 五步。
6. **產出前查 `quality/`**，用對應 checklist 驗證；沒有 checklist 的交付物類型，至少套用 `quality/quality-gate.md` 的通用關卡。
7. **有使用外部素材（Logo、角色、圖片）時查 `assets/`**，未登錄資產不得直接使用（見 `01-brand-guide.md`、`08-illustration-system.md`）。

## Rules
- 不確定交付物類型時，先問使用者，不要用路由表以外的猜測方式硬套模板。
- Token 與元件是唯一色彩／樣式來源；`docs/03-color-system.md` 明確禁止在文件中散落未登錄 Hex 值，`tokens/` 才是正式來源。
- `tokens/`、`components/`、`assets/` 目前狀態為 **Draft（v0.1.0，待 Owner 核准）**，理由與核准流程見各自 README 與 `14-brand-governance.md`。核准前的產出物應標註為草稿，不視為最終品牌交付物。

## Related Documents
`AGENT.md`、`docs/README.md`、`templates/README.md`、`14-brand-governance.md`

## Version
Version: 0.1.0（Draft — 手動建立，等待完整 bootstrap 套件與 Owner 核准後合併／取代）
