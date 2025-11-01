# 贡献指南 / Contributing Guide

欢迎参加商业训练营的GitHub基础课作业！/ Welcome to the Business Bootcamp GitHub Basics assignment!

## 作业要求 / Assignment Requirements

### 1. Fork 仓库 / Fork the Repository

首先，Fork `github.com/mofa-org/github101` 到你自己的 GitHub 账号。

First, fork `github.com/mofa-org/github101` to your own GitHub account.

### 2. 提交文章 / Submit an Article

以 Markdown 格式（.md）提交一篇文章，内容可以是：
- 训练营的想法和感受
- 组队的想法
- 学习笔记
- 其他相关内容

Submit an article in Markdown format (.md) about:
- Your thoughts about the bootcamp
- Ideas about team formation
- Learning notes
- Other relevant content

**重要 / Important**: 请使用你的 GitHub 用户名命名文件 / Please name the file using your GitHub username

例如 / Example: `zhangsan.md`

将文件提交到 `submissions/` 目录下。

Submit the file to the `submissions/` directory.

### 3. 创建 Issues / Create Issues

至少给其他同学的 3 个 repo 各提 1 个 issue。Issue 应该是有意义的，例如：
- 建议改进
- 发现的问题
- 功能请求
- 文档改进建议

Create at least 1 issue on 3 other students' repos. Issues should be meaningful, such as:
- Suggestions for improvement
- Problems found
- Feature requests
- Documentation improvement suggestions

### 4. 给予 Stars / Give Stars

给其他同学的 repo 10 个 stars，互相支持！

Give 10 stars to other students' repos to support each other!

### 5. 解决 Issue / Resolve an Issue

解决自己 Repo 至少一个 issue。这可以是：
- 他人提出的 issue
- 你自己创建的改进任务

Resolve at least 1 issue on your own repo. This can be:
- Issues raised by others
- Improvement tasks you created yourself

### 6. 获得 Stars / Get Stars

想办法为自己的 Repo 获得十个点赞。

Find ways to get ten stars for your repo.

### 7. 提交 Pull Request / Submit a Pull Request

完成文章后，向原始仓库（upstream）提交 Pull Request。

After completing your article, submit a Pull Request to the original repository (upstream).

## 提交步骤 / Submission Steps

### 步骤 1: Clone 你 Fork 的仓库 / Step 1: Clone Your Forked Repository

```bash
git clone https://github.com/你的用户名/github101.git
cd github101
```

### 步骤 2: 创建新分支 / Step 2: Create a New Branch

```bash
git checkout -b add-my-article
```

### 步骤 3: 复制模板并编辑 / Step 3: Copy Template and Edit

```bash
cp TEMPLATE.md submissions/你的用户名.md
# 使用你喜欢的编辑器编辑文件
# Edit the file with your favorite editor
```

### 步骤 4: 提交更改 / Step 4: Commit Changes

```bash
git add submissions/你的用户名.md
git commit -m "Add my bootcamp article"
git push origin add-my-article
```

### 步骤 5: 创建 Pull Request / Step 5: Create a Pull Request

1. 访问你 Fork 的仓库页面 / Visit your forked repository page
2. 点击 "Pull Request" 按钮 / Click the "Pull Request" button
3. 填写 PR 描述，说明你的文章内容 / Fill in the PR description explaining your article
4. 提交 PR / Submit the PR

## Pull Request 规范 / Pull Request Guidelines

你的 PR 标题应该遵循以下格式：

Your PR title should follow this format:

```
Add article: [你的用户名]
```

例如 / Example: `Add article: zhangsan`

PR 描述应该包含：

The PR description should include:

- 简要介绍文章内容 / Brief introduction to the article content
- 你从训练营学到了什么 / What you learned from the bootcamp
- （可选）你对课程的反馈 / (Optional) Your feedback on the course

## 注意事项 / Important Notes

1. 请确保你的 Markdown 文件格式正确 / Ensure your Markdown file is properly formatted
2. 文件名必须是你的 GitHub 用户名 / File name must be your GitHub username
3. 文件必须放在 `submissions/` 目录下 / File must be placed in the `submissions/` directory
4. 提交前请检查是否有拼写错误 / Check for spelling errors before submitting
5. 尊重他人，友善交流 / Be respectful and communicate kindly

## 需要帮助？/ Need Help?

如果你在提交过程中遇到问题，可以：

If you encounter problems during submission, you can:

1. 查看 [GitHub 文档](https://docs.github.com)
2. 在本仓库创建 Issue 寻求帮助
3. 向训练营导师咨询

Happy coding! 🚀
