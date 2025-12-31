# 兒童生長曲線追蹤網站

這是一個用於追蹤兒童身高和體重生長曲線的網頁應用程式。

## 功能特色

- 📊 視覺化生長曲線圖表（使用 Plotly.js）
- 👦👧 支援男生和女生的生長曲線數據
- 💾 本地儲存功能（使用瀏覽器 localStorage）
- 📱 響應式設計，支援手機和桌面裝置
- 📈 顯示多個百分位數（P3, P10, P25, P50, P75, P90, P97）

## 檔案說明

- `index.html` - 主要的 HTML 檔案，包含所有功能

## 部署方式

### 方法 1：直接開啟檔案
最簡單的方式是直接在瀏覽器中開啟 `index.html` 檔案。

### 方法 2：使用本地伺服器（推薦）

#### Python 3
```bash
# 在專案目錄下執行
python -m http.server 8000
```
然後在瀏覽器中開啟 `http://localhost:8000`

#### Node.js (使用 http-server)
```bash
# 安裝 http-server
npm install -g http-server

# 在專案目錄下執行
http-server -p 8000
```

#### PHP
```bash
# 在專案目錄下執行
php -S localhost:8000
```

### 方法 3：部署到網路伺服器

1. 將所有檔案上傳到您的網頁伺服器
2. 確保 `index.html` 在網站根目錄
3. 透過網址訪問您的網站

### 方法 4：使用 GitHub Pages + GitHub Actions（推薦）

本專案已配置 GitHub Actions 自動部署工作流程。

#### 設定步驟：

1. **在 GitHub 建立新儲存庫**
   - 登入 GitHub
   - 點擊右上角的 "+" → "New repository"
   - 輸入儲存庫名稱（例如：`growthup`）
   - 選擇 Public（GitHub Pages 免費版需要公開儲存庫）
   - 不要勾選 "Initialize this repository with a README"（因為我們已經有檔案了）

2. **將專案推送到 GitHub**
   ```bash
   # 在專案目錄下執行
   git init
   git add .
   git commit -m "Initial commit: Growth curve tracking app"
   git branch -M main
   git remote add origin https://github.com/您的使用者名稱/儲存庫名稱.git
   git push -u origin main
   ```

3. **啟用 GitHub Pages**
   - 進入儲存庫的 Settings（設定）
   - 點擊左側的 "Pages"
   - 在 "Source" 選擇 "GitHub Actions"
   - 儲存設定

4. **自動部署**
   - 當您推送程式碼到 `main` 或 `master` 分支時，GitHub Actions 會自動部署
   - 部署完成後，您的網站將在 `https://您的使用者名稱.github.io/儲存庫名稱` 上線
   - 您也可以在 Actions 標籤頁查看部署狀態

#### 手動觸發部署
如果需要手動觸發部署，可以：
- 進入儲存庫的 Actions 標籤頁
- 選擇 "Deploy to GitHub Pages" 工作流程
- 點擊 "Run workflow" 按鈕

### 方法 5：使用 Netlify

1. 註冊 Netlify 帳號
2. 將專案資料夾拖放到 Netlify 部署區域
3. 網站會自動部署並獲得一個網址

### 方法 6：使用 Vercel

1. 註冊 Vercel 帳號
2. 連接您的 GitHub 儲存庫或直接上傳專案
3. 自動部署完成

## 技術說明

- **前端框架**: 純 HTML/CSS/JavaScript（無需框架）
- **圖表庫**: Plotly.js（從 CDN 載入）
- **資料儲存**: 瀏覽器 localStorage
- **響應式設計**: CSS Grid 和 Flexbox

## 注意事項

- 資料儲存在瀏覽器的 localStorage 中，清除瀏覽器資料會導致紀錄遺失
- 建議定期備份重要資料
- 此應用程式完全在客戶端運行，不需要後端伺服器

## 瀏覽器支援

- Chrome/Edge（推薦）
- Firefox
- Safari
- Opera

## 授權

此專案為公開資料庫專案，可自由使用和修改。

