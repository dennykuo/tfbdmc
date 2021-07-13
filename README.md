# 使用 Codekit 編譯 Tailwind CSS

## 步驟

```yarn install```
或
``` npm install```

將目錄拉入 Codekit 中，並做好適當設定

## Build files

Entry: /assets/css/src/app.css
Output: /assets/css/dist/app.css

預設 purgeCSS 為啟用，偵測範圍為 **/*.html 及 **/*.blade.php

## Watch files

以下動作會觸發編譯 tailwind css

- 編輯非被編譯的 **/*.css
- 編輯 **/*.html 及 **/*.blade.php

## 附加套件

- postcss-nested: 讓 postcss 支援 scss 的嵌套語法
- postcss-extend-rule: 讓 postcss 支援嵌套語法中的 parent selector
- kutty: 預先設置的元件樣式庫 [https://kutty.netlify.app](https://kutty.netlify.app)，某些 UI 功能使用 alpine.js
- @tailwindcss/forms: 表單元件樣式
- @tailwindcss/typography: 內容文章樣式

## 備註

postcss-nested 套件會因 codekit 中 CSSO 先做了 minify 而導致錯誤，建議關閉 CSSO

有時 html 或 blade 檔案無法觸發 Compile 時，可重啟 codekit 試試