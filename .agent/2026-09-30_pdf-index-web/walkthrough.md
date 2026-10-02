# Walkthrough：教材 PDF 索引網頁初版

## Summary

建立「國中 PDF 教材」首頁、8 個獨立分類頁與共用樣式。首頁提供 7、8、9 年級上下學期、不分年級與進階教材共 8 張卡片；各分類頁依國文、生物或理化、地理、歷史、公民呈現。網站與教材 PDF 已公開推送至 GitHub。

## Files changed

- `index.html`：8 張教材分類入口卡片。
- `grade7-sem1.html` 至 `advanced.html`：8 個獨立分類頁。
- `grade8-sem1.html`：連結現有 10 份教材 PDF；理化區含 3 份教材。
- `styles.css`：共用的校園圖書館索引卡視覺與響應式排版。
- `AGENTS.md`、`handoff.md`、`CHANGELOG.md`、`docs/decisions.md`：更新進度、Git 同步狀態與決策紀錄。

## Verification

- 確認首頁含 8 個連至獨立 HTML 的入口。
- 確認 `grade8-sem1.html` 的 10 個 PDF 路徑與 `8年級第1學期/` 實際檔名完全相符。
- 確認共建立 9 個 HTML 頁面及 1 個共用樣式檔。
- 確認公開 GitHub 儲存庫已有 `main` 分支，且本機已追蹤該分支。

## Follow-ups

- 新增其他學期教材前，先確認分類，再在對應頁面加入連結。
