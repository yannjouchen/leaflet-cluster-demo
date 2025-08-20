# Leaflet MarkerCluster – 固定地理半徑示範

用「地理半徑（公尺）」來驅動 `Leaflet.markercluster` 的 `maxClusterRadius`。  
做法是依據目前 **緯度** 與 **縮放層級** 算出每像素約等於幾公尺，將公尺半徑換算為像素半徑。

## 線上預覽（GitHub Pages）
1. 建立 Repo：在 GitHub 建一個新專案，名稱建議：`leaflet-cluster-demo`
2. 把這兩個檔案（`index.html`, `README.md`）push 上去。
3. 進入 Repo → **Settings** → **Pages**。
4. 在 **Build and deployment** 區塊：
   - **Source** 選擇 `Deploy from a branch`
   - **Branch** 選 `main`、資料夾 `/ (root)`，按 **Save**。
5. 等待 30～90 秒，GitHub Pages 就會自動生效。

🔗 預覽網址會是：  
👉 [https://yannjouchen.github.io/leaflet-cluster-demo/](https://yannjouchen.github.io/leaflet-cluster-demo/)

## 本機開啟
- 直接用瀏覽器打開 `index.html`（需要可連網抓 CDN）。
- 或用任何靜態伺服器（例如 `python -m http.server 8080`）啟動後，瀏覽 `http://localhost:8080`。

## 重點程式
- 換算公式（Web Mercator）：
