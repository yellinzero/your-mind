---
description: 加载 life-os/ 目录的完整上下文
allowed-tools: Read, Glob
---

# 加载知识库上下文

适用范围：`life-os/` 目录

加载 PKM 知识库的完整上下文，以便更好地协助后续操作。

## 执行步骤

1. 读取 `life-os/CLAUDE.md` 获取 vault 上下文
2. 读取目标文件了解当前方向：
   - `life-os/Goals/2025-2029/0. Five Year Plan.md`
   - `life-os/Goals/2025-2029/1. Yearly Goals.md`
   - `life-os/Goals/2025-2029/2. Monthly Goals.md`
3. 读取最近的每日笔记（过去 3-7 天）
4. 扫描活跃项目（`life-os/Projects/*/CLAUDE.md`）
5. 汇总当前状态

## 输出

加载完成后，输出简要概览：

```markdown
## 当前上下文已加载

### 长期方向
[3 年目标概要]

### 本月重点
[月度目标]

### 近期动态
[最近几天的主要活动]

### 活跃项目
- [项目列表及状态]

---
准备就绪，可以开始协助。
```

## 使用场景

- 开始新的工作会话时
- 需要全面了解当前状态时
- 在做重要决策前获取完整上下文

## 相关资源

- 规范文档：`docs/references/life-os/`
- 项目管理：`docs/references/life-os/project-management.md`
