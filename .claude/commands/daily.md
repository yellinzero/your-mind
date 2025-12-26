---
description: 创建今日的每日笔记（操作 life-os/ 目录）
allowed-tools: Read, Write, Bash, Glob
---

# 每日笔记创建

适用范围：`life-os/` 目录

从模板创建今天的每日笔记，如果已存在则打开。

## 执行步骤

1. 获取今天的日期（YYYY-MM-DD 格式）
2. 检查 `life-os/Daily Notes/{date}.md` 是否存在
3. 如果不存在：
   - 读取 `life-os/Templates/Daily Template.md`
   - 替换模板变量（{{date}} 等）
   - 写入 `life-os/Daily Notes/{date}.md`
4. 显示今日笔记内容
5. 提示用户设置今日的 ONE Big Thing

## 模板变量

- `{{date}}` - 今天日期 YYYY-MM-DD
- `{{date:format}}` - 格式化日期
- `{{date-1}}` - 昨天日期
- `{{date+1}}` - 明天日期

## 相关资源

- 模板：`life-os/Templates/Daily Template.md`
- 规范：`docs/references/life-os/productivity-workflow.md`

## 后续操作

创建完成后建议：
1. 确定今日的 ONE Big Thing
2. 回顾昨日未完成任务
3. 设置时间块
