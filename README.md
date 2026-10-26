# 證件照小幫手（ID Photo Tool）

單頁網頁工具，比照 LunaShelf 模式以 GitHub Pages 發布、在手機主畫面當 App 用。

功能：
- 規格預設：美簽 DS-160／DV 樂透（600×600 px、JPEG ≤ 240 KB、頭部 50–69%、眼線距底 56–69%）、台灣護照／身分證 2 吋（35×45 mm、頭頂至下顎 71–80%）
- 上傳照片或直接拍照；拖曳／縮放／旋轉／亮度／對比調整，附構圖引導線
- 自動去背換白底（MediaPipe Selfie Segmentation，瀏覽器本機運算，照片不上傳）
- 臉部偵測即時檢測：頭部比例、置中、眼睛高度、亮度、背景，並給具體調整建議；附「自動對位」
- 匯出：單張成品 JPG（美簽自動壓至 240 KB 內）、4×6 吋 300 dpi 排版 JPG（沖洗裁切用）

注意：檢測為輔助估算，非官方認證。台灣護照官方規定照片不修改、不得合成，去背版請勿用於台灣護照送件（白牆原圖＋僅裁切最保險）。

## 發布方式（GitHub Pages）
1. 在 GitHub 建立 repo（例如 `idphoto`），把本資料夾所有檔案上傳到 main 分支。
2. Repo → Settings → Pages → Source 選「Deploy from a branch」、分支選 main / (root)、Save。
3. 約 1 分鐘後即可用 https://startchao.github.io/idphoto/ 開啟；iPhone Safari 開啟後「加入主畫面」即成 App 圖示。

所有處理都在使用者瀏覽器本機完成；AI 模型（MediaPipe）由 jsDelivr CDN 載入。
