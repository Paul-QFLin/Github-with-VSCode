# T00：準備 GitHub 帳號與操作環境

> 所屬階段：[回到第一階段：建立與取得 Repo](README.md) · [課程總覽](../../README.md)

## 任務目標

完成 GitHub 帳號註冊與電子郵件驗證，熟悉 GitHub 網頁介面，並在 VS Code 登入 GitHub、確認本機 Git 可用，以及帳號具有操作練習儲存庫的權限。完成後再進行 T01 建立或 T04 複製儲存庫等任務。

## 學習重點

- **GitHub 帳號**：註冊、驗證電子郵件、登入與帳號安全。若已有帳號，可直接登入並確認電子郵件已驗證。
- **GitHub 網頁版**：認識首頁、個人帳號選單與儲存庫頁面；儲存庫（Repository，簡稱 Repo）用來管理專案檔案及其版本。
- **本機工具**：Git 是本機版本控制工具；VS Code 是編輯器，GitHub 則提供遠端儲存庫與協作服務。
- **VS Code 帳號登入**：透過帳戶選單啟動 GitHub 登入，在瀏覽器完成授權，並核對登入帳號。

## 實作練習

### 1. 註冊並登入 GitHub

1. 開啟 [GitHub 註冊頁面](https://github.com/signup)，依畫面提示建立個人帳號，並完成電子郵件驗證。已有帳號者可到 [GitHub](https://github.com/) 選擇 **Sign in**（登入）。
2. 登入後，點選右上角的頭像，確認顯示的是預期的使用者名稱，再選擇 **Your profile**（個人資料）查看個人頁面。
3. 建議在帳號安全設定中啟用[雙重驗證](https://docs.github.com/zh/authentication/securing-your-account-with-two-factor-authentication-2fa/configuring-two-factor-authentication)，並安全保存復原資訊。不要將密碼、驗證碼或復原碼提交到儲存庫。

若使用公司或學校管理的帳號，請依管理員提供的登入與安全設定方式操作。

### 2. 認識 GitHub 網頁版

1. 回到 [GitHub 首頁](https://github.com/)，觀察首頁、搜尋欄與右上角帳號選單的位置。
2. 開啟公開範例儲存庫 [octocat/Hello-World](https://github.com/octocat/Hello-World)，查看擁有者、儲存庫名稱、檔案清單與 README 說明。
3. 點選一個檔案閱讀內容，再返回儲存庫首頁。此練習只需瀏覽，不必建立或修改任何檔案。

網頁的配置與文字可能因語言或版本而不同。

### 3. 確認 VS Code 與 Git

1. 若尚未安裝，請先從 [VS Code 官網](https://code.visualstudio.com/)及 [Git 下載頁面](https://git-scm.com/downloads)安裝適合自己作業系統的版本。
2. 開啟 VS Code，選擇 **Terminal → New Terminal**（終端機 → 新增終端機），輸入：

   ```sh
   git --version
   ```

3. 確認終端機顯示 Git 版本號。如果找不到 `git`，請確認已安裝 Git，重新啟動 VS Code 後再試。
4. 後續提交前，依 [GitHub 的 Git 設定說明](https://docs.github.com/zh/get-started/git-basics/set-up-git)設定 Git 使用者名稱與提交電子郵件。這些是提交紀錄的作者資訊，與 GitHub 帳號登入不同。

### 4. 在 VS Code 登入 GitHub

1. 在 VS Code 點選 **Accounts**（帳戶）圖示，選擇使用 GitHub 登入的選項。依版本或已安裝擴充功能不同，選項名稱與位置可能略有差異。
2. 依提示開啟瀏覽器，登入剛才確認的 GitHub 帳號，檢查授權要求後同意授權，並依提示返回 VS Code。
3. 再次開啟 **Accounts** 選單，確認已登入的 GitHub 使用者名稱正確。若登入錯誤帳號，請先登出，再以正確帳號重試。
4. 若練習使用既有的私人儲存庫，請在 GitHub 網頁確認此帳號可以存取該儲存庫，並向擁有者確認是否具有所需的操作權限。

VS Code 的 GitHub 登入與 Git 的 HTTPS／SSH 認證方式不一定相同。後續 Clone、Push 或 Pull 時若再次要求認證，請依提示完成授權；不要將密碼或權杖寫入專案檔案。

## 完成檢查

- [ ] 已登入 GitHub，電子郵件已驗證，並能辨識自己的使用者名稱。
- [ ] 能在網頁版找到個人資料，並瀏覽範例儲存庫的檔案與 README。
- [ ] VS Code 終端機的 `git --version` 顯示版本號。
- [ ] VS Code 的帳戶選單顯示正確的 GitHub 帳號。
- [ ] 使用既有私人練習儲存庫時，已確認帳號具有所需的存取與操作權限。
- [ ] 知道 Git 提交作者資訊與 GitHub 登入是不同的設定。

完成以上檢查後，可接著進行 [T01：建立一個新的 Repo](T01-建立一個儲存庫.md)。
