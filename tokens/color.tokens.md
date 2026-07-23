# Color Tokens

Status: **Draft — v0.1.0，待 Owner 核准**（估色來源見 `README.md`）。

依 `../docs/03-color-system.md` 的三層架構：Primitive → Semantic → Component。上層只能引用下層，不得跳過 Semantic 直接在元件裡寫 Hex。

## 1. Primitive

原始色階，不直接承載語意。

```css
:root {
  /* Blue */
  --primitive-blue-50:  #eff6ff;
  --primitive-blue-500: #2563eb;
  --primitive-blue-700: #1d4ed8;

  /* Teal */
  --primitive-teal-50:  #f0fdfa;
  --primitive-teal-500: #14b8a6;
  --primitive-teal-700: #0f766e;

  /* Purple */
  --primitive-purple-50:  #f5f3ff;
  --primitive-purple-500: #7c3aed;
  --primitive-purple-700: #6d28d9;

  /* Orange */
  --primitive-orange-50:  #fff7ed;
  --primitive-orange-500: #f97316;
  --primitive-orange-700: #c2410c;

  /* Neutral */
  --primitive-navy-900:  #0f172a;
  --primitive-gray-600:  #4b5563;
  --primitive-gray-200:  #e5e7eb;
  --primitive-gray-50:   #f8fafc;
  --primitive-white:     #ffffff;

  /* Status primitives */
  --primitive-green-600: #16a34a;
  --primitive-amber-500: #f59e0b;
  --primitive-red-600:   #dc2626;
  --primitive-sky-600:   #0284c7;
}
```

## 2. Semantic

給元件與模板使用的語意層。**分類色（brand-*）與狀態色（success/warning/danger/info）不得互換語意**——分類色是「這是哪一種內容」，狀態色是「這件事現在是什麼狀態」，兩者是不同的判斷維度（見 `../docs/03-color-system.md` 的 Rules）。

```css
:root {
  /* 品牌／分類色：對應資訊圖範例裡「Automation=紫、Create=橘」這種分類用法 */
  --color-brand-primary:   var(--primitive-blue-500);   /* 主標題、主要行動 */
  --color-brand-accent:    var(--primitive-teal-500);   /* 強調、次要重點 */
  --color-brand-automate:  var(--primitive-purple-500); /* Automation 類內容 */
  --color-brand-create:    var(--primitive-orange-500); /* Create 類內容 */

  /* 背景與表面 */
  --color-background: var(--primitive-white);
  --color-page-bg:     var(--primitive-gray-50);
  --color-surface:     var(--primitive-white);
  --color-border:      var(--primitive-gray-200);

  /* 文字 */
  --color-text:           var(--primitive-navy-900);
  --color-text-secondary: var(--primitive-gray-600);
  --color-text-on-brand:  var(--primitive-white);

  /* 狀態色：只用於表達狀態，不作分類使用 */
  --color-success: var(--primitive-green-600);
  --color-warning: var(--primitive-amber-500);
  --color-danger:  var(--primitive-red-600);
  --color-info:    var(--primitive-sky-600);

  /* 漸層（僅用於裝飾性標題／CTA，不承載精確數值判讀，符合 03 的 Rules） */
  --gradient-heading: linear-gradient(90deg, var(--color-brand-primary), var(--color-brand-accent));
  --gradient-cta:     linear-gradient(90deg, var(--color-brand-primary), var(--color-brand-automate));
  --gradient-divider: linear-gradient(90deg, var(--color-brand-automate), var(--color-brand-primary), var(--color-brand-accent), var(--color-brand-create));
}
```

## 3. Component

元件專用 Token，引用 Semantic 層，不直接引用 Primitive。

```css
:root {
  --card-bg:            var(--color-surface);
  --card-border:        var(--color-border);
  --card-shadow:        0 4px 20px rgba(15, 23, 42, 0.08);
  --card-shadow-hover:  0 10px 28px rgba(15, 23, 42, 0.13);

  --button-cta-bg:    var(--gradient-cta);
  --button-cta-text:  var(--color-text-on-brand);

  --badge-border: var(--color-brand-accent);
  --badge-text:   var(--color-brand-accent);

  --chart-categorical-1: var(--color-brand-primary);
  --chart-categorical-2: var(--color-brand-accent);
  --chart-categorical-3: var(--color-brand-automate);
  --chart-categorical-4: var(--color-brand-create);
  --chart-categorical-5: var(--primitive-gray-600); /* 第五分類色，超過五類時改用表格，見 11-dashboard-design-standard.md */
}
```

## Dark Mode

依 `../components/README.md` 的通用規則：深色模式只換 Semantic 層的背景／文字／陰影，品牌與狀態色的 Primitive 值不變，以維持跨主題辨識度。

```css
@media (prefers-color-scheme: dark) {
  :root {
    --color-text:           #f1f5f9;
    --color-text-secondary: #94a3b8;
    --color-background:     #0b1220;
    --color-page-bg:        #0b1220;
    --color-surface:        #17212f;
    --color-border:         #293548;
    --card-shadow:          0 4px 24px rgba(0, 0, 0, 0.45);
    --card-shadow-hover:    0 10px 32px rgba(0, 0, 0, 0.55);
  }
}
```

## Accessibility Notes
依 `../docs/13-accessibility-standard.md`：一般文字對比需達 4.5:1，大字至少 3:1。`--color-text` 在 `--color-background` 上、`--button-cta-text` 在 `--button-cta-bg` 漸層最深處，都需要在核准前實測對比，目前僅為估值，尚未跑過對比檢查。

## Related Documents
`../docs/03-color-system.md`、`../docs/11-dashboard-design-standard.md`、`../docs/13-accessibility-standard.md`

## Version
Version: 0.1.0 (Draft)
