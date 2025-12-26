---
paths: "**/*.md"
---

# Vault 的 Markdown 规范

这些约定适用于 vault 内所有 Markdown 文件。

## 文件命名

- **每日笔记：** `YYYY-MM-DD.md`（例如：`2024-01-15.md`）
- **项目文件夹：** PascalCase（例如：`MyProject/`）
- **通用笔记：** kebab-case（例如：`meeting-notes.md`）
- **模板：** 首字母大写 + 空格（例如：`Daily Template.md`）

## 标题层级

- H1（`#`）只用于笔记标题——每个文件仅一个
- H2（`##`）用于主要章节
- H3（`###`）用于子章节
- 不要跳级（例如：禁止 H1 -> H3）

## 链接

### 内部链接（Wiki 风格）
```markdown
[[笔记名]]                    # 链接到笔记
[[笔记名|显示文本]]            # 使用别名显示
[[笔记名#标题]]                # 链接到标题
[[文件夹/笔记名]]              # 带路径的链接
```

### 外部链接
```markdown
[显示文本](https://url.com)
```

## 标签

### 标准标签层级
```
#priority/high
#priority/medium
#priority/low

#status/active
#status/waiting
#status/completed
#status/archived

#context/work
#context/personal
#context/health
#context/learning
#context/family
```

### 标签放置位置
- 在 YAML frontmatter 中：`tags: [tag1, tag2]`
- 行内：放在相关行或段落末尾

## 任务格式

```markdown
- [ ] 未完成任务
- [x] 已完成任务
- [ ] 带上下文的任务 #work @home
- [ ] 带截止日期的任务 📅 2024-01-20
```

## YAML Frontmatter

所有笔记都应包含 frontmatter：
```yaml
---
date: YYYY-MM-DD
tags: [relevant, tags]
status: active|completed|archived
---
```

## 文本格式

- **加粗**：强调与关键术语
- *斜体*：轻度强调
- `代码/命令`：命令、路径、技术术语
- > 引用块：重要提示/警告

## 列表

- 无序列表使用 `-`
- 有序列表使用 `1.`
- 嵌套条目缩进 2 个空格

## 代码块

使用带语言标识的围栏代码块：
```javascript
const example = "code";
```

## 最佳实践

1. 一段只讲一个核心点
2. 章节之间用空行分隔
3. 尽量把单行控制在 100 字符以内
4. 添加相关笔记链接
5. 填写有意义的 frontmatter
