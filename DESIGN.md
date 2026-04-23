# MIYARISAN 妙利散® — Design System

> 版本 1.2 | 品牌：妙利散® / R-CHEVER 裕心 | 領域：醫藥・保健
> 風格定位：日本藥廠美學 × 科學公信力 × 溫暖親近

---

## 1. 品牌定位

| 維度 | 描述 |
|------|------|
| 產品 | 整腸劑・次世代益生菌製劑（CBM588 宮入菌） |
| 原廠 | ミヤリサン製薬株式会社（日本 70+ 年歷史） |
| 台灣代理 | R-CHEVER 裕心 |
| 目標受眾 | 重視品質的成人、家庭主要健康決策者、醫藥專業人員 |
| 品牌調性 | 權威・可信・日系精工・有溫度 |
| 禁忌調性 | 廉價感、過度活潑、誇大或虛假感 |

---

## 2. Logo 系統

### 主 Logo（妙利散®）
- 形態：黑色橢圓藥丸形 + 白字「MIYARISAN」+ 品牌圓形標誌（左上角）
- 中文名：妙利散® — 圓潤日系字體，獨立使用時為白字
- 檔案：
  - `assets/logo-brand.png` — 完整品牌方形版（紅色漸層底）
  - `assets/logo-red.png` — 橢圓標準版（適合白底、深色底）
  - `assets/logo-white.png` — 白字全白版（用於紅底）
  - `assets/logo-white.svg` — 可縮放向量版

### 母公司 Logo（R-CHEVER 裕心）
- 檔案：`assets/logo-rchever.png`
- 深色底使用：`filter: brightness(0) invert(1)`（CSS 反白）

### Logo 使用規則
| 背景色 | 使用版本 |
|--------|----------|
| 白底 `#ffffff` | `logo-red.png`（標準版）+ 建議加紅框或深藍框區隔 |
| 深藍底 `#172F60` | `logo-red.png`（標準版） |
| 深黑底 `#111827` | `logo-red.png`（標準版） |
| 紅底 `#CE0E2D` | `logo-white.png`（白字版） |

**禁止**：拉伸變形、改色、在低對比背景直接疊用、任意添加陰影效果。

---

## 3. 色彩系統

### 品牌主色
| Token | Hex | 用途 |
|-------|-----|------|
| `brand-red` | `#CE0E2D` | 主色・CTA・強調 |
| `brand-navy` | `#172F60` | 展板・深色主題・標題 |

### Red Scale — 紅色階
| Token | Hex | 用途 |
|-------|-----|------|
| `red-dark` | `#a80c24` | Hover 態・壓按態 |
| `red` | `#CE0E2D` | 主色 ✅ |
| `red-light` | `#e83556` | 漸層輔助色 |
| `red-pale` | `#fdf0f2` | 淺色背景・Soft badge 底 |

### Navy Scale — 深藍色階
| Token | Hex | 用途 |
|-------|-----|------|
| `navy-deep` | `#0d2248` | 最深版本 |
| `navy` | `#172F60` | 主深藍 ✅ |
| `navy-mid` | `#1e3d7a` | Hover 態 |
| `navy-light` | `#2a5099` | 圖表・輔助元素 |

### Brand Accent
| Token | Hex | 用途 |
|-------|-----|------|
| `crimson` | `#C8194B` | 特殊強調 |
| `hot-pink` | `#E5186E` | 漸層末端色 |
| `brand-gradient` | `#CE0E2D → #E5186E` | Hero 區塊・品牌漸層（135deg） |

### 中性色
| Token | Hex | 用途 |
|-------|-----|------|
| `text-primary` | `#111827` | 主文字 |
| `text-secondary` | `#374151` | 副標題・說明文 |
| `text-tertiary` | `#6b7280` | 補充資訊 |
| `text-placeholder` | `#9ca3af` | Placeholder・disabled |
| `border` | `#e5e7eb` | 分隔線・框線 |
| `bg-gray-2` | `#f0f2f5` | 次要背景 |
| `bg-gray` | `#f7f8fa` | 頁面背景 |
| `bg-white` | `#ffffff` | 卡片・對話框底色 |

### Semantic 語義色
| Token | Hex | 用途 |
|-------|-----|------|
| `success` | `#16a34a` | 認證通過・成功狀態 |
| `info` | `#2563eb` | 一般資訊 |
| `warning` | `#d97706` | 警示・注意 |
| `danger` | `#dc2626` | 錯誤・危險操作 |

### 深色主題（展板 / Homepage Dark）
- 背景：`#172F60`（Navy）或 `#111827`（深黑）
- 可搭配深藍漸層 + 光球/光暈背景元素（科技醫療感）
- 文字：白色 `#ffffff`（主）、`rgba(255,255,255,0.7)`（副）

---

## 4. 字型系統

### 字型家族

| 字型 | 定位 | 特性 |
|------|------|------|
| **FZLanTingHei（方正蘭亭黑）** | 主字型 — UI、內文、標題 | 幾何理性、乾淨俐落、日系無襯線 |
| **JF Jinxuan（jf 金萱）** | 展示字型 — Hero、Display | 人文溫暖、獨特個性、適合大字輸出 |

### @font-face 宣告

```css
/* ── 方正蘭亭黑 FZLanTingHei ── */
@font-face {
  font-family: 'FZLanTingHei';
  src: url('fonts/fzlt-w200.ttf') format('truetype');
  font-weight: 200; font-style: normal; font-display: swap;
}
@font-face {
  font-family: 'FZLanTingHei';
  src: url('fonts/fzlt-w300.ttf') format('truetype');
  font-weight: 300; font-style: normal; font-display: swap;
}
@font-face {
  font-family: 'FZLanTingHei';
  src: url('fonts/fzlt-w350.ttf') format('truetype');
  font-weight: 350; font-style: normal; font-display: swap;
}
@font-face {
  font-family: 'FZLanTingHei';
  src: url('fonts/fzlt-w400.ttf') format('truetype');
  font-weight: 400; font-style: normal; font-display: swap;
}
@font-face {
  font-family: 'FZLanTingHei';
  src: url('fonts/fzlt-w700.ttf') format('truetype');
  font-weight: 700; font-style: normal; font-display: swap;
}
@font-face {
  font-family: 'FZLanTingHei';
  src: url('fonts/fzlt-w900.ttf') format('truetype');
  font-weight: 900; font-style: normal; font-display: swap;
}

/* ── jf 金萱 JF Jinxuan ── */
@font-face {
  font-family: 'JFJinxuan';
  src: url('fonts/jf-jinxuan-ultralight.otf') format('opentype');
  font-weight: 200; font-style: normal; font-display: swap;
}
@font-face {
  font-family: 'JFJinxuan';
  src: url('fonts/JF-JINXUAN-BOOK.OTF') format('opentype');
  font-weight: 400; font-style: normal; font-display: swap;
}
@font-face {
  font-family: 'JFJinxuan';
  src: url('fonts/JF-JINXUAN-MEDIUM.OTF') format('opentype');
  font-weight: 500; font-style: normal; font-display: swap;
}
@font-face {
  font-family: 'JFJinxuan';
  src: url('fonts/JF-JINXUAN-BOLD.OTF') format('opentype');
  font-weight: 700; font-style: normal; font-display: swap;
}
@font-face {
  font-family: 'JFJinxuan';
  src: url('fonts/jf-jinxuan-heavy.otf') format('opentype');
  font-weight: 900; font-style: normal; font-display: swap;
}
```

### 字型堆疊（CSS Variables）

```css
:root {
  --font-ui:      'FZLanTingHei', 'PingFang TC', 'Noto Sans TC', sans-serif;
  --font-display: 'JFJinxuan', 'FZLanTingHei', 'PingFang TC', sans-serif;
  --font-en:      'Inter', system-ui, sans-serif;
}

body         { font-family: var(--font-ui); }
.hero-title,
.display-text { font-family: var(--font-display); }
.en, .num     { font-family: var(--font-en); }
```

### 字重對照

#### 方正蘭亭黑 FZLanTingHei

| 字重值 | 檔案 | 使用情境 |
|-------|------|---------|
| 200 | `fzlt-w200.ttf` | 極細輕量標注、裝飾文字 |
| 300 | `fzlt-w300.ttf` | 長文副標、說明文字 |
| 350 | `fzlt-w350.ttf` | Body 內文（推薦正文用） |
| 400 | `fzlt-w400.ttf` | UI 標準內文 |
| 700 | `fzlt-w700.ttf` | 標題、Badge、強調 |
| 900 | `fzlt-w900.ttf` | 特粗展示標題、數字統計 |

#### jf 金萱 JF Jinxuan

| 字重值 | 檔案 | 使用情境 |
|-------|------|---------|
| 200 | `jf-jinxuan-ultralight.otf` | 詩意感副標、日系輕標注 |
| 400 | `JF-JINXUAN-BOOK.OTF` | 溫暖內文、引言 |
| 500 | `JF-JINXUAN-MEDIUM.OTF` | 卡片標題、中等強調 |
| 700 | `JF-JINXUAN-BOLD.OTF` | Hero 副標、區塊標題 |
| 900 | `jf-jinxuan-heavy.otf` | Hero 主標、品牌 Display 文字 |

### 字型比例

| 角色 | 尺寸 | 字型 | 字重 | 行高 |
|------|------|------|------|------|
| Hero 主標 | 48–56px | JFJinxuan | 900 | 1.15 |
| Hero 副標 | 20–24px | JFJinxuan | 500 | 1.35 |
| 頁面標題 H1 | 32–40px | FZLanTingHei | 700 | 1.25 |
| 區塊標題 H2 | 24–28px | FZLanTingHei | 700 | 1.3 |
| 卡片標題 H3 | 18–22px | FZLanTingHei | 700 | 1.4 |
| 內文 Body | 16px | FZLanTingHei | 350 | 1.65 |
| 輔助說明 | 14px | FZLanTingHei | 350 | 1.6 |
| 標籤・Badge | 11–13px | FZLanTingHei | 700 | — |
| 數字統計 | 40–56px | FZLanTingHei | 900 | 1.0 |
| Eyebrow | 11px | FZLanTingHei | 700 | — |
| 微標注 | 10–11px | FZLanTingHei | 700 | — |

> **正文推薦用 W350**（`fzlt-w350.ttf`）而非 W400，視覺重量更舒適。

**規則**：
- 最小可讀字體 12px；行動版 Body 不低於 15px
- 中英文混排：英文數字與中文字之間加半形空格
- Letter-spacing：標題 `0.02em`；Badge/Eyebrow `0.08–0.12em`；數字統計 `-0.02em`

---

## 5. 間距系統

採用 **8pt 倍數系統**（基準 8px）：

```
4 / 8 / 12 / 16 / 24 / 32 / 48 / 64 / 96px
```

| 層級 | 值 | 用途 |
|------|----|------|
| xs | 4px | icon 間距、inline gap |
| sm | 8px | badge 內 padding |
| md | 16px | 卡片 padding、段落間距 |
| lg | 24–32px | 區塊間距 |
| xl | 48–64px | Section 間距 |
| 2xl | 96px | Hero padding |

---

## 6. 元件規格

### Badge（固底色標籤）
圓角：`6px`、字體：11.5px / 700 / letter-spacing 0.04em、padding：`4px 12px`

| 樣式 | 背景 | 文字 | 用途 |
|------|------|------|------|
| `badge-red` | `#DC411E` | `#fff` | 藥字號・主要標示 |
| `badge-navy` | `#172F60` | `#fff` | 醫療級・院所通路 |
| `badge-red-soft` | `#fff0ed` | `#DC411E` | 歷史・日期資訊 |
| `badge-navy-soft` | `#eef1f8` | `#172F60` | 日本進口・來源 |
| `badge-green` | `#f0fdf4` | `#16a34a` | 認證通過 |
| `badge-gray` | `#f0f0f4` | `#6b7280` | 一般標籤 |
| `badge-gold` | `linear-gradient(90deg, #D4A832, #F5C842)` | `#fff` | No.1・Premium |

### Pill（外框標籤）
圓角：`99px`、字體：12px / 600 / letter-spacing 0.04em、border：`1.5px solid`、padding：`5px 14px`

| 樣式 | 邊框 / 文字色 | 用途 |
|------|--------------|------|
| `pill-red` | `#DC411E` | 產品分類・功效 |
| `pill-navy` | `#172F60` | 通路・院所 |
| `pill-gray` | `#e0e0e5` / `#6b7280` | 次要分類 |

### Eyebrow 標題眉
```css
display: inline-flex; align-items: center; gap: 8px;
font-size: 11px; font-weight: 700; letter-spacing: 0.1em; text-transform: uppercase;
color: #DC411E;
/* ::before: width 18px, height 2px, background #DC411E, border-radius 2px */
```
用途：區塊標題前置標示（MADE IN JAPAN、臨床研究摘要）

### Live Dot Pill（動態認證標籤）
背景 `#fff0ed`、邊框 `rgba(220,65,30,0.2)`、文字 `#DC411E`、左側 6px 紅色脈衝圓點
用途：醫療級益生菌、藥字號認證等重要訴求標示

### Step Tag（步驟標記）
數字圓圈：30×30px、字體 13px / 700 / Inter
- Red 實底 `#DC411E`
- Navy 實底 `#172F60`
- 空心紅框 outline

---

## 7. 版面原則

### Layout Grid
- 行動版：16px 邊距、單欄
- 平板：24px 邊距
- 桌機：max-width `1200px`，左右自動置中

### 日式醫藥美學核心原則
1. **留白大方**：內容區塊間距充足，不塞滿頁面
2. **文字層次清晰**：主副標題對比強烈，行距舒適
3. **紅白對比為骨架**：主視覺以 Brand Red 為焦點，白色為基底
4. **科學感點綴**：可用圖示化數據（CBM588 菌株圖示、數字統計）
5. **品質感用留白換**：不過度裝飾，精準的細節傳遞可信度

### Hero 區塊
- 背景：白底（一般頁面）或 `#172F60` 深藍（展板、Dark theme）
- 主標：Brand Red 或 White（深色底）
- 搭配產品盒圖，建議右置或中置
- Eyebrow 標籤在標題上方

### 卡片
- 背景：`#ffffff`
- 圓角：`12px`
- 陰影：`0 2px 8px rgba(0,0,0,0.08)`（日系輕陰影）
- 邊框：通常不加；需區隔時用 `1px solid #e5e7eb`

---

## 8. 圖示使用

- 使用向量 SVG 圖示（Lucide Icons 或同風格線條圖示）
- 線條粗細統一 1.5px 或 2px
- **絕對不用 Emoji 作為功能性圖示**
- 互動圖示最小點擊區域 44×44px
- 圖示顏色繼承父元素或明確指定 Brand Red / Navy

---

## 9. 動態 / 互動

| 場景 | 建議 |
|------|------|
| Hover（按鈕） | 背景色深一階（`red-dark #a80c24`）、transition 150ms ease-out |
| 點擊回饋 | Scale 0.97 + opacity 輕微降低、100ms |
| 頁面過場 | Fade + 輕微上移（translateY -4px），200ms ease-out |
| Live dot | 2s pulse（opacity 1↔0.3）|
| 避免 | 超過 400ms 的動畫、純裝飾性動畫 |

---

## 10. Dark Theme（展板 / 深色頁）

| 元素 | 設定 |
|------|------|
| 頁面背景 | `#172F60` 或 `#111827` |
| 主標題 | `#ffffff` |
| 副標題 | `rgba(255,255,255,0.85)` |
| 說明文字 | `rgba(255,255,255,0.65)` |
| 卡片背景 | `rgba(255,255,255,0.08)` + `backdrop-filter: blur(12px)` |
| 卡片邊框 | `rgba(255,255,255,0.15)` |
| 背景裝飾 | 放射狀光球（`radial-gradient`，深藍/青藍色調）|
| Logo | 標準版（`logo-red.png`） |

---

## 11. 禁止清單

- 不改變品牌紅 `#CE0E2D` 的色相（可深/淺，不可變橘或粉）
- 不在淺灰底上直接放灰字（對比不足）
- 不混用不同圓角風格（統一 6px badge、12px 卡片、99px pill）
- 不用多餘的重疊陰影（日系風格保持輕盈）
- 不用誇張字型（圓潤字體本身已有個性，不需再加效果）
- 不用 Emoji 作為圖示
- Logo 不可隨意改色或加效果

---

---

## 13. Button 規格

### 尺寸

| 尺寸 | Padding | 字體 | 高度 | 用途 |
|------|---------|------|------|------|
| `sm` | `8px 16px` | 13px / 600 | 32px | Badge 旁、行內輔助 |
| `md`（預設） | `12px 24px` | 15px / 600 | 44px | 一般 CTA |
| `lg` | `16px 32px` | 16px / 700 | 52px | Hero 主要行動 |

圓角統一：`6px`（同 Badge 風格，不用 pill 圓角）
最小寬度：`120px`（避免過窄）
最小點擊區域：`44×44px`（行動版 touch target 標準）

---

### 樣式

#### Primary（主要行動）
```css
background: #CE0E2D;
color: #ffffff;
border: none;
border-radius: 6px;

/* Hover */
background: #a80c24;
transition: background 150ms ease-out;

/* Active / Pressed */
transform: scale(0.97);
background: #8f0a1e;

/* Disabled */
background: #f0f0f4;
color: #9ca3af;
cursor: not-allowed;
```

#### Secondary（次要行動）
```css
background: #ffffff;
color: #CE0E2D;
border: 1.5px solid #CE0E2D;

/* Hover */
background: #fdf0f2;

/* Disabled */
border-color: #e5e7eb;
color: #9ca3af;
```

#### Ghost — Navy（深色主題）
```css
background: transparent;
color: #172F60;
border: 1.5px solid #172F60;

/* Hover */
background: #eef1f8;
```

#### Text Link Button（文字連結按鈕）
```css
background: transparent;
color: #CE0E2D;
border: none;
padding: 0;
text-decoration: underline;
text-underline-offset: 3px;

/* Hover */
color: #a80c24;
```
> 見截圖 — 卡片底部「OTC 藥品規範」、「醫療通路規範」即為此樣式

#### Icon Button（純圖示）
```css
width: 40px; height: 40px;
border-radius: 6px;
display: flex; align-items: center; justify-content: center;
/* 補 hitSlop / padding 讓實際點擊區達 44px */
```

---

### Dark Theme 按鈕

| 場景 | 樣式 |
|------|------|
| 深藍背景主 CTA | Primary 不變（紅底白字） |
| 深藍背景次要 | `border: 1.5px solid rgba(255,255,255,0.6)` + 白字 |
| 深藍背景 Ghost | `background: rgba(255,255,255,0.1)` + 白字 + hover `rgba(255,255,255,0.2)` |

---

### Button 狀態總表

| 狀態 | 視覺變化 | 時長 |
|------|----------|------|
| Default | — | — |
| Hover | 背景深一階 | 150ms ease-out |
| Active | scale(0.97) | 80ms |
| Loading | 顯示 spinner（16px），禁用點擊，opacity 0.8 | — |
| Disabled | opacity 0.5，cursor not-allowed，不響應 hover | — |
| Success（短暫） | 綠色底 `#16a34a` + ✓ 圖示，1.5s 後恢復 | — |

---

## 14. 響應式斷點系統

### 斷點定義

| Token | 寬度 | 對應裝置 |
|-------|------|----------|
| `xs` | < 375px | 小型手機（少見，兼容用） |
| `sm` | 375px | 標準手機（iPhone SE, 12 mini） |
| `md` | 768px | 平板豎向 |
| `lg` | 1024px | 平板橫向 / 小桌機 |
| `xl` | 1280px | 標準桌機 |
| `2xl` | 1440px | 寬螢幕桌機 |

```css
/* Tailwind / CSS custom properties */
--screen-sm:  375px;
--screen-md:  768px;
--screen-lg:  1024px;
--screen-xl:  1280px;
--screen-2xl: 1440px;
```

---

### Container 寬度

| 斷點 | 內容最大寬 | 左右 padding |
|------|-----------|--------------|
| < 768px | 100% | 16px |
| 768px–1023px | 100% | 24px |
| 1024px–1279px | 960px | 32px |
| ≥ 1280px | 1200px | auto（置中） |

```css
.container {
  width: 100%;
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 16px;
}
@media (min-width: 768px)  { .container { padding: 0 24px; } }
@media (min-width: 1024px) { .container { padding: 0 32px; } }
```

---

### Grid 欄數

| 斷點 | 欄數 | 用途 |
|------|------|------|
| < 768px | 1 欄 | 全寬單欄 |
| 768px | 2 欄 | 卡片兩兩並排 |
| 1024px+ | 3 欄 | 標準三欄（Criteria、Feature 等） |
| 1280px+ | 4 欄 | 統計數據、小卡片格 |

```css
.grid-3 {
  display: grid;
  grid-template-columns: 1fr;
  gap: 24px;
}
@media (min-width: 768px)  { .grid-3 { grid-template-columns: repeat(2, 1fr); } }
@media (min-width: 1024px) { .grid-3 { grid-template-columns: repeat(3, 1fr); } }
```

---

### 字型 — 響應式縮放

| 元素 | Mobile (<768px) | Desktop (≥1024px) |
|------|-----------------|-------------------|
| Hero 主標 | 28–32px | 48–56px |
| 頁面 H1 | 24px | 36px |
| 區塊 H2 | 20px | 28px |
| 卡片 H3 | 18px | 20–22px |
| Body | 15px | 16px |

```css
/* Fluid typography — Hero */
font-size: clamp(28px, 5vw, 56px);
```

---

### Section 間距 — 響應式

| 斷點 | Section 上下 padding | 區塊間 gap |
|------|---------------------|-----------|
| Mobile | 48px | 32px |
| Tablet | 64px | 40px |
| Desktop | 96px | 64px |

---

### 元件行為 — 斷點變化

| 元件 | Mobile | Desktop |
|------|--------|---------|
| Criteria 卡片 | 單欄堆疊，各有獨立邊框 | 三欄共享外框，中間線分隔 |
| Hero | 文字上、圖下（垂直排列） | 左文右圖（水平排列） |
| Nav | Hamburger 選單 | 水平頂部導覽 |
| Badge 群組 | 換行堆疊，gap 8px | 單行水平排列 |
| Button 群組 | 全寬 100% | 自動寬度，inline |

---

## 15. 元件應用模式

### A. Criteria 分隔卡片（共享邊框三欄）

> 源自截圖：「益生菌怎麼選？」區塊

**結構特徵**：
- 三個卡片共用一個外框（不是各自獨立的卡片陰影）
- 中間用垂直 `1px solid #e5e7eb` 分隔，不加額外留白
- 每格內部 padding：32px
- 無背景色差異，全白

```css
.criteria-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  border: 1px solid #e5e7eb;
  border-radius: 12px;
  overflow: hidden;
}
.criteria-card {
  padding: 32px;
  border-right: 1px solid #e5e7eb;
}
.criteria-card:last-child {
  border-right: none;
}
```

**卡片內部結構（從上到下）**：
1. **Step tag**：`CRITERIA 01` — 10–11px / 700 / letter-spacing 0.12em / uppercase / `#6b7280`
2. 間距 16px
3. **卡片標題 H3**：22–24px / 700 / `#111827`
4. 間距 12px
5. **Body 內文**：16px / 400 / `#374151` / line-height 1.65
6. 彈性留白（`flex-grow: 1` 將連結推到底部）
7. **Text Link**：紅色底線文字連結

```html
<div class="criteria-grid">
  <div class="criteria-card">
    <span class="step-label">CRITERIA 01</span>
    <h3>法規合格</h3>
    <p>符合台灣 OTC 醫療級相關規範...</p>
    <a class="text-link">OTC 藥品規範</a>
  </div>
  <!-- × 3 -->
</div>
```

**Mobile 行為**：三欄改為單欄，border-right 移除，改用 `border-bottom` 分隔。

---

### B. Section 標準結構

每個內容區塊的標準層次：

```
[Eyebrow 標題眉]      ← 選用，紅色 uppercase 小標
[H2 主標題]           ← 區塊核心訴求
[副標說明]            ← 選用，14–16px 灰色補充
[主要內容區]          ← 卡片 / 列表 / 圖文
[CTA 按鈕]            ← 選用，Primary 或 Text Link
```

Eyebrow 與 H2 之間間距：8–12px
H2 與副標之間：12px
副標與主內容之間：40–48px

---

### C. Text Link（內文連結）

```css
.text-link {
  color: #CE0E2D;
  text-decoration: underline;
  text-underline-offset: 3px;
  text-decoration-thickness: 1px;
  font-weight: 600;
  font-size: inherit;
  transition: color 120ms ease-out;
}
.text-link:hover {
  color: #a80c24;
}
```

用途：卡片底部延伸連結、內文引用、「了解更多」類連結。

---

### D. Hero 區塊結構

```
[Eyebrow / Live Pill]
[主標題]  ← 最大字，品牌紅或白（深色底）
[副標語]  ← 16–18px，灰或半透明白
[Badge 群組]  ← 信任標籤（藥字號、日本進口、CBM588）
[CTA Button 群組]  ← Primary + Secondary
[產品盒圖]  ← 右置（桌機），下置（手機）
```

---

### E. 數據統計條

用於「70+ 年歷史」「500+ 億活菌」等數字訴求：

```css
.stat-item {
  text-align: center;
}
.stat-number {
  font-family: 'Inter', sans-serif;
  font-size: 40–48px;
  font-weight: 700;
  color: #CE0E2D;   /* 白底時紅字；深色底時白字 */
  letter-spacing: -0.02em;
  font-variant-numeric: tabular-nums;
}
.stat-unit {
  font-size: 20px;
  font-weight: 600;
  color: #CE0E2D;
}
.stat-label {
  font-size: 14px;
  color: #6b7280;
  margin-top: 4px;
}
```

---

### F. Divider（分隔線）

```css
/* 水平分隔 */
border-top: 1px solid #e5e7eb;

/* 有文字的分隔（居中標籤） */
display: flex; align-items: center; gap: 12px;
/* 兩側線段用 flex-grow: 1 的 hr 元素 */

/* 紅色重點分隔（Section 頂部裝飾線） */
width: 40px; height: 3px; background: #CE0E2D; border-radius: 2px;
```

---

### G. 導覽列（Nav）

```
桌機：
[Logo 左置] ─────────────────── [主導覽連結] [CTA Button 右置]
高度：64–72px，背景白，底部 border 1px #e5e7eb

手機：
[Logo 左置] [Hamburger 右置]
展開：全寬 Drawer，連結垂直排列，間距 16px
```

Active 狀態：連結顏色 `#CE0E2D`，可加底線或左側 3px 紅色指示條。

---

## 12. 速查 Cheat Sheet

```
Brand Red:    #CE0E2D   (hover: #a80c24 / active: #8f0a1e)
Brand Navy:   #172F60   (hover: #1e3d7a)
Brand Gradient: 135deg, #CE0E2D → #E5186E

Text:         #111827 / #374151 / #6b7280 / #9ca3af
Border:       #e5e7eb
BG:           #f7f8fa / #f0f2f5 / #ffffff

Font UI:      FZLanTingHei (W350 body / W700 title / W900 display)
Font Display: JFJinxuan (W900 hero / W700 section / W500 card)
Font EN/Num:  Inter

Card:         bg #fff, radius 12px, shadow 0 2px 8px rgba(0,0,0,0.08)
Badge:        radius 6px, padding 4px 12px
Pill:         radius 99px, padding 5px 14px, border 1.5px
Button (md):  padding 12px 24px, radius 6px, min-h 44px
Text Link:    color #CE0E2D, underline, offset 3px

Breakpoints:  sm 375 / md 768 / lg 1024 / xl 1280 / 2xl 1440
Container:    max-width 1200px, padding 16/24/32px
Grid:         1col(mobile) → 2col(768) → 3col(1024)
Section gap:  48px(mobile) → 64px(tablet) → 96px(desktop)
```
