# 📂 公版 SCSS 專案結構

此專案作為 **公版樣式結構範例**，提供開發人員統一的檔案規範。  
主要透過 `index.scss` 匯入所有部分檔案 (partials)，最後編譯成 `css/index.css`，並由 `index.html` 引用。

---

## 📁 專案目錄

```bash
PUBLIC-STRUCTURE/
├── scss/                  # 樣式相關檔案
│   ├── css/               # 編譯輸出的 CSS 目錄
│   │   ├── index.css      # 編譯後的 CSS
│   │   └── index.css.map  # Source map，方便除錯
│   │
│   ├── _base.scss         # 基礎樣式 (Reset、全域樣式)
│   ├── _components.scss   # 元件樣式 (Button、Card、Navbar...)
│   ├── _utils.scss        # 工具樣式 (helper classes)
│   ├── _variables.scss    # 全域變數 (字體、顏色、間距)
│   ├── index.scss         # 主入口 SCSS，負責匯入所有 partials
│   └── index.html         # 測試用靜態頁面
│
└── README.md              # 說明文件
```
---

## ⚙️ 編譯流程

1. 安裝 VSCode 擴充套件 [Live Sass Compiler](https://marketplace.visualstudio.com/items?itemName=ritwickdey.live-sass)  
   - 會自動將 `index.scss` 編譯成 `css/index.css`

2. 在 `index.html` 引用編譯後的 CSS：
   ```html
   <link rel="stylesheet" href="./scss/css/index.css">
## 📌 各檔案職責
### `_variables.scss`
集中管理專案變數（字體、顏色、間距…）
### `_components.scss`
撰寫可重用元件樣式（Button、Card…）
### `_utils.scss`
放置工具類樣式（helper classes，如文字置中、間距）
### `index.scss`
主入口，匯入所有部分檔案

## 🚀 注意事項
1. 所有` _* .scss` 檔案為 partials，不可直接編譯，需由 `index.scss` 匯入。

2. 編譯後的 CSS 統一輸出到 `/css`資料夾內

3. `.css.map` 檔案為壓縮後檔案，不需上傳至 FTP

## 上傳 FTP
- 只需將 `index.html`、`index.css`、`img/ 內的圖片 (可選)` 上傳即可
- 其餘檔案請保留

