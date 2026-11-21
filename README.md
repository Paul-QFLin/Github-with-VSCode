# GitHub with VS Code

以實作任務為主的 VS Code × GitHub 學習路徑，從建立 Repository 開始，逐步學會版本控制、跨電腦協作、分支管理與自動化。

## 學習方式

1. 先完成 [T00：準備 GitHub 帳號與操作環境](docs/01-基礎的儲存庫操作-repository-basics/T00-註冊Github與設定VSCode.md)，再依階段順序學習或選擇需要的主題。
2. 第一階段的任務已有獨立講義；後續階段目前為重組後的課程規劃，講義將依序製作。
3. 練習時請使用自己的測試 Repository；操作前先確認目前的資料夾、分支與遠端位置。

## 講義編寫原則

新增或更新課程講義時，請參考[《AI 講義編寫原則》](docs/AI講義編寫原則.md)，並沿用文件中的任務格式與縮寫約定。

## 課程目錄

第一階段已涵蓋建立與複製儲存庫、Commit、Push、Pull 及衝突處理。後續任務以此為基礎，不再將這些操作拆成獨立入門課。

T05 以後的編號與主題為**新課程規劃**，尚未製作成完整講義；各階段頁面保留舊任務作為編寫參考，舊編號與新編號不互相對應。

| 階段 | 主題 | 任務 |
| --- | --- | --- |
| [第一階段：建立與取得 Repo](docs/01-基礎的儲存庫操作-repository-basics/README.md) | 入門 | [T00 準備帳號與操作環境](docs/01-基礎的儲存庫操作-repository-basics/T00-註冊Github與設定VSCode.md)<br>[T01 建立新的 Repo](docs/01-基礎的儲存庫操作-repository-basics/T01-建立一個儲存庫.md)<br>[T02 儲存庫的確認 Commit](docs/01-基礎的儲存庫操作-repository-basics/T02-提交Commit一個版本.md)<br>[T03 推送至遠端 Push 與從遠端拉取 Pull](docs/01-基礎的儲存庫操作-repository-basics/T03-推送至遠端Push與從遠端拉取Pull.md)<br>[T04 Conflict 衝突發生的處理](docs/01-基礎的儲存庫操作-repository-basics/T04-衝突發生的處理.md) |
| [第二階段：檢視與回復版本](docs/02-版本控制-version-control/README.md) | 版本管理 | T05 查看變更與版本紀錄<br>T06 回復與放棄修改 |
| [第三階段：檔案與 Repo 管理](docs/03-檔案與儲存庫管理-files-and-repositories/README.md) | 實務操作 | T07 管理儲存庫中的檔案<br>T08 忽略不需要追蹤的檔案<br>T09 管理遠端位置與移轉專案 |
| [第四階段：多電腦協同工作](docs/04-多電腦協同工作-multi-computer-workflow/README.md) | 實務應用 | T10 在不同電腦接續工作<br>T11 同步 VS Code 操作環境 |
| [第五階段：分支與版本管理](docs/05-分支與版本管理-branches-and-releases/README.md) | 協作操作 | T12 建立、切換與合併分支<br>T13 使用 Pull Request 協作 |
| [第六階段：進階應用與自動化](docs/06-進階應用與自動化-advanced-and-automation/README.md) | 延伸學習 | T14 撰寫專案說明文件<br>T15 使用 Issues 與 Projects 管理工作<br>T16 標記與發布版本<br>T17 使用 GitHub Actions 自動化工作 |

## 目錄結構

```text
.
├── README.md
└── docs/
    ├── AI講義編寫原則.md
    ├── 01-基礎的儲存庫操作-repository-basics/
    ├── 02-版本控制-version-control/
    ├── 03-檔案與儲存庫管理-files-and-repositories/
    ├── 04-多電腦協同工作-multi-computer-workflow/
    ├── 05-分支與版本管理-branches-and-releases/
    └── 06-進階應用與自動化-advanced-and-automation/
```

每個階段目錄都有階段導覽頁；後續階段的舊任務文件暫時保留，供重寫講義時參考。
