# PDF 工具箱

純前端的線上 PDF 工具，所有檔案都在瀏覽器裡處理，**不會上傳到任何伺服器**。不需要後端，放上 GitHub Pages 就能用。

## 功能

| 類別 | 工具 | 說明 |
|---|---|---|
| 整理 | 合併 PDF | 多個 PDF 與照片依順序合併，可拖曳排序、旋轉 |
| 整理 | 拆分 PDF | 每頁一檔、自訂範圍或每 N 頁一份，多檔自動打包 ZIP |
| 整理 | 整理頁面 | 縮圖拖曳排序、旋轉、刪除頁面 |
| 最佳化 | 壓縮 PDF | 輕度（保留文字）、標準、強力三段 |
| 轉換 | 照片轉 PDF | 上傳或用手機相機拍照，支援 JPG/PNG/WebP/GIF/BMP |
| 轉換 | PDF 轉 JPG | 可選頁碼、解析度（最高 300 dpi）、JPG 或 PNG |
| 轉換 | PDF 轉 Markdown | 擷取文字，依字體大小判斷標題、辨識清單 |
| 編輯 | 添加頁碼 | 6 種位置、中英文格式、封面可不編號 |
| 編輯 | 添加浮水印 | 文字或圖片，可調大小、透明度、角度，置中或鋪滿 |
| 編輯 | 裁剪 PDF | 以公釐設定四邊裁切，附預覽 |
| 編輯 | 簽署 PDF | 手寫或上傳簽名照片（自動去背），拖曳到指定位置 |

## 使用的套件（透過 CDN 載入）

- [pdf-lib](https://pdf-lib.js.org/) 1.17.1：建立與修改 PDF
- [PDF.js](https://mozilla.github.io/pdf.js/) 3.11.174：渲染頁面、擷取文字
- [JSZip](https://stuk.github.io/jszip/) 3.10.1：打包多個檔案
- Noto Sans TC（Google Fonts）

## 在本機執行

直接用瀏覽器開啟 `index.html` 即可。若遇到瀏覽器限制，可以開一個簡單的本機伺服器：

```bash
python3 -m http.server 8000
# 然後打開 http://localhost:8000
```

## 部署到 GitHub Pages

專案已附上 `.github/workflows/pages.yml`，推送到 `main` 分支就會自動部署。

1. 在 GitHub 建立新的 repository，並推送這個專案。
2. 到 repository 的 **Settings → Pages**，在 **Source** 選擇 **GitHub Actions**。
3. 等 **Actions** 分頁的部署完成後，網站就會出現在 `https://<你的帳號>.github.io/<repository 名稱>/`。

## 限制

- 有密碼保護的 PDF 需要先解除密碼。
- 「標準」與「強力」壓縮會把頁面轉成圖片，壓縮後文字無法選取或搜尋。
- iPhone 的 HEIC 照片只有 Safari 能讀取。
- PDF 轉 Word/Excel/PowerPoint、OCR、加密等功能需要後端，目前沒有提供。

## 授權

MIT
