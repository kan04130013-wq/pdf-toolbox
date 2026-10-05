# PDF 工具箱

純前端的線上 PDF 工具，所有檔案都在瀏覽器裡處理，**不會上傳到任何伺服器**。不需要後端，放上 GitHub Pages 就能用。

## 功能

| 類別 | 工具 | 說明 |
|---|---|---|
| 整理 | 合併 PDF | 多個 PDF 與照片依順序合併，可拖曳排序、旋轉 |
| 整理 | 拆分 PDF | 每頁一檔、自訂範圍或每 N 頁一份，多檔自動打包 ZIP |
| 整理 | 移除頁面 | 點選縮圖刪除不要的頁面 |
| 整理 | 提取頁面 | 挑出需要的頁面，合併成一檔或每頁各存一檔 |
| 整理 | 旋轉 PDF | 逐頁或整份旋轉 |
| 整理 | 整理頁面 | 縮圖拖曳排序、旋轉、刪除頁面 |
| 整理 | 掃描為 PDF | 手機拍文件，四角拉正、自動增強／黑白／灰階濾鏡 |
| 最佳化 | 壓縮 PDF | 輕度（保留文字）、標準、強力三段 |
| 最佳化 | OCR 文字辨識 | 辨識掃描檔文字，輸出可搜尋的 PDF 或純文字（繁中、簡中、日、韓、英） |
| 轉換 | 照片轉 PDF | 上傳或用手機相機拍照 |
| 轉換 | PDF 轉 JPG | 可選頁碼、解析度（最高 300 dpi）、JPG 或 PNG |
| 轉換 | PDF 轉 Word | 可編輯文字（保留標題、段落、清單，掃描頁自動 OCR）或保留原版面 |
| 轉換 | PDF 轉 PowerPoint | 每頁一張投影片，可把頁面文字放進備忘稿 |
| 轉換 | PDF 轉 Markdown | 擷取文字，依字體大小判斷標題、辨識清單 |
| Office 轉 PDF | Word 轉 PDF | .docx 轉 PDF，保留標題、清單、表格、圖片；也可用瀏覽器列印產生可選取文字的 PDF |
| Office 轉 PDF | Excel 轉 PDF | .xlsx／.xls／.ods／.csv，可選工作表、自動橫向、縮小到一頁寬 |
| Office 轉 PDF | PPT 轉 PDF | .pptx 轉 PDF，支援母片、版面配置、文字、圖片、基本圖形、表格、背景 |
| Office 轉 PDF | HTML 轉 PDF | 上傳 .html 或貼上程式碼，自動避免把文字和區塊切成兩半 |
| 編輯 | 編輯 PDF | 加入文字、圖片、方框、螢光筆、手寫、白色遮蓋 |
| 編輯 | PDF 表單 | 直接在表單欄位上填寫，可選擇鎖定內容 |
| 編輯 | 添加頁碼 | 6 種位置、中英文格式、封面可不編號 |
| 編輯 | 添加浮水印 | 文字或圖片，可調大小、透明度、角度，置中或鋪滿 |
| 編輯 | 裁剪 PDF | 以公釐設定四邊裁切，附預覽 |
| 安全 | 簽署 PDF | 手寫或上傳簽名照片（自動去背），拖曳到指定位置 |
| 安全 | 標記密文 | 框選或搜尋文字後永久塗黑，被遮蔽的文字會真正從檔案刪除 |

## 使用的套件（透過 CDN 載入）

- [pdf-lib](https://pdf-lib.js.org/)、[PDF.js](https://mozilla.github.io/pdf.js/)、[JSZip](https://stuk.github.io/jszip/)
- 需要時才載入：[Tesseract.js](https://tesseract.projectnaptha.com/)（OCR）、[docx](https://docx.js.org/)（Word）、[PptxGenJS](https://gitbrent.github.io/PptxGenJS/)（PowerPoint）、[mammoth](https://github.com/mwilliamson/mammoth.js)（讀取 Word）、[SheetJS](https://sheetjs.com/)（讀取 Excel）、[html2canvas](https://html2canvas.hertzen.com/)（HTML 排版）

## 部署

把 `index.html` 放在 repository 最外層，到 **Settings → Pages** 選 **Deploy from a branch → main → / (root)**。

## 限制

- 有密碼保護的 PDF 需要先解除密碼。
- 「標準」與「強力」壓縮會把頁面轉成圖片，文字將無法選取。
- PDF 轉 Word 的「可編輯文字」模式不保留原本的排版與表格。
- OCR 準確度取決於掃描品質，辨識結果可能有錯字。
- Office 轉 PDF 產生的頁面是高解析度圖片，文字無法選取（Word、HTML 可改用「瀏覽器列印」）。
- PPT 轉 PDF 不支援圖表、SmartArt、特殊效果；舊版 .doc／.ppt 需先另存成 .docx／.pptx。

## 授權

MIT
