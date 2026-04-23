# MIYARISAN 妙利散® — Design System

> 版本 1.0 | 品牌：妙利散® / R-CHEVER 裕心 | 領域：醫藥・保健
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

### 主要字型
| 角色 | 字型 | 備用 |
|------|------|------|
| 中文內文・標題 | FZLanTingHei（方正蘭亭黑） | PingFang TC, Noto Sans TC |
| 英文 UI・數字 | Inter | system-ui, sans-serif |

```css
font-family: 'FZLanTingHei', 'PingFang TC', 'Noto Sans TC', sans-serif;
font-family: 'Inter', system-ui, sans-serif; /* 英文數字 */
```

### 字型比例
| 角色 | 尺寸 | 字重 | 行高 |
|------|------|------|------|
| Hero 主標 | 40–56px | 700 | 1.2 |
| 頁面標題 H1 | 32px | 700 | 1.3 |
| 區塊標題 H2 | 24px | 700 | 1.35 |
| 卡片標題 H3 | 18–20px | 600 | 1.4 |
| 內文 Body | 16px | 400 | 1.65 |
| 輔助說明 | 14px | 400 | 1.6 |
| 標籤・Badge | 11–13px | 600–700 | — |
| 微標注 | 10–11px | 700 | — |

**規則**：
- 最小可讀字體 12px；行動版 Body 不低於 16px
- 中英文混排：英文數字與中文字之間加半形空格
- Letter-spacing：標題 `0.02em`；Badge/Eyebrow `0.08–0.12em`

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

## 12. 速查 Cheat Sheet

```
Brand Red:    #CE0E2D   (hover: #a80c24)
Brand Navy:   #172F60   (hover: #1e3d7a)
Brand Gradient: 135deg, #CE0E2D → #E5186E

Text:         #111827 / #374151 / #6b7280 / #9ca3af
Border:       #e5e7eb
BG:           #f7f8fa / #f0f2f5 / #ffffff

Font CN:      FZLanTingHei, PingFang TC, Noto Sans TC
Font EN/Num:  Inter

Card:         bg #fff, radius 12px, shadow 0 2px 8px rgba(0,0,0,0.08)
Badge:        radius 6px, padding 4px 12px
Pill:         radius 99px, padding 5px 14px, border 1.5px
```
