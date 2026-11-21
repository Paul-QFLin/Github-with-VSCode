# GitHub with VS Code

以實作任務為主的 VS Code × GitHub 學習路徑，從建立 Repository 開始，逐步學會版本控制、跨電腦協作、分支管理與自動化。

## 學習方式

1. 先完成 [T00：準備 GitHub 帳號與操作環境](docs/01-基礎的儲存庫操作-repository-basics/T00-註冊Github與設定VSCode.md)，再依階段順序學習或選擇需要的主題。
2. 每項任務都有獨立的學習頁面，包含任務目標、學習重點、實作步驟與完成檢查。
3. 練習時請使用自己的測試 Repository；操作前先確認目前的資料夾、分支與遠端位置。

## 講義編寫原則

新增或更新課程講義時，請參考[《AI 講義編寫原則》](docs/AI講義編寫原則.md)，並沿用文件中的任務格式與縮寫約定。

## 課程目錄

| 階段 | 主題 | 任務 |
| --- | --- | --- |
| [第一階段：建立與取得 Repo](docs/01-基礎的儲存庫操作-repository-basics/README.md) | 入門 | [T00 準備帳號與操作環境](docs/01-基礎的儲存庫操作-repository-basics/T00-註冊Github與設定VSCode.md)<br>[T01 建立新的 Repo](docs/01-基礎的儲存庫操作-repository-basics/T01-建立一個儲存庫.md)<br>[T02 儲存庫的確認 Commit](docs/01-基礎的儲存庫操作-repository-basics/T02-提交Commit一個版本.md)<br>[T03 推送至遠端 Push 與從遠端拉取 Pull](docs/01-基礎的儲存庫操作-repository-basics/T03-推送至遠端Push與從遠端拉取Pull.md)<br>[T04 下載／複製 Repo](docs/01-基礎的儲存庫操作-repository-basics/T04-複製儲存庫.md)<br>[T05 在 VS Code 開啟 Repo](docs/01-基礎的儲存庫操作-repository-basics/T05-在編輯器開啟儲存庫.md) |
| [第二階段：基本版本控制](docs/02-版本控制-version-control/README.md) | 核心操作 | [T07 更新 GitHub 上的程式](docs/02-版本控制-version-control/T07-暫存變更.md)<br>[T08 建立版本紀錄](docs/02-版本控制-version-control/T08-提交變更.md)<br>[T09 Push 上傳本機版本](docs/02-版本控制-version-control/T09-推送變更.md)<br>[T10 Pull 取得最新版本](docs/02-版本控制-version-control/T10-拉取最新版本.md)<br>[T11 查看檔案差異](docs/02-版本控制-version-control/T11-檢視差異.md)<br>[T12 查看 Commit History](docs/02-版本控制-version-control/T12-查看提交紀錄.md) |
| [第三階段：檔案與 Repo 管理](docs/03-檔案與儲存庫管理-files-and-repositories/README.md) | 實務操作 | [T13 新增檔案](docs/03-檔案與儲存庫管理-files-and-repositories/T13-追蹤新檔案.md)<br>[T14 刪除或重新命名檔案](docs/03-檔案與儲存庫管理-files-and-repositories/T14-刪除與重新命名檔案.md)<br>[T15 設定 `.gitignore`](docs/03-檔案與儲存庫管理-files-and-repositories/T15-設定忽略檔案.md)<br>[T16 使用 Git Add 加入檔案](docs/03-檔案與儲存庫管理-files-and-repositories/T16-將檔案加入版本控制.md)<br>[T17 修改遠端位置](docs/03-檔案與儲存庫管理-files-and-repositories/T17-修改遠端網址.md)<br>[T18 將 Repo 複製到另一台電腦](docs/03-檔案與儲存庫管理-files-and-repositories/T18-複製到另一台電腦.md) |
| [第四階段：多電腦協同工作](docs/04-多電腦協同工作-multi-computer-workflow/README.md) | 實務應用 | [T19 在兩台電腦接續工作](docs/04-多電腦協同工作-multi-computer-workflow/T19-跨電腦接續工作.md)<br>[T20 同步多個專案](docs/04-多電腦協同工作-multi-computer-workflow/T20-管理多個儲存庫.md)<br>[T21 在另一台電腦取得最新程式](docs/04-多電腦協同工作-multi-computer-workflow/T21-在另一台電腦取得更新.md)<br>[T22 解決 Merge Conflict](docs/04-多電腦協同工作-multi-computer-workflow/T22-解決合併衝突.md)<br>[T23 同步 VS Code 環境](docs/04-多電腦協同工作-multi-computer-workflow/T23-同步編輯器環境.md) |
| [第五階段：分支與版本管理](docs/05-分支與版本管理-branches-and-releases/README.md) | 進階操作 | [T24 建立分支](docs/05-分支與版本管理-branches-and-releases/T24-建立開發分支.md)<br>[T25 切換分支](docs/05-分支與版本管理-branches-and-releases/T25-切換開發分支.md)<br>[T26 合併分支](docs/05-分支與版本管理-branches-and-releases/T26-合併分支.md)<br>[T27 Push 分支到 GitHub](docs/05-分支與版本管理-branches-and-releases/T27-推送分支.md)<br>[T28 建立 Pull Request](docs/05-分支與版本管理-branches-and-releases/T28-建立合併請求.md)<br>[T29 回復先前版本](docs/05-分支與版本管理-branches-and-releases/T29-還原與回復版本.md)<br>[T30 放棄未提交的修改](docs/05-分支與版本管理-branches-and-releases/T30-放棄未提交變更.md) |
| [第六階段：進階應用與自動化](docs/06-進階應用與自動化-advanced-and-automation/README.md) | 延伸學習 | [T31 移轉專案到另一個 Repo](docs/06-進階應用與自動化-advanced-and-automation/T31-移轉儲存庫.md)<br>[T32 使用 Issues 管理問題](docs/06-進階應用與自動化-advanced-and-automation/T32-管理問題.md)<br>[T33 使用 Projects 管理工作](docs/06-進階應用與自動化-advanced-and-automation/T33-管理專案工作.md)<br>[T34 撰寫專案說明文件](docs/06-進階應用與自動化-advanced-and-automation/T34-撰寫專案說明文件.md)<br>[T35 使用 Tags 與 Releases](docs/06-進階應用與自動化-advanced-and-automation/T35-標記與發布版本.md)<br>[T36 自動更新 GitHub](docs/06-進階應用與自動化-advanced-and-automation/T36-版本控制自動化.md)<br>[T37 使用 GitHub Actions](docs/06-進階應用與自動化-advanced-and-automation/T37-自動化工作流程.md) |

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

每個階段目錄都有階段導覽頁及該階段的任務文件。帳號設定已整合至 T00，因此不另設 T06。
