# T00：準備 GitHub 帳號與操作環境

> 所屬階段：[回到第一階段：建立與取得 Repo](README.md) · [課程總覽](../../README.md)

## 任務目標

歡迎開始第一份講義！這一課我們會一起準備好 GitHub 帳號與操作環境：認識 GitHub 網頁版、在 VS Code 登入，並確認本機 Git 已可使用。準備妥當後，建立或複製儲存庫就會更順利。已經有帳號或安裝好工具的同學，可以直接檢查目前設定，不必重做。
- **Why or Why Not**: 完成環境與帳號的設定才能夠確保能正常使用VSCode來存取與使用GitHub資源。


## 學習重點

- **GitHub 帳號**：學會註冊、驗證電子郵件及登入，也了解基本的帳號安全設定。已經有帳號的話，登入並確認電子郵件已驗證即可。
- **GitHub 網頁版**：我們會一起看看首頁、個人帳號選單與儲存庫頁面。儲存庫（Repository，簡稱 Repo）可以管理專案檔案及其版本。
- **本機工具**：認識 Git、VS Code 和 GitHub 各自負責什麼：Git 在本機管理版本，VS Code 是編輯器，GitHub 提供遠端儲存庫與協作服務。
- **VS Code 帳號登入**：從帳戶選單開始登入 GitHub，在瀏覽器完成授權後，確認 VS Code 使用的是正確帳號。

## 實作練習

### 1. 註冊並登入 GitHub

1. 請先開啟 <a href="https://github.com/signup" target="_blank" rel="noopener noreferrer">GitHub 註冊頁面</a>，跟著畫面提示建立個人帳號，並完成電子郵件驗證。已經有帳號的話，開啟 <a href="https://github.com/" target="_blank" rel="noopener noreferrer">GitHub</a>，選擇 **Sign in**（登入）就可以了。
2. 登入後，請點選右上角的頭像，看看顯示的使用者名稱是否正確；接著選擇 **Your profile**（個人資料），熟悉一下自己的個人頁面。
3. 為了讓帳號更安全，老師建議啟用<a href="https://docs.github.com/zh/authentication/securing-your-account-with-two-factor-authentication-2fa/configuring-two-factor-authentication" target="_blank" rel="noopener noreferrer">雙重驗證</a>，並妥善保存復原資訊。密碼、驗證碼和復原碼都請自己保管，不要放進儲存庫。

如果你使用的是公司或學校管理的帳號，請依管理員提供的登入與安全設定方式操作；不確定時，先向管理員確認即可。

### 2. 認識 GitHub 網頁版

1. 請在新分頁開啟 <a href="https://github.com/" target="_blank" rel="noopener noreferrer">GitHub 首頁</a>，找找首頁、搜尋欄和右上角帳號選單在哪裡。
2. 接著看看公開範例儲存庫 <a href="https://github.com/octocat/Hello-World" target="_blank" rel="noopener noreferrer">octocat/Hello-World</a>，認識擁有者、儲存庫名稱、檔案清單和 README 說明。
3. 點開一個檔案讀讀看，再回到儲存庫首頁。這裡只要瀏覽就好，不需要建立或修改任何檔案。

不同語言或版本的網頁配置可能稍有不同；找不到相同文字時，留意相近的功能或圖示即可。

### 3. 確認 VS Code 與 Git

1. 除了VS Code之外，要與GitHub網路互通還需要灌Git。如果電腦還沒有 VS Code 或 Git，請分別到 <a href="https://code.visualstudio.com/" target="_blank" rel="noopener noreferrer">VS Code官網</a>和 <a href="https://git-scm.com/downloads" target="_blank" rel="noopener noreferrer">Git 下載頁面</a>，下載並安裝適合自己作業系統的版本。已經安裝好的話，可以直接進行下一步。
**一般的電腦請選x64或AMD64的版本；如果是Apple系列、SnapdragonX系列的ARM架構的機器，再選ARM64版本下載。**

2. 開啟 VS Code，從選單選擇 **Terminal → New Terminal**（終端機 → 新增終端機），接著輸入：

   ```sh
   git --version
   ```

3. 如果終端機顯示 Git 版本號，就代表 Git 已經可以使用了。如果看到找不到 `git` 的訊息也別擔心：先確認 Git 已安裝，再重新啟動 VS Code 試一次。
4. 開始提交版本前，還需要設定 Git 使用者名稱和提交電子郵件。老師建議先看看<a href="https://docs.github.com/zh/get-started/git-basics/set-up-git" target="_blank" rel="noopener noreferrer">GitHub 的 Git 設定說明</a>；這些資料會顯示在提交紀錄中，和 GitHub 帳號登入是不同的設定。

### 4. 在 VS Code 登入 GitHub

1. 在 VS Code 找到 **Accounts**（帳戶）圖示並點選，接著選擇以 GitHub 登入。不同版本或擴充功能的選項名稱和位置可能稍有不同，找不到時可以留意相近的登入選項。
2. VS Code 會提示你開啟瀏覽器。請登入剛才確認的 GitHub 帳號，先看清楚授權內容，再依畫面提示同意並返回 VS Code。
3. 回到 VS Code，再開啟 **Accounts** 選單，確認顯示的是正確的 GitHub 使用者名稱。如果不小心登入了另一個帳號，先登出，再用正確帳號登入即可。
4. 如果接下來要練習使用私人儲存庫，請先到 GitHub 確認帳號能存取它；不確定是否有操作權限時，向儲存庫擁有者確認就可以。

小提醒：VS Code 的 GitHub 登入和 Git 使用 HTTPS／SSH 連線時的認證不一定相同。之後 Clone、Push 或 Pull 若再次要求登入，依提示完成授權即可；請不要把密碼或權杖寫進專案檔案。

## 小測驗

在進入下一課之前，來試試看吧！請選出**一個**答案，再展開下方解答確認。

**問題：** 我已安裝 Git，想確認它能否在 VS Code 終端機中使用，應該輸入哪個指令？

- A. `git --version`
- B. `git clone`
- C. `git push`
- D. `git commit`

<details>
<summary>查看答案</summary>

答案是 **A. `git --version`**。如果終端機顯示 Git 版本號，就代表 Git 可以使用。`git clone` 用來複製儲存庫，`git push` 用來上傳提交，而 `git commit` 用來建立提交。

如果看到找不到 `git` 的訊息，請先確認 Git 已安裝，再重新啟動 VS Code 試一次。

</details>

## 完成檢查

- [ ] 我已登入 GitHub、完成電子郵件驗證，也知道自己的使用者名稱。
- [ ] 我能找到個人資料，並瀏覽範例儲存庫的檔案與 README。
- [ ] VS Code 終端機輸入 `git --version` 後，會顯示 Git 版本號。
- [ ] VS Code 的帳戶選單顯示我預期使用的 GitHub 帳號。
- [ ] 如果使用私人練習儲存庫，我已確認帳號有需要的存取與操作權限。
- [ ] 我了解 Git 提交作者資訊和 GitHub 帳號登入是不同的設定。

都確認好了嗎？很棒！完成以上檢查後，就可以接著進行 [T01：建立一個新的 Repo](T01-建立一個儲存庫.md)。如果還有項目沒完成，先回到對應步驟慢慢確認，不用急著往下走。
