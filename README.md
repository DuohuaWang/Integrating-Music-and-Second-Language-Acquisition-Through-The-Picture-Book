# Integrating Music and Second Language Acquisition Through The Picture Book
### The Very Hungry Caterpillar

這是純靜態網站，只有 HTML、CSS、JavaScript，不需要資料庫、後端或建置流程。
把整個資料夾原封不動上傳到任何免費代管平台就能運作，不需要 Claude 帳號。

---

## 檔案結構

```
.
├── index.html                  首頁（Project Overview、Lesson Plans、Interactive Tools、Want to say?）
├── pages/                      內容頁，每份都有英文版 -en 和中文版 -zh
│   ├── motivation-en.html      Motivation
│   ├── motivation-zh.html      研究動機
│   ├── framework-en.html       Lesson Plan Framework
│   ├── framework-zh.html       教案架構
│   ├── lesson1-en.html         Class Plan（教案一）
│   ├── lesson1-zh.html
│   ├── lesson2-en.html         Class Plan 2：從單字到句子（教案二）
│   └── lesson2-zh.html
├── tools/                      四個互動工具
│   ├── rhythm-vocab.html       Rhythm Finder · Vocab（Starter）
│   ├── rhythm-sentence.html    Rhythm Finder · Sentence（Advanced）
│   ├── flashcards.html         A very happy caterpillar 閃卡
│   └── puzzle.html             拼拼看！Syllable Puzzle
├── .nojekyll                   GitHub Pages 用，請保留
└── README.md                   這份說明
```

所有連結都是相對路徑，放在網域根目錄或子資料夾都能正常運作，不需要額外設定。
圖片都已經內嵌在 HTML 裡，沒有另外的圖片檔。

## 部署方式（三選一）

**Netlify（最快，不用帳號設定）**
1. 打開 app.netlify.com/drop。
2. 把整個 `site` 資料夾拖進網頁。
3. 上傳完就會給你網址，之後可以在設定裡改網址名稱。

**GitHub Pages**
1. 在 GitHub 開一個新的 repository。
2. 把這個資料夾裡的所有檔案上傳（保持資料夾結構）。
3. Settings → Pages → Source 選 `Deploy from a branch`，branch 選 `main`、資料夾選 `/ (root)`。
4. 幾分鐘後網址會是 `https://<帳號>.github.io/<repo 名稱>/`。

**Cloudflare Pages**
1. Workers & Pages → Create → Pages → Upload assets。
2. 拖進整個資料夾。

## 注意事項

- **字體**：首頁和拼圖用 Google Fonts，需要連網才會載入；沒網路時會用系統字體，不影響功能。
- **發音**：用的是瀏覽器內建的語音（Web Speech API），不同裝置的聲音會不一樣。
- **進度紀錄**（閃卡星號、拼圖完成、速度設定）存在每個人自己的瀏覽器裡，換裝置不會同步。
- **Want to say?**：會開啟訪客自己的信箱寄到 alice7220815@gmail.com，所以留言不會顯示在網頁上。
- **更新內容**：改完檔案後，重新上傳整個資料夾就好。
