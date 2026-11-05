# CS Pocket Notes

以繁體中文整理電腦科學觀念的靜態學習筆記網站。每篇包含快速摘要、核心觀念、程式範例、常見錯誤與重點整理，適合學習與考前複習。

目前收錄 UNIX/C 系統程式設計的四個主題：檔案位移、行程建立與結束、select 與 poll、fcntl() Record Locking。

## 檔案結構

```text
cs-pocket-notes/
├── AGENTS.md
├── README.md
├── index.html
├── assets/
│   └── style.css
├── notes/
│   ├── file-offset.html
│   ├── fork-and-exit.html
│   ├── select-vs-poll.html
│   └── fcntl-record-locking.html
└── templates/
    └── note-template.html
```

## 本機瀏覽

直接以瀏覽器開啟 `index.html` 即可，不需安裝套件或建置。所有頁面使用相對路徑、UTF-8 與共用 CSS，無 JavaScript、外部字型或 API 依賴。

若已安裝 Python，也可在根目錄執行 `python -m http.server 8000 --bind 127.0.0.1`，再開啟 <http://127.0.0.1:8000>。

網頁內的 C 程式需另存成 `.c` 檔，在提供 POSIX API 的 Linux、macOS 或 WSL 環境編譯；Windows 原生 C 工具鏈不一定支援 `fork()`、`poll()` 等介面。瀏覽網站本身不需要 C 編譯器。

## 部署到 GitHub Pages

將專案推送到 GitHub 儲存庫，在 **Settings → Pages → Build and deployment** 選擇 **Deploy from a branch**，指定網站所在分支及 **/ (root)**，儲存後等待部署完成。不需要建置步驟；入口為根目錄的 `index.html`。

## 新增筆記

1. 完整閱讀 `AGENTS.md`，檢查 `notes/` 是否已有相同主題。
2. 複製 `templates/note-template.html` 至 `notes/主題英文名稱.html`。檔名使用小寫英文與連字號。
3. 更新 `<title>`、description、麵包屑、主標題與副標，填寫五個必要教學區塊。快速摘要使用 1～3 句話，重點整理保留 3～5 點。
4. 保留 `../assets/style.css`、頁內目錄 ID 與 `../index.html` 返回首頁連結。沿用共用樣式，不在單頁加入重複 CSS。
5. 在 `index.html` 的 `.notes-grid` 加入標題、簡介與 `notes/檔名.html` 連結，更新篇數文字。
6. 查證技術內容，提供簡短且符合概念的程式範例、編譯方式與預期結果；需要時在文末加入官方參考文件。
7. 檢查 HTML、UTF-8、所有相對路徑及目錄連結，實際確認桌面與手機寬度，並在支援 POSIX 的環境驗證範例。

設計使用主色 `#0F766E`、標題 `#1F2937`、背景 `#F8FAFC`、卡片 `#FFFFFF` 與次要文字 `#64748B`；全站共用 `assets/style.css`。
