---
description: 暂存所有变更并生成提交（不推送）
allowed-tools:
  - Bash(git status:*)
  - Bash(git diff:*)
  - Bash(git add:*)
  - Bash(git commit:*)
  - Bash(git remote:*)
  - Bash(git branch:*)
  - Bash(git rev-parse:*)
  - Bash(git log:*)
---

按顺序执行以下步骤：

1. 检查当前是否在 Git 仓库中，并确认分支与工作区状态：
   - 运行 `git rev-parse --is-inside-work-tree`
   - 运行 `git status -sb`

2. 如果工作区没有任何变更（clean）：
   - 告知用户"没有需要提交的变更"，并询问下一步要做什么。

3. 生成变更摘要（用于提交信息与确认范围）：
   - 运行 `git diff --name-status`
   - 如需要更细节，再运行 `git diff`

4. 确定当前分支：
   - 运行 `git rev-parse --abbrev-ref HEAD`

5. 生成提交信息：
    - 提交信息必须符合 **Conventional Commits** 规范：
       - 基本格式：`<type>(<scope>): <subject>`
       - `scope` 可选；`subject` 用现在时/祈使语气、简洁明确，避免句号结尾。
    - 常用 `type`（本仓库以文档/笔记为主，通常用 `docs` / `chore`）：
       - `docs`: 文档/笔记/规范更新
       - `chore`: 工具/配置/脚本/工作流调整
       - `refactor`: 结构调整但不改变外部行为（例如整理目录结构但不改语义）
       - `fix`: 修正错误内容/链接/拼写
       - `feat`: 新增可用能力（例如新增一条可执行 command / 新模板）
    - `scope` 建议用改动所在的主目录/主题（择一即可）：`life-os`、`docs`、`claude`、`output`、`news`、`tech`、`inspiration`。
    - 若用户在执行 `/push` 时提供了自定义 message：
       - 先检查是否匹配 `^(feat|fix|docs|refactor|style|test|chore)(\([^)]+\))?(!)?: .+`
       - 若不匹配：停止并要求用户确认是否改为符合规范的提交信息。
    - 若用户未提供 message：
       - 基于第 3 步的变更摘要，自动生成一条**单行** Conventional Commit（仅 subject）
       - 示例：
          - `docs(life-os): 翻译 CLAUDE.local 模板为中文`
          - `chore(claude): 更新 push 命令为仅提交模式`
          - `fix(docs): 修复 life-os 参考文档中的失效链接`
    - 提交信息必须准确反映改动意图，避免空泛词（如 `WIP` / `update` / `changes`）。

6. 暂存所有变更：
   - 运行 `git add -A`
   - 再次运行 `git status -sb` 确认暂存结果。

7. 创建提交：
   - 运行 `git commit -m "{message}"`
   - 如果提示"nothing to commit"，说明没有可提交内容：停止并告知用户。

8. 最后输出一段简短总结：
   - 本次提交信息
   - 涉及的主要文件/目录
   - 提示用户可手动运行 `git push` 推送到远程
   - 询问用户接下来要处理什么
