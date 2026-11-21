# 常用 GitHub 指令

本文件整理這套講義可能實際操作或明確講解的 Git 與 GitHub 結合指令。前面的任務會以 VS Code 的介面為主，後面的任務再適度使用終端機。

遇到指令回覆出現錯誤時，先閱讀錯誤訊息並確認目前資料夾、儲存庫、分支與遠端位置，不要直接使用強制或破壞性的指令。

## 1. 準備環境與取得專案

| 指令 | 用途 | 主要關聯的講義 |
| --- | --- | --- |
| `git --version` | 確認 Git 是否已安裝並可在終端機使用。 | [T00](01-基礎的儲存庫操作-repository-basics/T00-註冊Github與設定VSCode.md) |
| `git config --global user.name "使用者名稱"` | 設定所有本機儲存庫預設使用的提交作者名稱。 | [T00](01-基礎的儲存庫操作-repository-basics/T00-註冊Github與設定VSCode.md) |
| `git config --global user.email "電子郵件"` | 設定所有本機儲存庫預設使用的提交電子郵件。 | [T00](01-基礎的儲存庫操作-repository-basics/T00-註冊Github與設定VSCode.md) |
| `git config --get user.name` | 查看目前儲存庫或全域設定的使用者名稱。 | [T00](01-基礎的儲存庫操作-repository-basics/T00-註冊Github與設定VSCode.md) |
| `git config --get user.email` | 查看目前儲存庫或全域設定的提交電子郵件。 | [T00](01-基礎的儲存庫操作-repository-basics/T00-註冊Github與設定VSCode.md) |
| `git clone <儲存庫網址>` | 從 GitHub 取得或複製一份遠端儲存庫到本機。 | [T01](01-基礎的儲存庫操作-repository-basics/T01-建立一個儲存庫.md)、[T12](04-多電腦協同工作-multi-computer-workflow/T12-在不同電腦接續工作.md) |
| `git init` | 將目前資料夾初始化成本機 Git 儲存庫。講義以 VS Code 的 Initialize Repository 示範。 | [T01](01-基礎的儲存庫操作-repository-basics/T01-建立一個儲存庫.md) |

## 2. 檔案、暫存與提交

| 指令 | 用途 | 主要關聯的講義 |
| --- | --- | --- |
| `git status` | 查看目前分支、未追蹤檔案、未暫存修改、已暫存修改及合併狀態。 | [T02](01-基礎的儲存庫操作-repository-basics/T02-提交Commit一個版本.md)、[T04](02-版本控制-version-control/T04-衝突發生的處理.md)、[T09](03-檔案與儲存庫管理-files-and-repositories/T09-管理儲存庫中的檔案.md) |
| `git add <檔案或資料夾>` | 將指定修改加入下一次提交的暫存區。 | [T02](01-基礎的儲存庫操作-repository-basics/T02-提交Commit一個版本.md)、[T09](03-檔案與儲存庫管理-files-and-repositories/T09-管理儲存庫中的檔案.md) |
| `git add .` | 暫存目前資料夾中的變更，包括新檔案、修改與刪除；使用前先確認內容。 | [T02](01-基礎的儲存庫操作-repository-basics/T02-提交Commit一個版本.md)、[T09](03-檔案與儲存庫管理-files-and-repositories/T09-管理儲存庫中的檔案.md) |
| `git commit -m "提交訊息"` | 建立一個包含已暫存內容的本機版本。 | [T02](01-基礎的儲存庫操作-repository-basics/T02-提交Commit一個版本.md) |
| `git restore <檔案>` | 放棄尚未提交的工作區修改，使用前先確認會遺失的內容。 | [T06](02-版本控制-version-control/T06-回復與放棄修改.md) |
| `git restore --staged <檔案>` | 取消暫存，保留檔案目前的修改。 | [T06](02-版本控制-version-control/T06-回復與放棄修改.md) |
| `git rm <檔案>` | 從工作目錄刪除已追蹤檔案，並將刪除加入暫存區。 | [T09](03-檔案與儲存庫管理-files-and-repositories/T09-管理儲存庫中的檔案.md) |
| `git mv <原檔案> <新檔案>` | 移動或重新命名檔案，並將變更加入暫存區；Git 會依內容辨識是否顯示為重新命名。 | [T09](03-檔案與儲存庫管理-files-and-repositories/T09-管理儲存庫中的檔案.md) |
| `git status --ignored` | 查看一般變更及符合忽略規則的檔案。 | [T10](03-檔案與儲存庫管理-files-and-repositories/T10-忽略不需要追蹤的檔案.md) |
| `git check-ignore <檔案>` | 確認指定檔案是否符合忽略規則。 | [T10](03-檔案與儲存庫管理-files-and-repositories/T10-忽略不需要追蹤的檔案.md) |

在講義中，`git add`、暫存及 `git restore` 等操作會優先以 VS Code 的 Source Control 示範。

## 3. 查看修改與版本紀錄

| 指令 | 用途 | 主要關聯的講義 |
| --- | --- | --- |
| `git diff` | 查看工作區尚未暫存的修改。 | [T05](02-版本控制-version-control/T05-查看變更與版本紀錄.md) |
| `git diff --staged` | 查看已暫存、準備納入下一次提交的修改。 | [T05](02-版本控制-version-control/T05-查看變更與版本紀錄.md) |
| `git log` | 查看提交紀錄。 | [T05](02-版本控制-version-control/T05-查看變更與版本紀錄.md) |
| `git --no-pager log --oneline` | 不開啟分頁器，以簡短格式查看提交紀錄。 | [T05](02-版本控制-version-control/T05-查看變更與版本紀錄.md) |
| `git log --oneline --graph --decorate` | 查看簡短提交紀錄及分支、合併的呈現。 | [T07](02-版本控制-version-control/T07-建立切換與合併分支.md) |
| `git show <提交編號>` | 查看特定提交包含的內容。 | [T05](02-版本控制-version-control/T05-查看變更與版本紀錄.md)、[T06](02-版本控制-version-control/T06-回復與放棄修改.md) |

## 4. 上傳、下載與遠端位置

| 指令 | 用途 | 主要關聯的講義 |
| --- | --- | --- |
| `git push` | 把目前分支的本機提交上傳至遠端。 | [T03](01-基礎的儲存庫操作-repository-basics/T03-推送至遠端Push與從遠端拉取Pull.md)、[T12](04-多電腦協同工作-multi-computer-workflow/T12-在不同電腦接續工作.md) |
| `git pull --no-rebase` | 明確使用合併方式下載並整合遠端更新。 | [T03](01-基礎的儲存庫操作-repository-basics/T03-推送至遠端Push與從遠端拉取Pull.md)、[T04](02-版本控制-version-control/T04-衝突發生的處理.md)、[T12](04-多電腦協同工作-multi-computer-workflow/T12-在不同電腦接續工作.md) |
| `git fetch` | 取得遠端更新資訊，但先不自動合併到目前工作。 | [T12](04-多電腦協同工作-multi-computer-workflow/T12-在不同電腦接續工作.md) |
| `git remote -v` | 查看目前儲存庫的遠端名稱及網址。 | [T01](01-基礎的儲存庫操作-repository-basics/T01-建立一個儲存庫.md)、[T11](03-檔案與儲存庫管理-files-and-repositories/T11-管理遠端位置與移轉專案.md) |
| `git remote add <名稱> <網址>` | 新增一個遠端儲存庫位置。 | [T11](03-檔案與儲存庫管理-files-and-repositories/T11-管理遠端位置與移轉專案.md) |
| `git remote remove <名稱>` | 移除已設定的遠端位置。 | [T11](03-檔案與儲存庫管理-files-and-repositories/T11-管理遠端位置與移轉專案.md) |
| `git remote set-url <名稱> <新網址>` | 修改既有遠端的位置。 | [T11](03-檔案與儲存庫管理-files-and-repositories/T11-管理遠端位置與移轉專案.md) |

進入修改前，講義建議先 Fetch 或 Pull，再完成儲存、暫存、Commit，最後再 Push。這個流程可以降低衝突機會，但不能完全避免。

## 5. 衝突與合併

| 指令 | 用途 | 主要關聯的講義 |
| --- | --- | --- |
| `git status` | 確認衝突檔案及合併是否仍在進行。 | [T04](02-版本控制-version-control/T04-衝突發生的處理.md) |
| `git add <已處理的衝突檔案>` | 將處理完成的衝突檔案標記為已暫存。 | [T04](02-版本控制-version-control/T04-衝突發生的處理.md) |
| `git commit` | 完成合併提交，內容包含選定的衝突處理結果。 | [T04](02-版本控制-version-control/T04-衝突發生的處理.md) |
| `git merge --abort` | 如果確認要放棄目前的合併流程，回到合併前的狀態。 | [T04](02-版本控制-version-control/T04-衝突發生的處理.md) |

處理衝突時，不要先刪除或忽略標記，也不要使用強制推送。確認所有衝突區塊都已移除並儲存後，再暫存及提交。

## 6. 分支與 Pull Request

| 指令 | 用途 | 主要關聯的講義 |
| --- | --- | --- |
| `git branch` | 查看本機分支。 | [T07](02-版本控制-version-control/T07-建立切換與合併分支.md) |
| `git branch <分支名稱>` | 建立新的本機分支。 | [T07](02-版本控制-version-control/T07-建立切換與合併分支.md) |
| `git switch <分支名稱>` | 切換到既有分支。 | [T07](02-版本控制-version-control/T07-建立切換與合併分支.md) |
| `git switch -c <分支名稱>` | 建立並切換到新分支。 | [T07](02-版本控制-version-control/T07-建立切換與合併分支.md) |
| `git merge <分支名稱>` | 將指定分支的內容合併到目前分支。 | [T07](02-版本控制-version-control/T07-建立切換與合併分支.md) |
| `git push -u origin <分支名稱>` | 第一次將本機分支上傳到遠端並建立對應關係，以便在 GitHub 建立 Pull Request。 | [T08](02-版本控制-version-control/T08-使用Pull-Request協作.md) |
| `git branch -d <分支名稱>` | 在確認不再需要後刪除本機分支。 | [T07](02-版本控制-version-control/T07-建立切換與合併分支.md) |

講義主要先介紹分支與合併；Pull Request 則以 GitHub 網頁操作為主。

## 7. 回復與標記版本

| 指令 | 用途 | 主要關聯的講義 |
| --- | --- | --- |
| `git revert <提交編號>` | 建立一個新的提交來反轉指定提交，保留原本歷史。 | [T06](02-版本控制-version-control/T06-回復與放棄修改.md) |
| `git revert --no-edit <提交編號>` | 以 Git 預設訊息建立反向提交，不開啟提交訊息編輯器。 | [T06](02-版本控制-version-control/T06-回復與放棄修改.md) |
| `git reset --soft <提交編號>` | 移動到指定提交並保留暫存與工作區修改；屬於進階操作，使用前應理解影響。 | [T06](02-版本控制-version-control/T06-回復與放棄修改.md) |
| `git reset --mixed <提交編號>` | 移動到指定提交並保留工作區修改、取消暫存；使用前應理解影響。 | [T06](02-版本控制-version-control/T06-回復與放棄修改.md) |
| `git reset --hard <提交編號>` | 直接恢復指定提交並刪除相關未提交修改；本講義不建議初學者自行使用。 | [T06](02-版本控制-version-control/T06-回復與放棄修改.md) |
| `git tag <標籤名稱>` | 建立一個指向目前提交的輕量標籤。 | [T16](05-進階應用與自動化-advanced-and-automation/README.md#課程安排) |
| `git tag -a <標籤名稱> -m "標籤說明"` | 建立包含說明資訊的標籤。 | [T16](05-進階應用與自動化-advanced-and-automation/README.md#課程安排) |
| `git push origin <標籤名稱>` | 將指定標籤上傳至 GitHub。 | [T16](05-進階應用與自動化-advanced-and-automation/README.md#課程安排) |

回復工作時，優先使用建立新提交的方式保留歷史；只有確認資料不再需要時，才考慮放棄修改或使用較強的重設操作。

## 8. `.gitignore` 與忽略規則

`.gitignore` 是設定檔，不是單一的 Git 指令。講義會在 T10 說明如何建立及維護它：

```gitignore
# 依專案加入需要忽略的檔案或資料夾
*.log
.env
node_modules/
dist/
```

如果檔案已經被 Git 追蹤，修改 `.gitignore` 不會立刻停止追蹤；需要先確認專案需求，再視情況取消追蹤。
