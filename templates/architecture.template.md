# Architecture Template

## Metadata
- System Name:
- Owner:
- Version: 1.0.0
- Scope:
- Audience:

## Purpose
以一致方式表達系統分層、模組責任、資料流與治理邊界。

## Inputs
- 業務目標：
- 使用者角色：
- 核心模組：
- 外部依賴：
- 安全要求：

## Outputs
- 架構圖
- 模組責任表
- 資料流說明
- 風險與控制點

## Required Sections
1. Context
2. Layers
3. Components
4. Interfaces
5. Data Flow
6. Security and Governance
7. Observability

## Optional Sections
- 部署拓撲
- 模型路由
- RAG 與記憶
- 成本與容量

## Validation Rules
- 每個模組有明確責任與介面。
- 箭頭需標示資料或控制流向。
- 避免同一概念重複出現在多層。
- 安全、權限、日誌與評估不得省略。

## Example
```text
Interface → Orchestrator → Agent/Skill → Model Gateway → Knowledge/Data → Quality/Governance
```
