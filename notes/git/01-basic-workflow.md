# Git 基础工作流

Git 用来记录文件的变化历史。学习过程中，我需要养成小步提交的习惯。

## 日常命令

```bash
git status
git add .
git commit -m "docs: update linux notes"
git log --oneline
git diff
git push
```

## 基本流程

```text
修改文件
查看状态
git add 暂存
git commit 提交
git push 推送到 GitHub
```

## 第一原则

多运行 `git status`。

它能告诉我当前仓库处在什么状态，避免在不清楚的情况下乱操作。
