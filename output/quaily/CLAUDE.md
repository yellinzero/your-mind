# Quaily Newsletter

## 定位

Quaily 平台的 Newsletter 写作区。

## 目录结构

```
quaily/
├── CLAUDE.md
├── published.md      # 发布记录
└── 文章标题/
    ├── 文章标题.md
    └── (图片资源)
```

## 格式规范

参考：`docs/references/output/quaily-format.md`

### YAML Frontmatter

```yaml
---
slug: article-slug          # URL 标识
datetime: YYYY-MM-DD HH:mm  # 发布时间（24小时制）
summary: 文章摘要
tags:
  - 标签1
theme: light|dark
cover_image_url: "![[图片名.png]]"
---
```

## 图片引用

使用 Obsidian wiki-link 格式：`![[图片名.webp]]`

## 工具

- Quaily Obsidian 插件（位于根目录 `.obsidian/plugins/quail/`）
