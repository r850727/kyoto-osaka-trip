# 京都・大阪 九天八夜（2026/11/15 – 11/23）

京都、宇治、伏見、姬路、大阪自助旅行的行程網站。

## 👉 [打開行程網站](https://r850727.github.io/kyoto-osaka-trip/)

https://r850727.github.io/kyoto-osaka-trip/

想直接看某一天，可以在網址後面加 `#day1` 到 `#day9`，例如 [11/15 第一天](https://r850727.github.io/kyoto-osaka-trip/#day1)。住宿和航班資訊在 [#hotels](https://r850727.github.io/kyoto-osaka-trip/#hotels)。

- 用日期分頁切換每天的行程，每天的時間軸都排好了
- 點 📍 會在 Google 地圖上開啟地點；點 🧭 會用大眾運輸導航到目的地
- 航班和出發去機場的時間都有特別標出來
- 旅行期間打開網站，會自動跳到當天，並標出目前的行程

## 更新網站

網站由 GitHub Pages 從 `main` 分支的根目錄發佈。修改 `index.html` 並推送到 `main` 之後，等一兩分鐘網站就會自動更新。

## 修改行程

所有行程資料都在 `index.html` 裡的 `DAYS` 陣列，每一列代表一個行程：

```js
{t:'07:00', e:'08:30', k:'spot', ti:'清水坂 → 清水寺', n:'備註', p:['清水寺']}
```

- `t` / `e`：開始和結束時間
- `k`：類型，可以是 `airport`、`flight`、`move`、`spot`、`food`、`hotel`、`rest`
- `p`：地點。可以直接寫 Google 地圖的搜尋字，或寫成 `['顯示名稱', '搜尋字或 maps.app.goo.gl 網址']`
- `opt:1` 代表備選行程；`imp:'...'` 會用紅字標出重點；`nav:1` 會把地點改成導航連結
