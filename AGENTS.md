
# CS Pocket Notes — AI Development Guide

## 1. Project Overview

CS Pocket Notes 是一個以繁體中文撰寫的電腦科學學習筆記網站。

本專案的目的是將複雜的程式設計概念整理成容易理解、適合快速複習的學習內容。

網站主要提供：
- 清楚易懂的概念解釋
- 簡短的程式碼範例
- 常見錯誤與觀念比較
- 考試前的重點整理

本專案不只是建立單一網頁，而是建立一套可以持續新增學習筆記的網站系統。

## 2. Technology Stack

使用以下技術：
- HTML5：網頁結構
- CSS3：視覺設計與響應式排版
- GitHub Pages：靜態網站部署

開發限制：
- 不使用 React、Vue 或其他前端框架。
- 不需要後端、資料庫或 API Key。
- 優先使用原生 HTML 與 CSS。
- 所有網頁必須能直接透過瀏覽器開啟。
- 網站必須相容於 GitHub Pages。

## 3. Project Structure

專案採用以下固定結構：

cs-pocket-notes/
- AGENTS.md：AI 開發規則
- README.md：專案介紹與使用方法
- index.html：網站首頁
- assets/
  - style.css：全站共用樣式
- notes/
  - file-offset.html
  - fork-and-exit.html
  - select-vs-poll.html
  - fcntl-record-locking.html
- templates/
  - note-template.html：新增筆記的標準模板

所有新增的筆記頁面都必須放在 notes/ 目錄。

不要任意新增其他資料夾或改變現有結構。

## 4. Visual Design Rules

網站風格：
- 簡潔、現代、適合學生閱讀
- 使用卡片式布局呈現筆記
- 保持充足留白
- 避免過度動畫與複雜裝飾

固定配色：
- 主色：#0F766E
- 標題文字：#1F2937
- 背景色：#F8FAFC
- 卡片背景：#FFFFFF
- 次要文字：#64748B

排版要求：
- 使用系統字體，優先支援繁體中文。
- 標題必須有清楚的層級。
- 卡片使用一致的圓角與間距。
- 程式碼區塊使用等寬字體。
- 網頁必須支援手機與電腦閱讀。

所有頁面共用 assets/style.css。

除非必要，不得在個別頁面重複撰寫 CSS。

## 5. Homepage Rules

首頁固定包含以下區塊：

1. Header
   - 網站名稱：CS Pocket Notes
   - 簡單的網站導覽

2. Hero Section
   - 網站標題
   - 一段簡短的網站介紹

3. Notes Section
   - 使用卡片顯示所有筆記
   - 每張卡片包含標題、簡介與閱讀連結

4. Footer
   - 網站名稱
   - 簡單的專案說明

每當新增筆記時，必須同步更新首頁卡片。

不得讓首頁出現無法開啟的連結。

## 6. Note Page Template

所有筆記頁面必須使用
templates/note-template.html 作為基礎。

每篇筆記都必須包含：

1. Note Title
   - 清楚描述本篇主題。

2. Quick Summary
   - 使用 1～3 句話介紹核心概念。

3. Core Concepts
   - 使用容易理解的語言解釋重要觀念。

4. Code Example
   - 提供簡短的程式碼與說明。
   - 不適合使用程式碼的主題可以使用文字範例。

5. Common Mistakes
   - 說明學習者容易誤解的地方。

6. Key Takeaways
   - 整理 3～5 個重點。

每一篇筆記都必須有返回首頁的連結。

## 7. Naming Conventions

檔案命名規則：

- 一律使用小寫英文。
- 多個英文單字使用連字號連接。
- HTML 檔案使用 .html 副檔名。
- 不使用空白、中文或特殊符號作為檔名。

正確範例：
- file-offset.html
- process-control.html
- memory-management.html

錯誤範例：
- FileOffset.html
- 我的筆記.html
- new page.html

## 8. Workflow for Adding New Notes

當使用者要求新增筆記時，AI 必須：

Step 1：
閱讀 AGENTS.md，確認專案規則。

Step 2：
檢查 notes/ 內是否已有相同主題，避免重複。

Step 3：
複製 templates/note-template.html 的結構，建立新的 HTML 頁面。

Step 4：
按照 Note Page Template 的規定填入內容。

Step 5：
沿用 assets/style.css，不另外建立新的樣式系統。

Step 6：
更新 index.html，加入新筆記卡片及正確連結。

Step 7：
檢查頁面結構、文字、程式碼及導覽連結。

Step 8：
回報新增的檔案、修改的檔案及檢查結果。

如果使用者沒有特別要求，不得刪除舊筆記或改變網站整體風格。

## 9. Content Quality Rules

所有學習內容必須符合：

- 使用繁體中文解釋。
- 保留正確的英文技術術語。
- 內容準確，避免捏造知識。
- 解釋盡量簡單易懂。
- 必要時使用具體例子。
- 程式碼必須符合所描述的概念。
- 不直接複製他人的完整教學文章。
- 不確定的資訊必須先確認，不可猜測。

## 10. Development Safety Rules

AI 修改網站時必須：

- 優先修改現有檔案，而不是重建整個網站。
- 保留原有筆記內容。
- 不任意修改 AGENTS.md。
- 不刪除其他頁面或檔案。
- 不使用不必要的外部依賴。
- 不引入需要付費的服務。
- 不修改與目前任務無關的內容。

若需要重大架構變動，必須先向使用者說明並取得同意。

## 11. Completion Checklist

每次新增或修改頁面後，AI 都必須確認：

- [ ] HTML 結構完整
- [ ] 網站風格與其他頁面一致
- [ ] 繁體中文顯示正常
- [ ] 首頁與筆記頁面連結正確
- [ ] CSS 路徑正確
- [ ] 電腦與手機版面可正常閱讀
- [ ] 沒有遺漏必要的筆記區塊
- [ ] 沒有不必要的檔案修改

專案使用相對路徑，確保 GitHub Pages 可以正常運作。

例如：
- 首頁使用 assets/style.css
- 筆記頁面使用 ../assets/style.css
- 筆記返回首頁使用 ../index.html
- 首頁連結筆記使用 notes/檔名.html

## 12. Definition of Done

只有符合以下條件，才視為任務完成：

1. 指定的頁面已成功建立或修改。
2. 頁面符合本文件所有適用規則。
3. 首頁能正確連結至新增的筆記。
4. 新頁面可以正常顯示內容。
5. 既有網站功能沒有受到影響。
6. AI 已向使用者說明修改結果。

## 13. Core Principle

本專案最重要的原則是：

"Create once, extend consistently."

每次新增內容時，AI 都應沿用既有結構、
模板與設計規則，讓網站能持續擴充，
而不需要重新規劃整個專案。
