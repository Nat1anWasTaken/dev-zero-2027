# SITCON 2027 Slidev 主題

這是一套可獨立使用的主題，設計依循 [SITCON 2027 網站](https://sitcon.org/2027/)：採用 LINE Seed TW 字體、暖白紙張與霧灰表面、近黑色封面、螢光黃綠章節分隔，以及細線元素。參考資料最後確認於 2026 年 9 月。

## 重複使用

將整個目錄複製到另一個 Slidev 專案：

```yaml
---
theme: ./theme
layout: cover
title: 我的簡報
themeConfig:
  brand: SITCON
  year: '2027'
  footer: 學生計算機年會
  showPageNumber: true
---
```

不需從父簡報、同層網站或遠端字型服務載入任何資源。主題已內含完整繁體中文字型；Vite 會在部署至基礎路徑時正確解析其網址。

若要以套件形式發佈，請在此目錄執行 `npm pack`，並在使用此主題的專案安裝產生的壓縮檔。接著設定 `theme: sitcon-2027`。是否發佈至套件庫可自行決定。

## 版面配置

| 版面配置 | 用途／插槽 |
| --- | --- |
| `cover`、`intro`、`end` | 深色背景上的大標題與輔助文字 |
| `default` | 標題、內文、清單、程式碼與表格 |
| `section` | 螢光黃綠章節分隔頁 |
| `center` | 垂直置中的內容 |
| `statement` | 深色背景上的大型陳述 |
| `quote` | 霧灰背景上的 Markdown 引文 |
| `fact` | 螢光黃綠背景上的大型數字或短句 |
| `two-cols` | 預設／左欄內容，以及 `::right::` |
| `two-cols-header` | 預設內容或 `::header::`、`::left::`、`::right::`、`::bottom::` |
| `image-left`、`image-right` | 文字搭配圖片 |
| `image` | 圖片填滿內容區域，可選擇疊加文字 |
| `full` | 無框架，保留 24px 邊距 |
| `none` | 無框架與邊距 |

其他 Slidev 版面配置會保留其內建實作。

## 單頁選項

```yaml
layout: two-cols-header
tone: mist # paper（紙白）| mist（霧灰）| dark（深色）| acid（螢光黃綠）
eyebrow: 01 / 開發組
label: 架構
footer: false # 隱藏頁尾；填入字串可覆寫頁尾文字
layoutClass: gap-12 # 欄位格線工具類別
```

所有含框架的版面配置都接受 `background`、`backgroundSize` 與 `backgroundPosition`。搭配背景照片時，請使用 `tone: dark`；主題會降低照片亮度以確保可讀性。

圖片版面配置接受 `image`、`alt`、`caption`、`backgroundSize: cover | contain` 與 `backgroundPosition`。請將簡報圖片放在使用此主題的專案 `public/` 目錄，並以斜線開頭的路徑參照。圖片網址會遵循 Slidev 的部署基礎路徑。

```md
---
layout: image-right
image: /photos/community.webp
alt: 社群活動的參與者
caption: 圖片來源
backgroundPosition: 60% center
---

# 標題

輔助文字。
```

欄位版面配置會保留 Slidev 的 `class` 與 `layoutClass` 屬性。一般投影片的類別與樣式會經由共用框架傳遞。`center` 會垂直置中；若要水平置中，請加入 `class: text-center`。

## 結構與自訂方式

- `styles/tokens.css`：公開的色彩、字型與間距變數，以及表面變體。
- `styles/typography.css`：排版、Markdown 元素與文字輔助類別。
- `styles/layouts.css`：框架間距與版面組合。
- `components/SitconFrame.vue`：共用外框、品牌、背景與頁尾。
- `components/SitconColumns.vue`、`SitconImage.vue`：共用版面組合。
- `layouts/`：精簡且具名稱的 Slidev 進入點。
- `assets/fonts/`：完整繁體中文字型與其授權。

可在使用此主題的簡報 `style.css` 覆寫設計變數：

```css
:root {
  --sitcon-acid: #d9ff65;
  --sitcon-space-x: 48px;
  --sitcon-column-gap: 32px;
}
```

`--sitcon-*` 變數是公開的樣式介面。CSS 限定於 `.sitcon-frame`，避免影響簡報者控制項。次要文字可使用 `sitcon-muted` 與 `sitcon-caption`。

此主題的目標尺寸為 Slidev 980px 畫布寬度下的 16:9 投影片；內容溢出時不會自動縮小。

## 資源

LINE Seed TW © LY Corporation，依 SIL OFL 1.1 發佈；詳見 `assets/fonts/OFL.txt` 與 [LINE Seed](https://seed.line.me/index_tw.html)。內含的 Regular 與 ExtraBold 檔案，是 SITCON 2027 網站使用的完整 WOFF2 字型，而非頁面專用子集。

本主題以文字呈現品牌識別。此儲存庫另附的示範照片不包含在主題套件中。
