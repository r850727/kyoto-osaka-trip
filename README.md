# 京都・大阪 九天八夜（2026/11/15 – 11/23）

京都、宇治、伏見、姬路、大阪自助旅行的行程網站。

- 用日期分頁切換每天的行程，每天的時間軸都排好了
- 點 📍 會在 Google 地圖上開啟地點；點 🧭 會用大眾運輸導航到目的地
- 航班和出發去機場的時間都有特別標出來
- 旅行期間打開網站，會自動跳到當天，並標出目前的行程

## 發佈到 GitHub Pages

1. 把 `index.html` 推到 GitHub repo
2. 到 repo 的 **Settings → Pages**
3. Source 選 **Deploy from a branch**，Branch 選 `main` / `(root)`，然後存檔
4. 等一兩分鐘，網址會是 `https://<帳號>.github.io/<repo 名稱>/`

## 修改行程

所有行程資料都在 `index.html` 裡的 `DAYS` 陣列，每一列代表一個行程：

```js
{t:'07:00', e:'08:30', k:'spot', ti:'清水坂 → 清水寺', n:'備註', p:['清水寺']}
```

- `t` / `e`：開始和結束時間
- `k`：類型，可以是 `airport`、`flight`、`move`、`spot`、`food`、`hotel`、`rest`
- `p`：地點。可以直接寫 Google 地圖的搜尋字，或寫成 `['顯示名稱', '搜尋字或 maps.app.goo.gl 網址']`
- `opt:1` 代表備選行程；`imp:'...'` 會用紅字標出重點；`nav:1` 會把地點改成導航連結
