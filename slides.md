---
theme: ./theme
title: SITCON 2027 開發組零籌
info: SITCON 2027 開發組第一次籌備會議
layout: cover
footer: false
drawings:
  persist: false
comark: true
duration: 35min
---

# SITCON 2027<br>開發組零籌

---
layout: intro
---

# 這場會的目的

- 熟悉彼此
- 再介紹一次開發組的工作內容
- 收集各位的興趣
- 約每週同步會議時間

<!--
歡迎大家加入今年的開發組！今天先互相認識，再介紹工具、工作內容和分工，最後一起約固定會議時間。
-->

---
layout: default
---

# 自我介紹

- 平常主要玩什麼技術？
- 最愛或最熟悉的語言、框架？
- 還有什麼想讓大家知道的事？

<!--
輪流自我介紹。技術可以是網頁前後端、Mobile App、ML、資安、競程，都歡迎聊聊。
-->

---
layout: image-right
image: /images/wolf-avatar.jpg
alt: Wolf 的 Gravatar 頭像
backgroundSize: contain
---

# 小幫手！Wolf

- 因為組長 Nathan 今年也是年會副召
- Wolf 會是我們的小幫手
- 會幫忙一起追進度！

<!--
因為你們的組長同時也是今年年會的副召，所以請 Wolf 擔任開發組小幫手，一起追進度。
頭像來源：Gravatar，使用 me@wolf-yuan.dev 對應的頭像，擷取於 2026-09-14。
-->

---
layout: default
---

# 關於開發組

- 主要負責網站與 App 的開發
- 大多數專案會由其他組提供設計稿與 spec，我們負責實作

<!--
相比活動、議程、設計等比較需要創意的組，開發組更多在做的是「執行」。
主要工作幾乎都會有別組做好設計稿、開好 spec 給我們，我們負責把它實作出來。
-->

---
layout: two-cols-header
---

# 常用工具

::left::

## GitLab

<img src="/images/gitlab-work-items.png" alt="SITCON GitLab 工作項目畫面" class="tool-shot" />

::right::

## GitHub

<img src="/images/github.png" alt="SITCON GitHub 組織畫面" class="tool-shot" />

<style>
.tool-shot { width: 100%; height: 255px; object-fit: contain; object-position: top; }
</style>

<!--
介紹開發組常用的兩個工具，搭配畫面帶大家認識。
圖片使用專案既有素材：public/images/gitlab-work-items.png、public/images/github.png。
-->

---
layout: center
---

# 在會議文件留下<br>你的 GitHub Username！

我會把大家加到 Team 裡面

<!--
停一下，讓大家在會議文件填上 GitHub Username。
-->

---
layout: default
---

# 工作內容

<div class="project-grid">
  <section>
    <h2>CFP 徵稿網站</h2>
    <p>徵稿規範與投稿資訊</p>
    <p class="project-time">約 9 月，徵稿規範出來後</p>
  </section>
  <section>
    <h2>CFS 贊助徵求網站</h2>
    <p>贊助資訊與合作方案</p>
    <p class="project-time">約 9 月，贊助資訊出來後</p>
  </section>
  <section>
    <h2>年會主網站</h2>
    <p>年會主題與議程表</p>
    <p class="project-time">約 10 月，主視覺出來後</p>
  </section>
  <section>
    <h2>大地遊戲</h2>
    <p>會眾與年會現場互動</p>
    <p class="project-time">約 10 月，活動組規劃出來後</p>
  </section>
</div>

<style>
.project-grid { display: grid; grid-template-columns: repeat(2, minmax(0, 1fr)); gap: 24px 36px; }
.project-grid section { border-top: 2px solid var(--sitcon-accent); padding-top: 16px; }
.project-grid h2 { font-size: 28px; margin-bottom: 10px; }
.project-grid p { margin-bottom: 8px; }
.project-grid .project-time { font-size: 18px; color: var(--sitcon-muted); }
</style>

<!--
這是開發組整個籌備週期的四個主要專案。月份是目前預估，開始時間取決於其他組提供規範、資訊、主視覺和活動規劃。
接下來逐一介紹。
-->

---
layout: image-right
image: /images/cfp-2026.png
alt: SITCON 2026 CFP 徵稿網站首頁
backgroundSize: contain
caption: SITCON 2026 徵稿網站
---

# CFP 徵稿網站

Call for Paper

- 提供徵稿規範與投稿資訊
- 約 **9 月**，徵稿規範出來後開始

[2026 徵稿網站](https://sitcon.org/2026/cfp/)

<!--
在 SITCON 中的任何地方聽到有人說「CFP」，指的就是徵稿網站。
歷年參考：https://sitcon.org/2026/cfp/、https://sitcon.org/2025/cfp/
截圖來源：https://sitcon.org/2026/cfp/，擷取於 2026-09-14。
-->

---
layout: image-right
image: /images/cfs-2026.png
alt: SITCON 2026 CFS 贊助徵求網站首頁
backgroundSize: contain
caption: SITCON 2026 贊助徵求網站
---

# CFS 贊助徵求網站

Call for Sponsor

- 約 **9 月**，贊助資訊出來後開始開發
- 預計沿用 2026 設計
- 只要調整資訊順序、資料與配色

[2026 贊助徵求網站](https://sitcon.org/2026/cfs/)

<!--
在 SITCON 中聽到「CFS」，指的就是贊助徵求網站。
以往 CFS 幾乎都是 PDF 贊助徵求書，2026 年第一次轉為網站。
因為去年的設計真的很好看，今年應該會復用它。開發組的工作大概是重新排列資訊流、改資料和顏色。Shout out to 毛哥！
截圖來源：https://sitcon.org/2026/cfs/，擷取於 2026-09-14。
-->

---
layout: image-right
image: /images/main-2026.png
alt: SITCON 2026 年會主網站首頁
backgroundSize: contain
caption: SITCON 2026 年會主網站
---

# 年會主網站

- 約 **10 月**，年會主視覺出來後開始開發
- 年會主題與 SITCON 介紹
- 最重要的 **議程表**
- **徵稿結束後**才切換主網站

[2026 年會主網站](https://sitcon.org/2026/)

<!--
在徵稿期結束後，https://sitcon.org 才會換成年會主網站。
主網站主要展示年會的主題、關於 SITCON 自己的一些資訊，還有最重要的議程表。
歷年參考：https://sitcon.org/2026/、https://sitcon.org/2025/
截圖來源：https://sitcon.org/2026/，擷取於 2026-09-14。
-->

---
layout: image-right
image: /images/game-ntag.png
alt: GitLab NTag 工作項目及相關的 App 與 Spec 製作項目
backgroundSize: contain
caption: NTag 活動規劃工作項目
---

# 大地遊戲

讓會眾與年會現場互動

- 今年想嘗試 **NFC 貼紙＋手機 App**
- 約 **10 月**，活動組規劃出來後開始開發
- 最晚 **12 月送審**

[NTag 工作項目](https://gitlab.com/sitcon-tw/2027/-/work_items/89)

<!--
為了增進會眾與年會各種設施、機制的互動，我們有大地遊戲這個酷東西。
以往幾乎都以 PWA 形式存在，今年想嘗試引入 NFC 貼紙，並做成手機 App。
今年收進來的應該有些 Flutter 人才，嘻嘻。
至少 12 月需要送審，組長會去要 OCF 的帳號。
截圖來源：https://gitlab.com/sitcon-tw/2027/-/work_items/89，擷取於 2026-09-14。
工作項目目前另列 App 製作為 9/18–10/16、Spec 製作為 8/28–9/30；投影片保留本次零籌原稿的概略起始月份，實際排程以團隊確認為準。
-->

---
layout: default
---

# 分工方式

- 以專案為單位分工
- 每個專案原則上由 1～2 人主責
- 遇到問題或工作量太大時，可以找其他人支援

<!--
原則上由 1～2 人主責一個專案，可以抓支援。
起火了總副召會下場救火，但請盡量不要起火。
-->

---
layout: center
---

# 登記你的興趣！

依照想參與或想嘗試的專案填寫

<!--
請大家到會議文件填寫興趣登記。可以勾選自己想參與，或想趁這次嘗試的專案；這份登記會作為後續分工的參考。
-->

---
layout: end
---

# 來約固定會議時間！

[when2meet.app/92DFEB7](https://when2meet.app/92DFEB7)

每週同步工作進度與下週安排

<!--
一起填寫可以開會的時段：https://when2meet.app/92DFEB7
固定會議主要同步這週做了什麼、目前進度，以及下週要做什麼。
-->
