# GitHub with VS Code

以實作任務為主的 VS Code × GitHub 學習路徑，從建立 Repository 開始，逐步學會版本控制、跨電腦協作、分支管理與自動化。

## 學習方式

1. 先完成 [T00：準備 GitHub 帳號與操作環境](docs/01-基礎的儲存庫操作-repository-basics/T00-註冊Github與設定VSCode.md)，再依階段順序學習或選擇需要的主題。
2. 第一階段 T00～T03、第二階段 T04～T08、第三階段 T09～T11、第四階段 T12～T13，以及第五階段 T14～T17 已有獨立講義；其他後續課程仍在規劃中。
3. 練習時請使用自己的測試 Repository；操作前先確認目前的資料夾、分支與遠端位置。
4. [常用 GitHub 指令](docs/常用GitHub指令.md)可隨時查閱本講義會使用的終端機指令。

<!--
## 講義編寫原則

新增或更新課程講義時，請參考[《AI 講義編寫原則》](docs/AI講義編寫原則.md)，並沿用文件中的任務格式與縮寫約定。
-->

## 課程目錄

| 階段 | 主題 | 任務 |
| --- | --- | --- |
| [第一階段：建立與取得儲存庫](docs/01-基礎的儲存庫操作-repository-basics/README.md) | 入門 | [T00 準備帳號與操作環境](docs/01-基礎的儲存庫操作-repository-basics/T00-註冊Github與設定VSCode.md)<br>[T01 建立新的 Repo](docs/01-基礎的儲存庫操作-repository-basics/T01-建立一個儲存庫.md)<br>[T02 儲存庫的確認 Commit](docs/01-基礎的儲存庫操作-repository-basics/T02-提交Commit一個版本.md)<br>[T03 推送至遠端 Push 與從遠端拉取 Pull](docs/01-基礎的儲存庫操作-repository-basics/T03-推送至遠端Push與從遠端拉取Pull.md) |
| [第二階段：版本檢視與協作](docs/02-版本控制-version-control/README.md) | 版本管理與協作 | [T04 Conflict 衝突發生的處理](docs/02-版本控制-version-control/T04-衝突發生的處理.md)<br>[T05 查看變更與版本紀錄](docs/02-版本控制-version-control/T05-查看變更與版本紀錄.md)<br>[T06 回復與放棄修改](docs/02-版本控制-version-control/T06-回復與放棄修改.md)<br>[T07 建立、切換與合併分支](docs/02-版本控制-version-control/T07-建立切換與合併分支.md)<br>[T08 使用 Pull Request 協作](docs/02-版本控制-version-control/T08-使用Pull-Request協作.md) |
| [第三階段：檔案與儲存庫管理](docs/03-檔案與儲存庫管理-files-and-repositories/README.md) | 實務操作 | [T09 管理儲存庫中的檔案](docs/03-檔案與儲存庫管理-files-and-repositories/T09-管理儲存庫中的檔案.md)<br>[T10 忽略不需要追蹤的檔案](docs/03-檔案與儲存庫管理-files-and-repositories/T10-忽略不需要追蹤的檔案.md)<br>[T11 管理遠端位置與移轉專案](docs/03-檔案與儲存庫管理-files-and-repositories/T11-管理遠端位置與移轉專案.md) |
| [第四階段：多電腦協同工作](docs/04-多電腦協同工作-multi-computer-workflow/README.md) | 實務應用 | [T12 在不同電腦接續工作](docs/04-多電腦協同工作-multi-computer-workflow/T12-在不同電腦接續工作.md)<br>[T13 同步 VS Code 操作環境](docs/04-多電腦協同工作-multi-computer-workflow/T13-同步VSCode操作環境.md) |
| [第五階段：進階應用與自動化](docs/05-進階應用與自動化-advanced-and-automation/README.md) | 延伸學習 | [T14 撰寫專案說明文件](docs/05-進階應用與自動化-advanced-and-automation/T14-撰寫專案說明文件.md)<br>[T15 使用 Issues 與 Projects 管理工作](docs/05-進階應用與自動化-advanced-and-automation/T15-使用Issues與Projects管理工作.md)<br>[T16 標記與發布版本](docs/05-進階應用與自動化-advanced-and-automation/T16-標記與發布版本.md)<br>[T17 使用 GitHub Actions 自動化工作](docs/05-進階應用與自動化-advanced-and-automation/T17-使用GitHub-Actions自動化工作.md) |

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
    └── 05-進階應用與自動化-advanced-and-automation/
```

T04 衝突處理已移至第二階段，分支與 Pull Request 也納入該階段；後續任務依序安排於第三至第五階段。
