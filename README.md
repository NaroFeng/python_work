# 太空戰情室 · 全球太空發射任務與商業航太趨勢分析

靜態版 GitHub Pages 站台：深色玻璃擬態儀表板，分析 2000–2026 年全球 3,065 筆
軌道發射任務（資料來源：Wikipedia 歷年軌道發射列表）。

## 內容

| 路徑 | 說明 |
| --- | --- |
| `index.html` | 單一頁面前端（Tailwind CSS + Chart.js + 原生 JS 動畫引擎） |
| `data/bootstrap.json` | KPI、8 大機構卡片、市佔率、火箭可靠度 |
| `data/race.json` | 動態排行榜的週（ISO Week）／月時間序列 |
| `data/agency/*.json` | 各機構中文檔案、影片與 KPI |
| `data/sync_status.json` | 靜態版說明（同步功能僅本機 Flask 可用） |
| `vendor/` | Tailwind CSS 與 Chart.js 的本地化版本（現場無網路也能完整呈現） |

## 功能

- **航太機構選擇矩陣**：點擊 8 大機構卡片即時切換全部視角
- **機構檔案與發射影片**：中文簡介、KPI、載具可靠度、2025-2026 發射精華（YouTube）
- **動態排行榜拉扯圖**：DOM + CSS `translateY` 物理交換動畫、60fps rAF 線性插值；
  支援週／月粒度、歷史累積／滾動 52 週、1x/2x/4x 倍速
- **全球市佔率消長圖** ＋ **Top 10 火箭家族可靠度排行**

> 本頁為建置當下的資料快照；「🔄 同步最新數據」功能需於本機以 Flask 執行。
