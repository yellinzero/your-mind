# Quaily 文章格式规范

本规范适用于 `output/quaily/` 目录下的所有文章。

## 目录结构

每篇文章一个文件夹：

```
output/quaily/
├── 文章标题/
│   ├── 文章标题.md      # 主文件
│   └── images/          # 图片资源（可选）
│       └── *.png|*.webp
```

## YAML Frontmatter

每篇文章必须包含以下 frontmatter：

```yaml
---
slug: article-slug          # URL 标识，英文小写+下划线
datetime: YYYY-MM-DD HH:mm  # 发布时间
summary: 文章摘要            # 1-2 句话概括
tags:                       # 标签列表
  - 标签1
  - 标签2
theme: light|dark           # 主题色
cover_image_url: "![[图片名.png]]"  # 封面图（Obsidian 格式）
---
```

### 字段说明

| 字段 | 必填 | 说明 |
|------|------|------|
| `slug` | 是 | URL 路径标识，使用英文小写和下划线 |
| `datetime` | 是 | 发布日期时间 |
| `summary` | 是 | 文章摘要，用于预览和 SEO |
| `tags` | 是 | 分类标签，数组格式 |
| `theme` | 否 | 页面主题，默认 light |
| `cover_image_url` | 否 | 封面图片 |

## 图片引用

使用 Obsidian wiki-link 格式：

```markdown
![[图片名.webp]]
```

图片放在文章同级目录或 images 子目录。

## 写作风格

- 第一人称叙述
- 中文为主，技术术语可用英文
- 段落间空行分隔
- 适当使用引用块突出重点

## 示例

```markdown
---
slug: my_first_article
datetime: 2025-12-25 10:00
summary: 这是我的第一篇文章
tags:
  - 随笔
theme: light
---

正文内容...

![[示例图片.webp]]

更多内容...
```
