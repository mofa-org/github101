# Git 常用命令指南 / Git Command Guide

这份指南包含了完成作业所需的常用 Git 命令。/ This guide contains common Git commands needed to complete the assignment.

## 基础配置 / Basic Configuration

```bash
# 设置用户名 / Set username
git config --global user.name "Your Name"

# 设置邮箱 / Set email
git config --global user.email "your.email@example.com"

# 查看配置 / View configuration
git config --list
```

## 克隆仓库 / Clone Repository

```bash
# 克隆你 Fork 的仓库 / Clone your forked repository
git clone https://github.com/your-username/github101.git

# 进入仓库目录 / Enter repository directory
cd github101
```

## 分支操作 / Branch Operations

```bash
# 查看所有分支 / View all branches
git branch -a

# 创建新分支 / Create new branch
git checkout -b feature-branch-name

# 切换分支 / Switch branch
git checkout branch-name

# 删除分支 / Delete branch
git branch -d branch-name
```

## 添加和提交 / Add and Commit

```bash
# 查看状态 / Check status
git status

# 添加文件 / Add files
git add filename.md
# 或添加所有文件 / Or add all files
git add .

# 提交更改 / Commit changes
git commit -m "Add: my bootcamp article"

# 修改上一次提交 / Amend last commit
git commit --amend
```

## 推送和拉取 / Push and Pull

```bash
# 推送到远程仓库 / Push to remote repository
git push origin branch-name

# 从远程仓库拉取 / Pull from remote repository
git pull origin branch-name

# 强制推送（慎用）/ Force push (use with caution)
git push -f origin branch-name
```

## 同步上游仓库 / Sync with Upstream

```bash
# 添加上游仓库 / Add upstream repository
git remote add upstream https://github.com/mofa-org/github101.git

# 查看远程仓库 / View remote repositories
git remote -v

# 从上游拉取最新代码 / Fetch latest code from upstream
git fetch upstream

# 合并上游代码到当前分支 / Merge upstream code to current branch
git merge upstream/main

# 或者使用 rebase / Or use rebase
git rebase upstream/main
```

## 查看历史 / View History

```bash
# 查看提交历史 / View commit history
git log

# 简洁方式查看 / View in concise format
git log --oneline

# 查看某个文件的历史 / View history of a file
git log filename.md

# 查看具体某次提交 / View specific commit
git show commit-hash
```

## 查看差异 / View Differences

```bash
# 查看未暂存的修改 / View unstaged changes
git diff

# 查看已暂存的修改 / View staged changes
git diff --cached

# 查看两个分支的差异 / View differences between branches
git diff branch1..branch2
```

## 撤销操作 / Undo Operations

```bash
# 撤销工作区的修改 / Discard changes in working directory
git checkout -- filename.md

# 取消暂存 / Unstage files
git reset HEAD filename.md

# 撤销最后一次提交（保留修改）/ Undo last commit (keep changes)
git reset --soft HEAD~1

# 撤销最后一次提交（丢弃修改）/ Undo last commit (discard changes)
git reset --hard HEAD~1
```

## 解决冲突 / Resolve Conflicts

```bash
# 当拉取或合并时遇到冲突 / When encountering conflicts during pull or merge
# 1. 查看冲突文件 / View conflicting files
git status

# 2. 打开冲突文件，手动解决冲突标记 / Open conflicting files and resolve conflict markers
# 冲突标记如下 / Conflict markers look like:
# <<<<<<< HEAD
# 你的修改 / Your changes
# =======
# 其他人的修改 / Other's changes
# >>>>>>> branch-name

# 3. 标记冲突已解决 / Mark conflicts as resolved
git add filename.md

# 4. 完成合并 / Complete merge
git commit -m "Resolve merge conflicts"
```

## 暂存工作 / Stash Work

```bash
# 暂存当前工作 / Stash current work
git stash

# 查看暂存列表 / View stash list
git stash list

# 恢复最近的暂存 / Apply most recent stash
git stash apply

# 恢复并删除最近的暂存 / Apply and drop most recent stash
git stash pop

# 删除所有暂存 / Clear all stashes
git stash clear
```

## 标签操作 / Tag Operations

```bash
# 创建标签 / Create tag
git tag v1.0.0

# 创建带说明的标签 / Create annotated tag
git tag -a v1.0.0 -m "Release version 1.0.0"

# 查看所有标签 / View all tags
git tag

# 推送标签到远程 / Push tags to remote
git push origin v1.0.0
# 推送所有标签 / Push all tags
git push origin --tags
```

## 常见问题解决 / Common Issues

### 提交信息写错了 / Wrong commit message

```bash
# 修改最后一次提交信息 / Amend last commit message
git commit --amend -m "Correct commit message"
```

### 提交了不该提交的文件 / Committed wrong files

```bash
# 从暂存区移除文件但保留在工作目录 / Remove from staging but keep in working directory
git rm --cached filename

# 然后提交 / Then commit
git commit -m "Remove file from tracking"
```

### 忘记创建分支，在 main 上直接修改了 / Made changes on main instead of a branch

```bash
# 创建新分支（会带着你的修改）/ Create new branch (will carry your changes)
git checkout -b new-branch-name

# 回到 main 分支 / Go back to main branch
git checkout main

# 重置 main 分支 / Reset main branch
git reset --hard origin/main
```

## 最佳实践 / Best Practices

1. **经常提交** / Commit frequently
   - 小步提交，每次提交只包含一个逻辑改动
   - Make small commits, each containing only one logical change

2. **写好提交信息** / Write good commit messages
   - 使用清晰、描述性的提交信息
   - Use clear, descriptive commit messages
   - 格式：`类型: 简短描述` (例如：`Add: article submission`, `Fix: typo in readme`)

3. **提交前检查** / Check before committing
   - 使用 `git status` 和 `git diff` 检查将要提交的内容
   - Use `git status` and `git diff` to review what you're about to commit

4. **保持仓库整洁** / Keep repository clean
   - 不要提交临时文件、编译产物等
   - Don't commit temporary files, build artifacts, etc.
   - 使用 `.gitignore` 忽略不需要的文件

5. **定期同步** / Sync regularly
   - 定期从上游仓库拉取最新代码
   - Regularly pull latest code from upstream repository

## 学习资源 / Learning Resources

- [Git 官方文档](https://git-scm.com/doc)
- [GitHub 文档](https://docs.github.com/cn)
- [Pro Git 书籍](https://git-scm.com/book/zh/v2)
- [Learn Git Branching](https://learngitbranching.js.org/)

---

💡 **提示**: 不确定某个命令的用法时，可以使用 `git help <command>` 查看帮助文档。

💡 **Tip**: When unsure about a command, use `git help <command>` to view help documentation.
