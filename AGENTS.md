# 國中教材PDF索引（專案藍圖 / AGENTS.md）

> 本檔為跨 Agent 通用的專案說明書。任何 Agent 開工前應先讀本檔與 `handoff.md`；詳細脈絡放在 `docs/decisions.md`、`CHANGELOG.md` 與 `.agent/`。

## 專案簡介

建立可依科目與學年度瀏覽並開啟國中教材 PDF 的靜態網頁。

## 技術棧與版本

HTML5／CSS3／原生 JavaScript；不使用第三方套件，支援目前版本的 Chrome、Edge、Safari 與 Firefox。

## 常用指令

尚未建立開發流程。

## 三層邊界

- **永遠要做**：保持 PDF 分類清楚、手機也能使用；修改前保留既有教材檔。
- **要先問我**：新增或移除教材連結、變更分類方式、部署或公開網站。
- **絕對不要做**：刪除或覆寫 PDF、對外傳送資料、產生付費或不可逆的服務操作。

## 教材分類規則

- 7 年級的「自然」科目顯示為「生物」。
- 8、9 年級的「自然」科目顯示為「理化」。

## 目標與路線圖

- [x] 階段一：建立教材 PDF 索引網頁初版。
- [ ] 階段二：依實際教材擴充學年度與科目資料。
  - [x] 8 年級第 1 學期：5 科共 16 份教材（國文 5、理化 3、地理 3、歷史 2、公民 3）。
  - [ ] 其他年級與學期：尚無教材。

## 資料夾結構

```text
.
├── 8年級第1學期/           # 目前已整理的教材 PDF
├── .agent/                # 跨 Agent 任務文件與範本
├── docs/                  # 決策紀錄
├── AGENTS.md              # 專案藍圖
├── handoff.md             # 交接狀態
├── CHANGELOG.md           # 變更歷史
├── index.html              # 首頁
├── grade*-sem*.html        # 各年級、學期教材頁
├── all-grades.html         # 不分年級教材頁
├── advanced.html           # 進階教材頁
├── apcs-classification.html # APCS 實作題演算法分類頁
└── styles.css              # 網站共用樣式
```

## Session 開始時必讀

每次開始新任務前，依序讀取：

1. `handoff.md`
2. `CHANGELOG.md`
3. `docs/decisions.md`
4. `.agent/` 最近 2–3 個任務資料夾（若與本次任務相關）

純文字修改或小型單檔調整可略過此步驟。

## 任務文件工作流程

預計修改 3 個以上檔案、涉及架構變更，或使用者要求先規劃時，先在 `.agent/<YYYY-MM-DD>_<task-slug>/` 建立 `implementation_plan.md`，等待使用者審核或修正後再執行。完成後在相同資料夾寫 `walkthrough.md`。範本位於 `.agent/_templates/`。

單純 bug 修復、格式調整或小型單檔修改，可直接記一行到 `CHANGELOG.md`。

## 收工紀律

收工或 session 結束前，更新路線圖、完整改寫 `handoff.md`、在 `CHANGELOG.md` 補一行摘要；有架構決策時更新 `docs/decisions.md`，有任務文件時完成 `walkthrough.md`。

## 工作約定

- 任何 Agent、任何電腦：開工先讀 `handoff.md`，收工必更新它。
- 修改共用檔案前先讀最新內容，避免覆蓋其他 Agent 的變更。
- 所有回應與文件使用繁體中文。
- 使用 Git／GitHub 作為同步方式；工作分支為 `main`，遠端為公開的 `origin`。
