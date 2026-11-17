Debby *Huang*

個人品牌識別規範 v1.0。取自履歷網站的實際 CSS，並把對比度不足的地方修正成可直接使用的版本。

[Wordmark](#wordmark)[色彩](#color)[對比度](#contrast)[字型](#type)[形狀與動態](#shape)[用法與禁忌](#rules)[Tokens](#tokens)

## Wordmark

不另做 Logo，姓名本身就是標誌。名字用黑，姓氏用金色斜體，這個對比就是識別。

Debby *Huang*

Debby *Huang*

### 規格

字型 Playfair Display 700，姓氏改為 600 斜體。\
最小尺寸：螢幕高度 20px、列印 8mm。\
淺底用 `#0f172a` 搭 `#C8A96E`；深底用白搭 `#C8A96E`。

### 安全間距

Debby *Huang*

四邊至少留一個大寫 H 的高度。

### 金色在 Wordmark 上可以用

Wordmark 是大字，金色對比度只需 3:1。在深底上為 8.0:1，在淺底上約 2.1:1，所以淺底使用時字級要在 24px 以上，小於這個尺寸改用單色深藍版本。

## 色彩

橄欖綠是主色，金色是點綴，深藍黑負責文字與重量。這不是「深藍＋金」，而是「橄欖＋金」，深色只是承載。

**Olive**`#6B7C45`\
主色。圖形、線條、大按鈕底色

**Olive text 新增**`#5A6B36`\
橄欖綠的小字版本

**Olive dark**`#3a4724`\
引言、公司名、標籤文字

**Olive light**`#8A9E5A`\
漸層起點、深底上的綠

**Gold**`#C8A96E`\
點綴。姓氏、線條、大數字、✦

**Gold text 新增**`#8A6A2A`\
淺底上的金色小字

**Ink**`#0f172a`\
標題、主按鈕、深色區塊

**Muted**`#475569`\
內文、副標

**Paper**`#f8fafc`\
頁面底色

### 使用比例

Paper 60 Ink 28 9

金色每頁最多 1 到 2 處。用得越少越貴。

## 對比度

依 WCAG 2.1 計算，一般文字需 4.5:1，大字（24px 以上或 19px 粗體）需 3:1。比值為約略值。

| 前景 / 背景 | 樣本 | 比值 | 判定 |
| --- | --- | --- | --- |
| Ink on Paper | 標題 Aa | 17.1 | 通過 |
| Muted on Paper | 內文 Aa | 7.3 | 通過 |
| Olive on Paper | 小字 Aa | 4.4 | 小字差一點 |
| **Olive text on Paper** | 小字 Aa | 5.6 | 修正後通過 |
| Olive dark on Paper | 標籤 Aa | 9.5 | 通過 |
| Gold on Paper | 小字 Aa | 2.1 | 不通過 |
| **Gold text on Paper** | 小字 Aa | 4.8 | 修正後通過 |
| Gold on Ink | 深底 Aa | 8.0 | 通過 |
| White on Olive（按鈕） | 按鈕 Aa | 4.6 | 勉強通過 |

### 修正規則

原站的區塊小標（0.8rem）與時間（0.85rem）使用 `#C8A96E`，在淺底上約 2.1:1，要改成 `#8A6A2A`。橄欖綠小字（hero-tag、nav hover）改用 `#5A6B36`。金色原色保留給 Wordmark 姓氏、大數字、線條與 ✦，以及所有深色底。

## 字型

襯線負責個性，無襯線負責閱讀。中文必須明確指定，不能落到系統預設字。

標題、數字、Wordmark

Playfair 品牌行銷

Playfair Display 400 / 600 / 700 / 斜體\
中文搭配 Noto Serif TC 600 / 700

內文、標籤、按鈕

Inter 讓顧客一見鍾情，進而建立長久關係。

Inter 400 / 500 / 600\
中文搭配 Noto Sans TC 400 / 500 / 700

### 字級

Hero 姓名clamp(3rem, 5vw, 4.5rem)

區塊標題2.5rem

專案標題1.45rem

內文與說明0.95–1.05rem，行高 1.6–1.75

標籤與小註解0.75–0.85rem，最小 12px

### Font stack

```
--font-serif: 'Playfair Display', 'Noto Serif TC', serif;
--font-sans:  'Inter', 'Noto Sans TC', system-ui, sans-serif;
```

## 形狀與動態

### 形狀

卡片 24px\
膠囊按鈕與標籤 2rem\
成果列 16px\
Hero 照片拱形 `120px 120px 16px 16px`

### 間距

容器最大寬 1200px，左右 2rem\
區塊上下 8rem\
技能格 1.5rem，專案格 2.5rem\
響應式斷點 900px

### 陰影

靜止：`0 4px 20px rgba(0,0,0,.03)`\
hover：`0 24px 48px rgba(0,0,0,.08)`\
只用極輕陰影，不用色彩陰影。

### 動態

緩動 `cubic-bezier(.16,1,.3,1)`，0.3–0.4s\
只有可點擊的元件才上浮。\
需支援 `prefers-reduced-motion`。

## 用法與禁忌

這樣用：小字用深一階

Project showcase

代表專案

淺底上的金色小字一律用 Gold text。

不要：淺底上用原色金做小字

Project showcase

代表專案

對比度只有 2.1:1，列印後幾乎看不見。

這樣用：金色只當點綴

500 人到場

一個大數字配一條金線，其餘留白。

不要：金色鋪滿整區

500 人到場

金色大面積使用會失去點綴的價值，也變得廉價。

這樣用：分類標籤用品牌色

活動企劃

標籤底用橄欖綠 12%，字用 Olive dark。

不要：用狀態綠點或其他品牌色

活動企劃

亮綠圓點像「線上中」，且不在色票內。川鋼與 ECOCO 的品牌色也不要混進來。

### Wordmark 禁忌

- 不拉伸、不加外框或陰影、不改字型。
- 姓氏不換成橄欖綠或其他顏色，也不改成正體。
- 放在雜亂照片上時，先加深色遮罩，再使用深底版本。
- 不與 ECOCO 或川鋼的標誌並排排版，避免讀成合作品牌。

## Design tokens

複製到網站 CSS 的 `:root`，簡報與 PDF 範本也用同一份色碼。

```
:root {
  /* brand */
  --olive: #6B7C45;
  --olive-light: #8A9E5A;
  --olive-dark: #3a4724;
  --olive-text: #5A6B36;   /* 小字用 */
  --accent: #C8A96E;       /* 大字、線條、深底 */
  --accent-text: #8A6A2A;  /* 淺底小字用 */
  --ink: #0f172a;
  --muted: #475569;
  --bg: #f8fafc;
  /* type */
  --font-serif: 'Playfair Display', 'Noto Serif TC', serif;
  --font-sans: 'Inter', 'Noto Sans TC', system-ui, sans-serif;
  /* shape */
  --radius-card: 24px;
  --radius-pill: 2rem;
  --ease: cubic-bezier(.16, 1, .3, 1);
}
```

Debby *Huang*｜個人品牌識別規範 v1.0。色碼取自履歷網站原始碼，標示「新增」者為對比度修正版本。