# 地理骨架訓練器

這是一個可直接部署到 GitHub Pages 的純前端地理空間記憶遊戲。網站不需要安裝套件、不需要 build，也不需要後端或資料庫。

## 三個學習模組

1. **世界大框架**：亞洲、歐洲、非洲、美洲、大洋洲，以及太平洋、大西洋、印度洋。
2. **臺灣周邊國家與海域**：臺灣周邊陸地骨架，以及太平洋、臺灣海峽、巴士海峽、東海。
3. **臺灣島與周邊島嶼**：臺灣島、澎湖群島、金門列嶼、馬祖列嶼、釣魚臺列嶼、龜山島、綠島、蘭嶼、琉球嶼（小琉球）、南海諸島。

每一個模組都使用相同流程：

- 觀察骨架
- 定位回想（系統隨機出題，點圖後立即判定）
- 顯影比較空間偏差

## 專案結構

```text
geography-memory-trainer-github/
├── index.html
├── assets/
│   ├── styles.css
│   └── app.js
├── .nojekyll
└── README.md
```

所有地圖向量資料已經內嵌在 `assets/app.js`，因此執行時不需要下載外部地圖資料，也沒有 CDN 相依性。

## 本機測試

可以直接雙擊 `index.html` 開啟。也可以用本機伺服器：

```bash
python3 -m http.server 8080
```

再開啟：

```text
http://localhost:8080
```

## 部署到 GitHub Pages

1. 在 GitHub 建立新的 repository。
2. 將此資料夾內的所有檔案上傳到 repository 根目錄。
3. 開啟 repository 的 **Settings → Pages**。
4. 在 **Build and deployment** 選擇 **Deploy from a branch**。
5. Branch 選擇 `main`，Folder 選擇 `/(root)`。
6. 儲存後等待 GitHub Pages 建立網址。

網站網址通常會是：

```text
https://你的帳號.github.io/你的-repository-名稱/
```

## 單檔版本

ZIP 外另附 `geography-memory-trainer-standalone.html`。它把 HTML、CSS、JavaScript 和地圖資料全部放在同一個檔案，適合直接傳送或快速測試。

## 技術與資料說明

- 純 HTML、CSS、JavaScript 與 SVG。
- 不收集、不上傳使用者資料。
- 小島符號為方便辨識與點選而適度放大。
- 南海諸島以一個整體學習項目呈現，不拆細。
- 海域光圈用於空間記憶，不代表精確海域邊界。
- 地圖輪廓取自 Natural Earth 衍生資料。
