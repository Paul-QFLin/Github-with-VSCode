# T17：使用 GitHub Actions 自動化工作

> 所屬階段：[回到第五階段：進階應用與自動化](README.md) · [課程總覽](../../README.md)

## 任務目標

在前面的課程，我們學會撰寫 README、管理 Issues 和發布版本。這一課，老師會帶你認識 GitHub Actions，建立一個簡單的工作流程：當 `main` 有新提交，或你手動啟動流程時，自動確認儲存庫中的 `README.md` 存在且不是空檔案。

GitHub Actions 會依照 Workflow（工作流程）中的觸發條件執行工作。這次的範例只讀取檔案，不會修改或推送任何內容，也不需要設定密碼或權杖。

## 學習重點

- **Workflow（工作流程）**：放在 `.github/workflows/` 的 YAML 設定檔，描述何時以及如何執行自動化工作。
- **Event（事件）**：觸發 Workflow 的情況，例如 Push 到 `main` 或手動啟動。
- **Job（工作）和 Step（步驟）**：Job 是一組執行工作，Step 則是 Job 中依序執行的動作或指令。
- **Actions（動作）**：可在 Workflow 中使用的步驟，例如取回儲存庫檔案。
- **執行結果**：可在 GitHub 的 **Actions** 頁面查看每次執行狀態和步驟紀錄。
- **最小權限**：Workflow 只取得完成任務所需的權限。本課設定為唯讀，不使用 Secrets（祕密）或自動提交。

## 實作練習

### 開始之前

請先完成第一階段 [T00](../01-基礎的儲存庫操作-repository-basics/T00-註冊Github與設定VSCode.md)～[T03](../01-基礎的儲存庫操作-repository-basics/T03-推送至遠端Push與從遠端拉取Pull.md)，第二階段 [T04](../02-版本控制-version-control/T04-衝突發生的處理.md)～[T08](../02-版本控制-version-control/T08-使用Pull-Request協作.md)，第三階段 [T09](../03-檔案與儲存庫管理-files-and-repositories/T09-管理儲存庫中的檔案.md)～[T11](../03-檔案與儲存庫管理-files-and-repositories/T11-管理遠端位置與移轉專案.md)，第四階段 [T12](../04-多電腦協同工作-multi-computer-workflow/T12-在不同電腦接續工作.md)～[T13](../04-多電腦協同工作-multi-computer-workflow/T13-同步VSCode操作環境.md)，以及第五階段 [T14](T14-撰寫專案說明文件.md)～[T16](T16-標記與發布版本.md)。

使用自己的私人測試儲存庫，例如 T14 的 `readme-practice`。在 VS Code 開啟該儲存庫，確認資料夾與分支正確，並檢查 **Source Control**（原始檔控制）的 **Changes**（變更）和 **Staged Changes**（已暫存的變更）。若有未完成的工作，先妥善保留。

GitHub Actions 可能依帳號、儲存庫或組織設定而受限；若看不到 **Actions** 頁面或無法執行 Workflow，先確認功能是否啟用及自己是否有權限，不要嘗試繞過管理設定。

### 1. 建立 Workflow 檔案

1. 在 VS Code 檔案總管的儲存庫根目錄，建立資料夾 `.github`，再在其中建立 `workflows` 資料夾。
2. 在 `.github/workflows/` 中新增 `check-readme.yml`。請確認副檔名是 `.yml`，不要存成 `.yml.txt`。
3. 輸入以下內容並儲存：

   ```yaml
   name: README 檢查

   on:
     push:
       branches:
         - main
     workflow_dispatch:

   permissions:
     contents: read

   jobs:
     check-readme:
       runs-on: ubuntu-latest
       steps:
         - name: 取得儲存庫檔案
           uses: actions/checkout@v4
         - name: 確認 README 存在且非空
           run: test -s README.md
   ```

4. 看看各部分的意思：

   - `on` 設定觸發方式：Push 到 `main`，或手動啟動 `workflow_dispatch`。
   - `permissions` 將 `GITHUB_TOKEN` 的內容權限限制為 `read`（唯讀）。
   - `jobs` 定義要執行的工作；`runs-on` 指定 GitHub 提供的執行環境。
   - `actions/checkout` 取回儲存庫檔案；`test -s README.md` 檢查檔案存在且內容不是空的。

這個 Workflow 只檢查檔案，不會修改 README，也不會自動 Commit 或 Push。

### 2. 檢查並推送 Workflow

1. 回到 **Source Control**，確認只有 `.github/workflows/check-readme.yml` 是本次新增的檔案。若有其他變更，先檢查並妥善保留，不要一起提交。
2. 點選 Workflow 檔案檢查內容，確認事件、權限和檔名都正確。以 `新增 README 自動檢查流程` 為訊息 Commit。
3. 確認 Commit 完成後，依 T03 的方式 Push 到 GitHub。若 `main` 受保護，依 T08 透過 Pull Request 提交，不要繞過保護規則。
4. 回到 GitHub 儲存庫，確認 `.github/workflows/check-readme.yml` 已出現在檔案清單中。

### 3. 查看自動執行結果

1. 在 GitHub 儲存庫開啟 **Actions**，找到 **README 檢查** Workflow 和剛才的 Push 執行紀錄。
2. 點開執行紀錄，查看 Job `check-readme` 和兩個步驟。若兩步都完成，執行結果會顯示成功。
3. 若尚未看到執行紀錄，先確認 Workflow 檔案已 Push 到 `main`、YAML 路徑和檔名正確，以及儲存庫允許 Actions 執行。
4. 也可以從 **Actions** 頁面開啟 **README 檢查**，選擇 **Run workflow**（執行工作流程），確認使用 `main` 分支後手動執行。完成後查看這次手動執行的結果。

如果執行失敗，打開失敗的步驟閱讀訊息，檢查 `README.md` 是否存在且不為空，以及 Workflow 設定是否正確。先修正原因，再 Commit 和 Push；不要因為失敗就增加不必要的權限。

### 4. 了解自動化的權限與風險

- 本課使用 `permissions: contents: read`，只允許讀取儲存庫內容；不要為了讓範例執行而改成 `write-all`。
- 本課不需要 Secrets。不要把密碼、權杖或其他憑證寫進 YAML、README 或提交紀錄。
- GitHub Actions 會在執行環境中運行設定檔中的動作和指令。正式專案使用外部 Action 前，先確認來源、版本和專案政策。
- 自動修改或推送檔案會改變專案內容。若未來真的需要這類功能，應先明確確認需求，使用最小必要權限並遵守審查規則；不要在本練習中新增自動 Commit 或 Push。

GitHub 官方提供<a href="https://docs.github.com/en/actions/writing-workflows/quickstart" target="_blank" rel="noopener noreferrer">GitHub Actions 快速入門</a>和<a href="https://docs.github.com/en/actions/writing-workflows/workflow-syntax-for-github-actions" target="_blank" rel="noopener noreferrer">Workflow 語法說明</a>，可在需要時查閱。

## 小測驗

在進入下一課之前，來試試看吧！請選出**一個**答案，再展開下方解答確認。

**問題：** 本課的 Workflow 只需要檢查 `README.md`，應該使用哪種權限設定？

- A. `permissions: write-all`，讓 Workflow 可以隨意修改整個儲存庫。
- B. `permissions: contents: read`，只給它讀取儲存庫內容的權限。
- C. 將 GitHub 密碼直接寫進 Workflow。
- D. 移除所有檢查，改用 Force Push。

<details>
<summary>查看答案</summary>

答案是 **B**。Workflow 只需要讀取 README，因此使用唯讀權限即可。不要為了單純檢查檔案而授予寫入權限或加入密碼。

</details>

## 完成檢查

- [ ] 我知道 Event、Workflow、Job 和 Step 分別代表什麼。
- [ ] 我已建立 `.github/workflows/check-readme.yml`，並了解它如何被 Push 或手動執行觸發。
- [ ] 我已將 Workflow 推送到測試儲存庫，並在 GitHub Actions 查看執行結果。
- [ ] 我知道本課 Workflow 只有唯讀權限，不會修改或推送檔案。
- [ ] 我知道不應將密碼或權杖寫入 Workflow，也不應授予自動化不必要的權限。

都確認好了嗎？很棒！你已經完成一個會自動檢查專案說明的安全範例，也知道要先確認自動化的觸發條件和權限。準備好後，可以依專案需要繼續調整或探索 GitHub Actions。
