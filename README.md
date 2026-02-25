# fubon-omnitag-dist

此專案提供 **Fubon Omnitag SDK 的打包產物（distribution files）**。

客戶可直接 clone 此 repo，並將 `fubon-omnitag/` 資料夾放入 Cordova App 的 `src/assets/` 後使用。

## 專案用途

- 提供可直接部署的 SDK 靜態檔案
- 免自行建置（build）
- 適用 Cordova App WebView 載入情境

## 目錄說明

```text
.
├─ README.md
└─ fubon-omnitag/
   ├─ fubon-omnitag.js
   └─ *.chunk.js
```

- `fubon-omnitag.js`：SDK 主入口檔
- `*.chunk.js`：SDK 執行時所需分包檔案

## 使用方式

1. Clone 此 repo。
2. 將整個 `fubon-omnitag/` 資料夾複製到 Cordova 專案的 `src/assets/` 下。
3. 確保 App 端以 `assets/fubon-omnitag/fubon-omnitag.js` 為路徑載入 SDK。

範例結構：

```text
your-cordova-app/
└─ src/
   └─ assets/
      └─ fubon-omnitag/
         ├─ fubon-omnitag.js
         └─ *.chunk.js
```

## 注意事項

- 請**完整保留** `fubon-omnitag/` 內所有檔案。
- 不要任意更名、刪除或只複製部分檔案，否則 chunk 載入可能失敗。
- 本 repo 內容為打包後產物，除非有明確需求，請勿直接修改。

## 更新方式

- SDK 升級時，請以新版 `fubon-omnitag/` **完整覆蓋**舊版資料夾。
- 若 App 有快取機制，建議發版時一併確認快取更新策略，避免載入到舊檔。

