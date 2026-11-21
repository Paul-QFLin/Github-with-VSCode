# T15：使用 Issues 與 Projects 管理工作

> 所屬階段：[回到第五階段：進階應用與自動化](README.md) · [課程總覽](../../README.md)

## 任務目標

在 T14，我們練習了整理專案說明。這一課，老師會帶你用 GitHub Issues 記錄待辦工作或問題，再用 Projects 看板安排工作進度。透過清楚的標題和說明，自己或協作者可以知道要做什麼、目前進行到哪裡。

Issue 是工作紀錄與討論，不會直接修改專案檔案；Projects 則能把 Issues 集中整理。完成實際工作後，仍需依照專案流程 Commit、Push 或透過 Pull Request 分享修改。

## 學習重點

- **Issue**：記錄待辦事項、問題、建議或需要討論的工作。標題應清楚，內容可補充背景和完成條件。
- **Labels（標籤）**：協助分類 Issue，例如文件、錯誤或功能需求；選擇專案已使用的標籤，不確定時先確認。
- **Project（專案）**：將多個 Issues 和其他工作項目集中管理，可用表格或看板檢視進度。
- **Status（狀態）**：在看板上移動工作項目，例如待辦、進行中、已完成；狀態應反映實際進度。
- **Issue 與程式碼修改的差別**：建立或關閉 Issue 不會自動修改、提交或推送檔案。
- **專案權限與可見度**：在自己的測試儲存庫練習，建立 Project 前確認擁有者、可見度和分享對象。

## 實作練習

### 開始之前

請先完成第一階段 [T00](../01-基礎的儲存庫操作-repository-basics/T00-註冊Github與設定VSCode.md)～[T03](../01-基礎的儲存庫操作-repository-basics/T03-推送至遠端Push與從遠端拉取Pull.md)，第二階段 [T04](../02-版本控制-version-control/T04-衝突發生的處理.md)～[T08](../02-版本控制-version-control/T08-使用Pull-Request協作.md)，第三階段 [T09](../03-檔案與儲存庫管理-files-and-repositories/T09-管理儲存庫中的檔案.md)～[T11](../03-檔案與儲存庫管理-files-and-repositories/T11-管理遠端位置與移轉專案.md)，第四階段 [T12](../04-多電腦協同工作-multi-computer-workflow/T12-在不同電腦接續工作.md)～[T13](../04-多電腦協同工作-multi-computer-workflow/T13-同步VSCode操作環境.md)，以及 [T14：撰寫專案說明文件](T14-撰寫專案說明文件.md)。

請使用 T14 建立的 `readme-practice` 私人測試儲存庫，並在 <a href="https://github.com/" target="_blank" rel="noopener noreferrer">GitHub 網頁</a>登入有權限管理該儲存庫的帳號。確認儲存庫和擁有者正確；建立 Issue 或 Project 前，先確認它們的可見度符合練習需要。請勿在 Issue 或留言中寫入密碼、權杖或其他敏感資料。

如果儲存庫沒有 **Issues** 或 **Projects** 頁籤，可能是功能未啟用或帳號權限不足。先檢查儲存庫設定並向擁有者確認，不要在未授權的專案新增工作項目。

### 1. 建立 Issues 記錄工作

1. 在測試儲存庫開啟 **Issues**，選擇 **New issue**（新增 Issue）。
2. 建立第一個 Issue：

   - **Title（標題）**：`確認 README 的閱讀清單連結`
   - **Description（說明）**：`檢查 README 中的 reading-list.md 連結能否開啟，並記錄檢查結果。`

3. 建立第二個 Issue：

   - **Title（標題）**：`補充 README 的使用方式`
   - **Description（說明）**：`檢查使用方式是否清楚；如有遺漏，補上必要步驟並確認預覽結果。`

4. 建立前再次確認 Issue 所屬的儲存庫和內容，再選擇 **Submit new issue**（提交新 Issue）。
5. 回到 Issues 清單，確認兩項工作都已建立並各自有編號。若儲存庫已有合適的 Label，可以為 Issue 加上對應標籤；不確定標籤代表什麼時，先不要新增或套用。

### 2. 建立 Project 看板並加入 Issues

1. 在測試儲存庫開啟 **Projects**，選擇 **New project**（新增 Project）。若畫面提供範本，選擇 **Board**（看板）或相近的看板檢視。
2. 將 Project 命名為 `README 練習工作看板`。建立或設定可見度時，確認只分享給預期的對象；本練習建議使用私人 Project。
3. 查看看板上的 **Status**（狀態）欄。若有預設狀態，確認有待辦、進行中和已完成等狀態；若名稱不同，依畫面調整或使用最接近的狀態。
4. 在 Project 中選擇 **Add item**（新增項目）或相近選項，搜尋並加入剛才建立的兩個 Issue。確認每張卡片都連到 `readme-practice` 儲存庫的 Issue。
5. 若 Project 與 Issue 分屬不同擁有者，或畫面要求授權，先確認帳號權限與 Project 可見度；不確定時先取消，不要擴大分享範圍。

GitHub 的 Projects 介面可能因版本或擁有者設定而不同；如果看板不是預設檢視，可以從 Project 的檢視選單新增 Board 檢視。

### 3. 更新工作進度

1. 在 GitHub 開啟 `確認 README 的閱讀清單連結` Issue，依 T14 確認 README 的連結能開啟 `reading-list.md`。
2. 確認檢查已完成後，在 Issue 留下簡短結果，例如：`已確認 README 的閱讀清單連結可以開啟。` 再選擇 **Close issue**（關閉 Issue）。
3. 回到 Project 看板，將這張卡片的 **Status** 設為 **Done**（已完成）或相近狀態。若它已自動移到完成欄，檢查狀態正確即可。
4. 將 `補充 README 的使用方式` 卡片移到 **In Progress**（進行中）或相近狀態。此 Issue 仍保持開啟，表示工作尚未完成。
5. 回到 Issues 清單及 Project 看板，確認第一項工作已完成、第二項仍在進行中。

如果第二項工作實際上還沒開始，請將狀態留在待辦，不要只為了練習看板而標記成進行中。狀態要反映真實工作情況。

### 4. Issue 完成後仍要提交檔案修改

如果你真的依第二個 Issue 修改 README，回到 VS Code 確認正確的測試儲存庫，檢查差異並 Commit，再依專案使用方式 Push 或建立 Pull Request。完成後回到 GitHub 更新 Issue 討論和 Project 狀態，確認工作已實際完成再關閉 Issue。

建立 Project 或關閉 Issue 不會自動提交 README；反過來，提交檔案也不一定會自動更新 Project 狀態。除非專案已設定自動化規則，否則請自行確認兩邊進度一致。

## 小測驗

在進入下一課之前，來試試看吧！請選出**一個**答案，再展開下方解答確認。

**問題：** 我在 Project 看板上把一個 Issue 移到 Done，README 的檔案修改也會自動提交到 GitHub 嗎？

- A. 會，Project 狀態會自動建立 Commit。
- B. 不會；Issue 和 Project 用來記錄及整理工作，檔案修改仍需透過 Git 檢查、Commit 並 Push 或建立 Pull Request。
- C. 會，但只限私人儲存庫。
- D. 不會；Issue 不能用來追蹤文件工作。

<details>
<summary>查看答案</summary>

答案是 **B**。Issue 和 Project 協助記錄與追蹤工作，並不會自動修改或提交專案檔案。完成文件修改後，仍要依照 Git 和專案協作流程分享。

</details>

## 完成檢查

- [ ] 我已在測試儲存庫建立清楚描述工作的 Issues。
- [ ] 我已建立私人 Project 看板，並確認擁有者和可見度。
- [ ] 我已將 Issues 加入看板，並讓狀態反映實際進度。
- [ ] 我知道 Issue 和 Project 不會自動修改或提交檔案。
- [ ] 我知道完成實際工作後，還要依 Git 流程提交和分享修改，再更新 Issue 狀態。
- [ ] 我沒有在 Issue 或留言中放入密碼、權杖或其他敏感資料。

都確認好了嗎？很棒！你現在可以用 Issues 記錄工作，並用 Projects 整理進度。準備好後，可以繼續[第五階段 T16：標記與發布版本](README.md)。
