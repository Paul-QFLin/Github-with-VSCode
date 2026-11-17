# GitHub with VS Code

以實作任務為主的 VS Code × GitHub 學習路徑，從建立 Repository 開始，逐步學會版本控制、跨電腦協作、分支管理與自動化。

## 學習方式

1. 依階段順序學習，或從下方目錄選擇需要的主題。
2. 每項任務都有獨立的學習頁面，包含任務目標、學習重點、實作步驟與完成檢查。
3. 練習時請使用自己的測試 Repository；操作前先確認目前的資料夾、分支與遠端位置。

## 課程目錄

| 階段 | 主題 | 任務 |
| --- | --- | --- |
| [第一階段：建立與取得 Repo](docs/01-repository-basics/README.md) | 入門 | [T01 建立新的 Repo](docs/01-repository-basics/T01-create-repository.md)、[T02 將資料夾建立成 Repo](docs/01-repository-basics/T02-initialize-repository.md)、[T03 將本機 Repo 上傳到 GitHub](docs/01-repository-basics/T03-publish-repository.md)、[T04 下載／複製 Repo](docs/01-repository-basics/T04-clone-repository.md)、[T05 在 VS Code 開啟 Repo](docs/01-repository-basics/T05-open-repository.md)、[T06 設定 GitHub 帳號](docs/01-repository-basics/T06-github-authentication.md) |
| [第二階段：基本版本控制](docs/02-version-control/README.md) | 核心操作 | [T07 更新 GitHub 上的程式](docs/02-version-control/T07-stage-changes.md)、[T08 建立版本紀錄](docs/02-version-control/T08-commit-changes.md)、[T09 Push 上傳本機版本](docs/02-version-control/T09-push-changes.md)、[T10 Pull 取得最新版本](docs/02-version-control/T10-pull-changes.md)、[T11 查看檔案差異](docs/02-version-control/T11-view-diff.md)、[T12 查看 Commit History](docs/02-version-control/T12-commit-history.md) |
| [第三階段：檔案與 Repo 管理](docs/03-files-and-repositories/README.md) | 實務操作 | [T13 新增檔案](docs/03-files-and-repositories/T13-track-new-files.md)、[T14 刪除或重新命名檔案](docs/03-files-and-repositories/T14-delete-rename-files.md)、[T15 設定 `.gitignore`](docs/03-files-and-repositories/T15-gitignore.md)、[T16 使用 Git Add 加入檔案](docs/03-files-and-repositories/T16-git-add.md)、[T17 修改遠端位置](docs/03-files-and-repositories/T17-change-remote-url.md)、[T18 將 Repo 複製到另一台電腦](docs/03-files-and-repositories/T18-clone-to-another-computer.md) |
| [第四階段：多電腦協同工作](docs/04-multi-computer-workflow/README.md) | 實務應用 | [T19 在兩台電腦接續工作](docs/04-multi-computer-workflow/T19-work-across-computers.md)、[T20 同步多個專案](docs/04-multi-computer-workflow/T20-manage-multiple-repositories.md)、[T21 在另一台電腦取得最新程式](docs/04-multi-computer-workflow/T21-fetch-pull-on-another-computer.md)、[T22 解決 Merge Conflict](docs/04-multi-computer-workflow/T22-resolve-merge-conflict.md)、[T23 同步 VS Code 環境](docs/04-multi-computer-workflow/T23-sync-vscode-environment.md) |
| [第五階段：分支與版本管理](docs/05-branches-and-releases/README.md) | 進階操作 | [T24 建立分支](docs/05-branches-and-releases/T24-create-branch.md)、[T25 切換分支](docs/05-branches-and-releases/T25-switch-branch.md)、[T26 合併分支](docs/05-branches-and-releases/T26-merge-branches.md)、[T27 Push 分支到 GitHub](docs/05-branches-and-releases/T27-push-branch.md)、[T28 建立 Pull Request](docs/05-branches-and-releases/T28-create-pull-request.md)、[T29 回復先前版本](docs/05-branches-and-releases/T29-restore-revert.md)、[T30 放棄未提交的修改](docs/05-branches-and-releases/T30-discard-changes.md) |
| [第六階段：進階應用與自動化](docs/06-advanced-and-automation/README.md) | 延伸學習 | [T31 移轉專案到另一個 Repo](docs/06-advanced-and-automation/T31-migrate-repository.md)、[T32 使用 Issues 管理問題](docs/06-advanced-and-automation/T32-manage-issues.md)、[T33 使用 Projects 管理工作](docs/06-advanced-and-automation/T33-manage-projects.md)、[T34 撰寫專案說明文件](docs/06-advanced-and-automation/T34-project-documentation.md)、[T35 使用 Tags 與 Releases](docs/06-advanced-and-automation/T35-tags-and-releases.md)、[T36 自動更新 GitHub](docs/06-advanced-and-automation/T36-git-automation.md)、[T37 使用 GitHub Actions](docs/06-advanced-and-automation/T37-github-actions.md) |

## 目錄結構

```text
.
├── README.md
└── docs/
    ├── 01-repository-basics/
    ├── 02-version-control/
    ├── 03-files-and-repositories/
    ├── 04-multi-computer-workflow/
    ├── 05-branches-and-releases/
    └── 06-advanced-and-automation/
```

每個階段目錄都有階段導覽頁及該階段的任務文件。任務編號沿用本頁的 T01–T37，方便查找與追蹤學習進度。
