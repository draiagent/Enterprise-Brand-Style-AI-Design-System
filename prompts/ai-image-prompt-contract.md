# Prompt: AI Image Prompt Contract

實作 `../docs/09-image-prompt-system.md` 的八段式 Prompt Contract。填空後即可交給生圖工具（例如 gpt-image-2）執行。

## 1. Objective
```
用途：{{這張圖用在哪裡，例如「Instagram/LinkedIn carousel 第 N 張」}}
成功條件：{{例如「讀者 3 秒內看懂這一頁在講什麼」}}
```

## 2. Canvas
```
比例：{{1:1 / 3:4 / 4:5 / 9:16 / 16:9，見 tokens/spacing.tokens.md 的 Grid 段落}}
方向：{{直式／橫式／方形}}
輸出尺寸：{{實際會用的生圖工具支援的尺寸，例如 gpt-image-2 僅支援 1024x1024/1536x1024/1024x1536，選最接近 Canvas 比例的一個}}
```

## 3. Audience
```
受眾：{{例如「正在評估 AI 工具的知識工作者」}}
情境：{{例如「在 LinkedIn 上滑動瀏覽時停下來看的第一眼」}}
```

## 4. Content Hierarchy
```
標題：{{主標題}}
副標：{{一句話說明}}
重點內容：{{逐項列出，例如卡片清單、步驟}}
CTA：{{行動呼籲文字}}
Logo／品牌標示位置：{{若需要放品牌識別，說明位置與哪個核准版本，見 assets/}}
```

## 5. Visual Direction
```
風格：Modern UI, Apple + OpenAI + Notion + Canva 混合感, 3D Flat Illustration icon, Soft Neumorphism, Card UI
材質：白底、卡片式圓角陰影、玻璃擬物化
鏡頭／視角：icon 需同一系列、同一透視角、同一光源、同一陰影（見 docs/07-icon-system.md）
背景：白底大留白、幾何點陣、漸層光暈、sparkles，裝飾保持節制
```

## 6. Brand Constraints
```
色彩（引用 tokens/color.tokens.md，Draft 狀態）：
  主標題漸層：--color-brand-primary → --color-brand-accent（藍 → 青綠）
  Automation 類內容：--color-brand-automate（紫）
  Create 類內容：--color-brand-create（橘）
CTA 按鈕：--gradient-cta（藍 → 紫），白字，pill 形狀
字體調性：超粗大標、一般粗副標、Regular 內文（對應 tokens/typography.tokens.md 的 Roles）
安全距離：Logo／品牌標示需保留最小安全距離（Logo 高度 25%，見 docs/01-brand-guide.md），本 Prompt Contract 不生成 Logo 本體
```

## 7. Negative Constraints
```
- 不生成或模擬任何 Logo、真實品牌商標、真人肖像
- 不在圖片內生成大段精確繁體中文——重要文字後製排版（見 docs/09-image-prompt-system.md Rules）
- 不加入浮水印、QR Code、額外未要求的人物
- 不使用會與內容競爭注意力的雜亂背景
- 不使用色彩以外無法辨識的狀態提示（例如只用顏色區分對錯）
```

## 8. Quality Checks
```
- 繁體中文文字（若有後製）需逐字校對
- 構圖是否符合 Canvas 比例與安全區（tokens/spacing.tokens.md）
- 是否符合 Brand Constraints 的色彩與字體調性
- 是否誤植真實品牌 Logo 或造成品牌混淆
- 對照 quality/checklist-ai-image.md 逐項確認
```

## Traceability
依 `../docs/09-image-prompt-system.md`：Prompt 版本、使用模型、參考圖與輸出需可追蹤。建議在 `../examples/` 或交付物旁附上：
```yaml
prompt_version: 0.1.0
model: gpt-image-2
reference_images: []
output_status: draft   # draft | approved
```

## Related Documents
`../docs/09-image-prompt-system.md`、`../docs/08-illustration-system.md`、`../templates/ai-image.template.md`、`../tokens/`

## Version
Version: 0.1.0 (Draft)
