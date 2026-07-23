# Pipelines

## Purpose
把 `docs/` + `templates/` + `tokens/` + `components/` + `prompts/` + `quality/` 串成可重複執行的端到端流程，對應根目錄 `README.md` 的 Production Flow：

```
Requirement → Planning → Pipeline Selection → Prompt → Template
→ Components → Tokens → Assets → Generation → Quality Review
→ Revision → Release
```

## Status
Draft — v0.1.0。目前只完成三條交付物類型的 Pipeline（AI Image、HTML Page、Infographic），其餘見 `../docs/15-design-roadmap.md` Phase 2。

## Files
| Pipeline | 交付物類型 |
|---|---|
| `ai-image.pipeline.md` | AI 圖像生成 |
| `html-page.pipeline.md` | HTML 頁面／Artifact |
| `infographic.pipeline.md` | 資訊圖表／Carousel |

## Related Documents
`../SKILL.md`（Routing Table）、`../AGENT.md`、`../docs/15-design-roadmap.md`

## Version
Version: 0.1.0 (Draft)
