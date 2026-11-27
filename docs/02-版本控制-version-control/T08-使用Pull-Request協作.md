# T08：使用 Pull Request 協作

> 所屬階段：[回到第二階段：版本檢視與協作](README.md) · [課程總覽](../../README.md)

## 任務目標

在 T07，我們練習了建立分支、在分支上提交修改，並合併回 `main`。這一課，老師會帶你把功能分支推送到 GitHub，建立 Pull Request（PR，拉取請求），讓修改內容可以先被檢視與討論，再合併回 `main`。

Pull Request 不是單純的「把程式拉下來」，而是提出一個整合修改的請求。建立 PR 後，可以查看差異與提交、留下討論、邀請有權限的協作者檢查；確認修改與檢查結果都符合需求後，才進行合併。合併後再把 GitHub 上的 `main` 拉回本機，確認取得整合結果。

請只在自己有權限操作的測試儲存庫練習。若這是正式或共用專案，請遵守專案的審查、核准及合併規則。
- **Why or Why Not**: Pull Request讓修改在合併前能被檢視、討論與審查，協助團隊確認內容符合需求，再安全地整合到目標分支。

## 學習重點

- **Pull Request**：請求將來源分支的修改整合到目標分支；例如把 `feature/pr-introduction` 合併進 `main`。
- **推送功能分支**：本機分支要先 Push 到 GitHub，才能從 GitHub 建立對應的 PR。
- **Base 與 Compare**：Base 是要接收修改的目標分支，Compare 是提供修改的來源分支。建立 PR 前要再次確認方向正確。
- **檢視 PR**：透過 **Conversation**、**Commits** 和 **Files changed** 查看討論、提交與檔案差異。
- **討論與審查**：使用留言提出問題、說明建議或回覆。Review 的 **Approve**（核准）應由其他有權限的協作者提出；PR 作者不能核准自己的 PR。
- **合併與取得結果**：PR 合併後，GitHub 的 `main` 才包含該分支的修改；本機要切回 `main` 並 Pull，才會取得合併後的內容。

## 實作練習

### 開始之前

請先完成第一階段 [T00](../01-基礎的儲存庫操作-repository-basics/T00-註冊Github與設定VSCode.md)～[T03](../01-基礎的儲存庫操作-repository-basics/T03-推送至遠端Push與從遠端拉取Pull.md)，以及本階段 [T04](T04-衝突發生的處理.md)～[T07](T07-建立切換與合併分支.md)。

在 VS Code 開啟一個自己有寫入權限的測試儲存庫，並在 <a href="https://github.com/" target="_blank" rel="noopener noreferrer">GitHub 網頁</a>開啟同一個儲存庫。確認目前位於 `main`、本機和 GitHub 已同步，而且 **Source Control**（原始檔控制）的 **Changes**（變更）與 **Staged Changes**（已暫存的變更）沒有其他工作。如果有未完成的修改或不確定的提交，先妥善保留並請老師協助，不要把不相關的內容一起提交或推送。

這次會新增專用練習檔 `pr-practice.md`。請勿在正式專案、共用專案或含有重要工作的儲存庫中練習。

### 1. 在 main 建立練習起點

1. 在 VS Code 檢查左下角的分支名稱，確認目前是 `main`。
2. 在檔案總管新增 `pr-practice.md`，輸入並儲存：

   ```text
   這是 Pull Request 練習的共同起點。
   ```

3. 在 **Source Control** 檢查變更，確認只有這個練習檔案。將它 Stage（暫存），以 `新增 Pull Request 練習檔案` 為訊息 Commit。
4. 依 [T03：推送至遠端 Push 與從遠端拉取 Pull](../01-基礎的儲存庫操作-repository-basics/T03-推送至遠端Push與從遠端拉取Pull.md) 的方式 Push `main`。回到 GitHub 確認檔案與提交已出現。

如果 Push 被拒絕，先閱讀提示並確認遠端更新；不要使用 Force Push（強制推送）。

### 2. 建立功能分支並完成修改

1. 依 [T07：建立、切換與合併分支](T07-建立切換與合併分支.md) 的方式，從 `main` 建立並切換到 `feature/pr-introduction`。建立後先確認 VS Code 左下角顯示的是這個分支。
2. 開啟 `pr-practice.md`，在共同起點後新增：

   ```text
   這一行透過 Pull Request 提出。
   ```

3. 儲存後，在 **Source Control** 檢查差異，確認只有預期的練習內容。將修改暫存，以 `在功能分支新增介紹` 為訊息 Commit。
4. 確認目前仍在 `feature/pr-introduction`，且沒有其他未完成的修改。在 VS Code 開啟終端機，確認目前資料夾是這個測試儲存庫，輸入：

   ```sh
   git push -u origin feature/pr-introduction
   ```

   `-u` 會在第一次推送時設定本機分支與遠端分支的對應關係；這樣該分支之後可以使用 VS Code 的 Push 操作。若要求登入或授權，確認使用的 GitHub 帳號及儲存庫後再依提示操作。
5. Push 完成後，在 GitHub 儲存庫的分支清單確認 `feature/pr-introduction` 已出現。這一步只把分支上傳，尚未將修改合併到 `main`。

如果推送失敗，先閱讀錯誤訊息並確認分支、遠端位置和權限；不要改推到 `main`，也不要使用強制推送。

### 3. 在 GitHub 建立 Pull Request

1. 在 GitHub 開啟測試儲存庫的 **Pull requests**，選擇 **New pull request**。若頁面出現「Compare & pull request」提示，也可以選擇它。
2. 在比較頁確認：
   - **base** 是 `main`，表示修改要合併進 `main`。
   - **compare** 是 `feature/pr-introduction`，表示修改來自功能分支。
3. 確認方向和儲存庫正確後，選擇 **Create pull request**。
4. 輸入標題 `新增分支介紹`，並在描述中說明這次做了什麼、希望檢查什麼。例如：

   ```text
   ## 修改內容
   - 在練習檔案新增一行介紹。

   ## 檢查重點
   - 確認新內容只出現在預期的檔案中。
   ```

5. 再次確認 Base 和 Compare，然後建立 PR。建立後，PR 頁面會顯示來源分支、目標分支、提交和檢查狀態。

### 4. 檢視修改並進行討論

1. 在 PR 的 **Commits** 頁籤確認 `在功能分支新增介紹` 已列出。
2. 在 **Files changed** 頁籤檢查差異：確認只修改了 `pr-practice.md`，且新增文字正確。檢視時若發現不熟悉或不預期的修改，先不要合併；回到 VS Code 確認來源並與協作者討論。
3. 在 **Conversation** 頁籤的留言區留下簡短問題或檢查紀錄，例如：`已確認這次只修改 pr-practice.md，新增內容符合練習目標。` 選擇 **Comment** 發布。這可練習在 PR 中留下討論；若有協作者，請邀請對方檢視並回覆。
4. 收到回覆或審查建議時，先確認問題與修改範圍。需要修改時，回到 VS Code 確認仍在 `feature/pr-introduction`，完成修改、檢查並 Commit，再 Push 同一個分支；PR 會自動更新。回到 **Files changed** 確認更新內容後，再回覆討論。
5. 若有其他有權限的協作者，請在 PR 選擇 **Reviewers** 邀請對方。協作者可依專案規則留下 **Comment**、**Request changes**（要求修改）或 **Approve**（核准）。作為 PR 作者，你可以留言與回覆，但不能核准自己的 PR；不要以作者身分代替協作者核准。

### 5. 確認並合併 Pull Request

合併前，請逐項確認：

- 目標儲存庫和分支正確，Base 是 `main`，Compare 是 `feature/pr-introduction`。
- **Files changed** 中只有預期的修改，內容已檢查。
- 討論或協作者提出的問題已處理，且符合儲存庫要求的審查與檢查狀態。

確認後，在 PR 頁面選擇 **Merge pull request**，依 GitHub 提示確認合併。GitHub 的按鈕、可選合併方式及是否需要審查，可能依儲存庫設定不同；若合併按鈕無法使用、檢查失敗、要求尚未取得的核准，或提示有衝突，先停止並遵守專案規則，不要嘗試繞過保護設定。遇到衝突可參考 [T04：衝突發生的處理](T04-衝突發生的處理.md)。

合併成功後，確認 PR 顯示已合併，並在 GitHub 的 `main` 檢查 `pr-practice.md` 已包含新增文字。

### 6. 將合併結果取得到本機

1. 回到 VS Code，確認 **Source Control** 沒有未提交或未暫存的修改。若工作目錄有其他工作，先妥善保留，不要直接丟棄。
2. 切換到本機 `main`，確認左下角顯示 `main`。
3. 依 T03 的方式在 VS Code 選擇 **... → Pull**，或在終端機確認位於正確儲存庫後輸入：

   ```sh
   git pull --no-rebase
   ```

4. Pull 完成後開啟 `pr-practice.md`，確認新增文字已在本機 `main`。在 GitHub 也確認 PR 已合併及 `main` 上的檔案內容，這表示協作流程已完成。

若遠端分支在 PR 合併後已刪除，仍可從 `main` Pull 合併結果；來源分支刪除不會撤銷已合併的修改。若 GitHub 提供 **Delete branch**，可以在確認 PR 已合併且結果正確後選擇刪除遠端練習分支；這是可選的清理步驟，不影響已合併的 `main`。

## 小測驗

在進入下一課之前，來試試看吧！請選出**一個**答案，再展開下方解答確認。

**問題：** 我已在功能分支完成修改並 Push，準備建立 PR，要如何設定來源與目標？

- A. Base 選功能分支，Compare 選 `main`，這樣功能分支會收到 `main` 的修改。
- B. Base 選 `main`，Compare 選功能分支，讓功能分支的修改提出合併到 `main`。
- C. Base 和 Compare 都選 `main`，再由 GitHub 猜測來源分支。
- D. 先把功能分支直接改名為 `main`，就不需要 PR。

<details>
<summary>查看答案</summary>

答案是 **B**。Base 是接收修改的目標分支，Compare 是提供修改的來源分支。合併前也要檢查 PR 的檔案差異、討論和專案要求的審查狀態。

</details>

## 完成檢查

- [ ] 我已從 `main` 建立功能分支，並將它 Push 到 GitHub。
- [ ] 我知道 PR 的 Base 是目標分支，Compare 是來源分支。
- [ ] 我已在 PR 檢查提交與檔案差異，並留下或回覆討論。
- [ ] 我知道 PR 作者不能核准自己的 PR，審查需遵循儲存庫規則。
- [ ] 我已確認檢查與審查要求，並在 GitHub 合併 PR。
- [ ] 我已切換回本機 `main` 並 Pull，確認取得合併後的檔案內容。
- [ ] 我知道遇到檢查失敗、權限限制或合併衝突時應先停止確認，不繞過專案規則。

都確認好了嗎？很棒！你已經走過從功能分支提出修改、討論審查，到合併並取得結果的流程。準備好後，可以繼續[第三階段：檔案與 Repo 管理](../03-檔案與儲存庫管理-files-and-repositories/README.md)。
