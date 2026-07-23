# Prompts

## Purpose
提供可重複使用、可稽核的 Prompt 範本，實作 `../docs/09-image-prompt-system.md` 定義的 Prompt Contract，避免每次生成 AI 圖像或 AI 輔助文件時重新發明結構。

## Status
Draft — v0.1.0。

## Files
| 檔案 | 用途 |
|---|---|
| `ai-image-prompt-contract.md` | AI 圖像生成的八段式 Prompt Contract，套用 `../tokens/` 作為 Brand Constraints |

## Usage
1. 複製 `ai-image-prompt-contract.md` 的八個段落結構。
2. 依 `../templates/ai-image.template.md` 收集的 Inputs 填入 Objective / Canvas / Audience / Content Hierarchy。
3. Visual Direction 與 Brand Constraints 段落直接引用 `../tokens/color.tokens.md`、`../tokens/typography.tokens.md`，不要自己重新配色。
4. 组好的 prompt 連同版本、使用的模型與參考圖記錄下來（見 `../docs/09-image-prompt-system.md` 的可追蹤性要求），實務上可存放在 `../examples/` 或交付物本身的版本紀錄中。

## Related Documents
`../docs/09-image-prompt-system.md`、`../templates/ai-image.template.md`、`../tokens/`

## Version
Version: 0.1.0 (Draft)
