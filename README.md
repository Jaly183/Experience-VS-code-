# 成長的代價：Solow 比較靜態

適用大學部總體經濟學，約 15–20 分鐘。單一 HTML、繁體中文、無外部依賴。

## 預覽

直接以瀏覽器開啟 `index.html`。若瀏覽器限制本機檔案儲存，可在本資料夾執行：

```sh
python3 -m http.server 8000
```

再開啟 http://localhost:8000 。紀錄依瀏覽器及來源隔離，本機檔案與 HTTP 的紀錄不共用。

## 功能

- 調整儲蓄率、人口成長率、折舊率，比較兩組正穩態。
- 三段「預測 → 操作 → 解釋」任務、自由探索與黃金律定位。
- 紀錄存於瀏覽器，可下載 CSV；不需帳號或 token。

## 發布 GitHub Pages

先由教師審閱教材，再將本資料夾作為獨立 repository 推送至自己的 GitHub repo。於該 repo 的 Settings → Pages 選擇從分支部署，選 `main`、根目錄 `/`，保存後使用 GitHub 顯示的網址。本交付不含遠端建立或公開發布。

```sh
git remote add origin <你的 GitHub repo URL>
git push -u origin main
```

若尚未初始化，可先 `git init -b main`、`git add .`、`git commit -m "publish: Solow 互動教材"`。commit 需要你自己的 Git 姓名與 email。

詳見 [使用手冊](使用手冊-sim.md) 及 [設計歸檔](sdd-archive/2026-09-21-solow-comparative-statics/design.md)。頁面仍標示待授課教師審核。


## 本次交付狀態

已初始化本機 `main` 分支並將交付檔案加入暫存區。初始 commit 因目前未設定 Git 姓名與 email 而未完成；本機開啟與 zip 交付不受影響。設定本 repo 的真實身分後即可完成：

```sh
git config user.name "你的姓名"
git config user.email "你的 email"
git commit -m "publish: Solow 比較靜態互動教材"
```

未建立遠端 repo、未公開發布。成品仍待教師審核。

## 重跑驗證

`tests/verify.py` 使用 Python Playwright 與 macOS 的本機 Chrome。安裝 Playwright 後，在本資料夾執行 `python3 tests/verify.py`；測試啟動暫時的 localhost 伺服器，使用隔離的瀏覽器資料，不修改正式紀錄。其他系統需調整腳本內的 Chrome 路徑。教材本身無需這些測試工具。
