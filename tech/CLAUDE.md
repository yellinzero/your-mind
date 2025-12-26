# 技术模块 (tech/)

## 定位

卡片式技术知识库，用于记录遇到的技术问题和学习到的知识点。

## 卡片类型

| 类型 | 目录 | 用途 |
|------|------|------|
| **问题卡片** | `problems/` | 记录技术难点及解决方案 |
| **知识卡片** | `knowledge/` | 记录学习到的知识点 |

## 目录结构

```
tech/
├── CLAUDE.md           # 本文件
├── problems/           # 问题卡片
│   ├── tags.md         # 标签索引
│   └── YYYY-MM-DD-标题.md
└── knowledge/          # 知识卡片
    ├── tags.md         # 标签索引
    └── YYYY-MM-DD-标题.md
```

## 文件命名

- 格式：`YYYY-MM-DD-简短标题.md`
- 使用小写英文 + 连字符
- 示例：`2025-12-26-connection-pool-exhaustion.md`

## 创建卡片

使用 `/card` 命令快速创建：

```
/card problem [标题]    # 创建问题卡片
/card knowledge [标题]  # 创建知识卡片
/card                   # 交互式选择
```

## 审核卡片

完成卡片编写后，使用 `tech-reviewer` 技能进行审核：

```
帮我 review tech/problems/2025-12-26-xxx.md
```

审核会：
- 验证内容准确性
- 查找参考资料核实
- 指出错误或遗漏
- 提供改进建议

## 标签系统

每种卡片有独立的标签索引：
- 问题卡片：`problems/tags.md`
- 知识卡片：`knowledge/tags.md`

在卡片 frontmatter 中使用标签：

```yaml
tags: [高并发, 云服务器, 性能问题]
```

## 相关规范

→ `docs/references/tech/documentation-format.md`

## 可用命令

| 命令 | 用途 |
|------|------|
| `/card` | 创建技术卡片 |

## 可用技能

| 技能 | 用途 |
|------|------|
| `tech-reviewer` | 审核技术卡片 |
