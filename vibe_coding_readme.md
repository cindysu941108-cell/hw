# 🚀 Taichung Metro Web Project - Vibe Coding Prompt Guide

本專案為 **臺中捷運 (Taichung Metro) 多頁面響應式網站**。整個開發過程採用 **Vibe Coding** 的理念，透過自然語言提示詞（Prompts）引導 AI 完成前端架構設計、樣式模組化、多頁面拆分與整合，以及最終的跨頁面組件維護。

本文件詳細紀錄本專案開發過程中所使用的核心指令（Prompts）與操作邏輯，方便於 GitHub 上分享與複現。

---

## 📌 目錄
1. [什麼是本專案的 Vibe Coding？](#-什麼是本專案的-vibe-coding)
2. [核心 Vibe Coding 指令集 (Prompt Guide)](#-核心-vibe-coding-指令集-prompt-guide)
   - [階段一：頁面拆分與內容補齊](#階段一頁面拆分與內容補齊)
   - [階段二：單頁面整合 (All-in-One SPA Concept)](#階段二單頁面整合-all-in-one-spa-concept)
   - [階段三：解耦與結構優化 (CSS 拆分與模組化)](#階段三解耦與結構優化-css-拆分與模組化)
3. [專案目錄結構 (Project Structure)](#-專案目錄結構-project-structure)
4. [GitHub 部署與測試連結](#-github-部署與測試連結)

---

## 💡 什麼是本專案的 Vibe Coding？

在傳統開發中，我們需要手寫每個 HTML 標籤、手動計算 CSS 佈局與維護複雜的路由結構。
在 **Vibe Coding** 的模式下，開發者的核心角色轉變為 **「架構設計師與指揮官」**：
- **明確需求邊界**：告訴 AI 頁面架構與統一樣式。
- **維護語意一致性**：確保導覽列、側邊欄、主內容區與頁尾在不同頁面維持語意學（Semantic HTML）與樣式繼承。
- **靈活切換架構**：能隨時下達指令在「多頁面架構 (MPA)」與「單頁面架構 (SPA)」之間無縫切換與解耦。

---

## 🎯 核心 Vibe Coding 指令集 (Prompt Guide)

以下為本專案在各階段使用的關鍵 AI 提示詞（Prompts）：

### 階段一：頁面拆分與內容補齊
> **目標**：基於現有的 `index.html` 與 `hw07css.css`，補齊其他未完成的次級頁面內容。

* **使用的 Prompt 指令：**
  ```text
  你現在是 senior 前端工程師。請基於現有的 index.html 架構（含上方導覽列、左側側邊欄、主內容區、頁尾與 hw07css.css），幫我補齊以下四個頁面的完整 HTML 原始碼：
  1. history.html：捷運歷史與發展時間軸
  2. food.html：綠線18個車站及轉乘資訊
  3. guide.html：特色車站及周邊導覽
  4. traffic.html：營運班距、票價、搭乘流程
  要求：
  - 嚴格保留統一的 CSS 類別與 DOM 結構。
  - 採用豐富且結構化的語意內容。
  - 輸出格式需便於獨立下載與維護。
  ```

---

### 階段二：單頁面整合 (All-in-One SPA Concept)
> **目標**：為了便於快速展示或簡化部署，將多頁面內容合併為單一頁面，透過錨點（Anchor）導向。

* **使用的 Prompt 指令：**
  ```text
  請幫我將原本的四個 HTML 頁面內容（history, food, guide, traffic）與首頁整合成單一 HTML 檔案（taichung_metro_all_in_one.html）。
  要求：
  - 上方導覽列與側邊選單改為錨點連結（#history, #food 等），點擊可順暢捲動至對應區塊。
  - 保持共用 hw07css.css 的樣式設定。
  ```

---

### 階段三：解耦與結構優化 (CSS 拆分與模組化)
> **目標**：將整合後的檔案解耦，恢復為乾淨的項目包結構，實現「 HTML 結構與 CSS 樣式完全分離」。

* **使用的 Prompt 指令：**
  ```text
  請將 HTML 頁面與 CSS 樣式完全分離，並幫我規劃標準的站台專案目錄結構。
  檔案規格要求：
  - 根目錄包含 index.html 與 hw07css.css。
  - 子目錄 SecondMetro/ 放 history.html, food.html, guide.html, traffic.html。
  - 確保所有 HTML 頁面正確引用相對路徑 ../hw07css.css，實現統一視覺樣式維護。
  ```

---

## 📁 專案目錄結構 (Project Structure)

```text
taichung_metro_site/
├── index.html              # 臺中捷運首頁
├── hw07css.css             # 網站核心共用 CSS 樣式表
├── README.md               # 專案說明與 Vibe Coding 指令集 (本檔案)
└── SecondMetro/            # 次級分頁資料夾
    ├── history.html        # 捷運歷史與發展時間軸
    ├── food.html           # 綠線18個車站及轉乘資訊
    ├── guide.html          # 特色車站及周邊導覽
    └── traffic.html        # 營運班距、票價、搭乘流程
```

---

## 🔗 GitHub 部署與測試連結

您可以透過以下方式取得程式碼或線上預覽專案：

- 📦 **GitHub Repository / Code Download**：
  [https://github.com/your-username/taichung-metro-vibe-coding](https://github.com/your-username/taichung-metro-vibe-coding) *(請將 your-username 替換為您的 GitHub 帳號)*
  
- 🌐 **GitHub Pages 線上展示**：
  [https://your-username.github.io/taichung-metro-vibe-coding/index.html](https://your-username.github.io/taichung-metro-vibe-coding/index.html)

---

### 🛠️ 快速開始 (Quick Start)
1. Clone 本專案：
   ```bash
   git clone https://github.com/your-username/taichung-metro-vibe-coding.git
   ```
2. 使用瀏覽器開啟 `index.html` 或使用 Live Server 進行預覽。