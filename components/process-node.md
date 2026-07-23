# Component: Process Node

## Purpose
表達工作流程、步驟或架構圖中的一個節點，用於 Workflow、Architecture 與 Presentation 類交付物（例如「Think → Organize → Create → Automate → Build → Improve」這種流程圖）。

## Required Content
- 步驟編號或順序指示（僅在內容本身確實是有順序的流程時才使用，見下方 Rules）
- 節點標題
- 一行說明

## Optional Content
- icon
- 連接箭頭／線條至下一個節點
- 分支條件文字

## Sizes / Variants
| 變體 | 用途 |
|---|---|
| `node--linear` | 線性流程（單一路徑，如 Think→Organize→Create） |
| `node--branch` | 有條件分支的節點 |
| `node--layer` | 架構圖裡的分層節點（Frontend / API / Model / Database…），不強調順序，強調層級 |

## States
`default`；若用於互動式流程圖，需要 `active`（目前所在步驟）與 `completed`。

## Tokens Used
`--card-bg`、`--card-border`、`--radius-lg`、`--color-brand-primary`（節點編號圈）、`--gradient-divider`（節點間連接線，僅裝飾用途）

## Accessibility
- 節點順序需在 DOM 順序中與視覺順序一致，不得只靠絕對定位排列而打亂閱讀順序。
- 連接箭頭若只用圖片／SVG 表達「接下來」的意思，需要有文字順序作為替代（例如清單標記的 1. 2. 3.）。

## Prohibited Usage
- **不得為了「看起來像流程」而幫非順序性的內容加上編號**——依 `../docs/06-component-system.md` 的原則精神與一般設計實務，數字徽章（01/02/03）只在內容本身確實是流程、時間序或步驟時才使用；純分類或並列資訊不應加編號製造假流程感。
- 不得讓節點的視覺分支數量超過內容實際的邏輯分支數量。

## Example
```html
<ol class="process">
  <li class="node--linear">
    <span class="node-index" aria-hidden="true">1</span>
    <h3>Think</h3>
    <p>Research ideas and solve problems</p>
  </li>
  <li class="node--linear">
    <span class="node-index" aria-hidden="true">2</span>
    <h3>Organize</h3>
    <p>Store notes, sources, and summaries</p>
  </li>
</ol>
```

## Related Documents
`../docs/02-design-language.md`、`../docs/06-component-system.md`、`../templates/workflow.template.md`

## Version
Version: 0.1.0 (Draft)
