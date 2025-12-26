# Life-OS - 人生规划系统

## 定位

这是基于 Obsidian 的人生规划系统，用于日常记录、目标追踪、项目管理。

## 目录结构

| 目录 | 用途 |
|------|------|
| `Daily Notes/` | 每日笔记（YYYY-MM-DD.md） |
| `Goals/` | 目标管理（按 5 年周期组织） |
| `Projects/` | 活跃项目（各有独立 CLAUDE.md） |
| `Templates/` | 可复用笔记模板 |
| `Inbox/` | GTD 待处理区 |
| `Archives/` | 已完成/归档内容 |

## 目标结构

目标按 5 年周期管理：

```
Goals/
├── [起始年]-[结束年]/          # 5 年周期
│   ├── 0. Five Year Plan.md    # 5 年愿景
│   ├── 1. Yearly Goals.md      # 年度目标
│   ├── 2. Monthly Goals.md     # 月度目标
│   └── 3. Weekly Review.md     # 周回顾
└── (下一个周期...)
```

每 5 年开启新的目录，保持历史周期可追溯。

## 规范文档

操作此目录时，请参考以下规范：

| 规范 | 路径 | 适用范围 |
|------|------|----------|
| Markdown 规范 | `docs/references/life-os/markdown-standards.md` | 所有 md 文件 |
| 生产力工作流 | `docs/references/life-os/productivity-workflow.md` | Goals/、Daily Notes/ |
| 项目管理 | `docs/references/life-os/project-management.md` | Projects/ |

## 可用命令

| 命令 | 用途 |
|------|------|
| `/daily` | 创建今日每日笔记 |
| `/weekly` | 运行周回顾流程 |
| `/onboard` | 加载完整上下文 |

## 可用技能

| 技能 | 用途 |
|------|------|
| `life-os-file-ops` | 读写 vault 文件、管理链接 |
| `daily-workflow` | 晨间/午间/晚间工作流 |
| `goal-tracking` | 目标进度追踪 |

## 可用代理

| 代理 | 用途 |
|------|------|
| `goal-aligner` | 分析活动与目标的对齐情况 |
| `weekly-reviewer` | 引导周回顾流程 |
| `note-organizer` | 整理笔记、修复链接 |
| `inbox-processor` | GTD 式处理 Inbox |

## 标签系统

- **优先级**: `#priority/high`, `#priority/medium`, `#priority/low`
- **状态**: `#active`, `#waiting`, `#completed`, `#archived`
- **场景**: `#work`, `#personal`, `#health`, `#learning`, `#family`

## 每日工作流

### 晨间 (5 分钟)
1. 运行 `/daily` 创建当日笔记
2. 确定 ONE Big Thing
3. 回顾昨日未完成任务
4. 设置时间块

### 晚间 (5 分钟)
1. 完成反思部分
2. 移动未完成任务
3. 运行 `/commit` 保存

### 周回顾 (周日，30 分钟)
1. 运行 `/weekly` 引导式回顾
2. 计算目标进度
3. 规划下周重点

## 个人覆盖

个人设置请创建 `CLAUDE.local.md`（已被 gitignore）。
