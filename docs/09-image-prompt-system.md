# 09 — AI Image Prompt System

## Purpose
建立可控、可重複、可稽核的 AI 圖像生成提示詞規範。

## Scope
適用於海報、資訊圖、角色、場景、背景、概念圖與既有圖片編修。

## Principles
Prompt 應先描述任務、訊息和版面，再描述風格；品牌資產與精確文字由正式來源控制。

## Prompt Contract
1. **Objective**：用途與成功條件。
2. **Canvas**：比例、方向、輸出尺寸。
3. **Audience**：受眾與情境。
4. **Content Hierarchy**：標題、重點、CTA、Logo 位置。
5. **Visual Direction**：風格、材質、鏡頭、光線、背景。
6. **Brand Constraints**：色彩、角色、Logo、安全距離。
7. **Negative Constraints**：禁止錯字、浮水印、額外人物、錯誤 Logo、雜亂背景。
8. **Quality Checks**：繁體中文、構圖、可讀性與事實。

## Rules
- 重要繁體中文應後製排版，不依賴模型一次生成正確。
- 編修圖片必須明確指出保留與修改項目。
- 未取得目標圖像時不得假定已存在。
- Prompt 版本、模型、參考圖與輸出需可追蹤。

## Validation
使用 `quality/` 檢查品牌一致、文字正確、構圖、比例、資產與不必要新增內容。

## Related Documents
`prompts/`、`08-illustration-system.md`、`03-color-system.md`、`05-layout-grid.md`

## Version
Version: 1.0.0