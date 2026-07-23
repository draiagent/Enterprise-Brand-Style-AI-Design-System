# Changelog

依 `docs/14-brand-governance.md` 的 Change Classes 記錄（Patch / Minor / Major）。

## 0.1.0 — Draft Foundation Layers (Minor)
- 新增 `SKILL.md`、`AGENT.md` 作為能力路由與決策政策層。
- 新增 `tokens/`：色彩、字體、間距（Draft，待 Owner 核准實際 Hex 值與字族）。
- 新增 `components/`：Card、Button、Badge、Callout、Nav、Table、Chart Container、Process Node 的元件規格。
- 新增 `prompts/`：AI 圖像 Prompt Contract。
- 新增 `assets/`：資產登錄規格（目前登錄為空）。
- 新增 `examples/`：一組草稿參考範例（AI Assistants 資訊卡）。
- 新增 `quality/`：通用品質關卡與三份交付物類型的檢查清單（AI Image、HTML Page、Infographic）。
- 新增 `pipelines/`：AI Image、HTML Page、Infographic 三條端到端流程。

此版本為手動建立的第一版基礎骨架，對應 `.bootstrap/` 中尚未觸發解壓縮的完整套件；待該套件正式展開後，需要人工比對、合併或取代本版本內容，不應假設兩者已自動同步。

## Unreleased
- `.bootstrap/` 套件解壓縮與正式版 tokens/components 合併。
- Poster、Dashboard、Presentation 等其餘交付物類型的 pipeline。
