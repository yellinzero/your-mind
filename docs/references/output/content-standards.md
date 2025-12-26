# 内容输出系统规范

本规范适用于 `output/` 目录下的所有内容创作。

## 目录结构

```
output/
├── universal/      # 通稿
├── quaily/         # Quaily Newsletter
├── xiaohongshu/    # 小红书
├── wechat/         # 微信公众号
├── substack/       # Substack
├── long-video/     # 长视频
└── short-video/    # 短视频
```

## 通用原则

### 文件组织

- 每篇内容一个文件夹（标题作为文件夹名）
- 主文件与文件夹同名
- 图片/资源放在同级目录

```
平台目录/
└── 内容标题/
    ├── 内容标题.md
    └── (资源文件)
```

### 发布记录

每个平台目录下维护 `published.md`，格式：

```markdown
# XX 发布记录

| 日期 | 标题 | 链接 | 备注 |
|------|------|------|------|
| 2025-01-01 | 文章标题 | https://... | |
```

### 内容清理

- 已发布内容定期清理原文
- 保留 `published.md` 作为历史记录
- 重要内容可保留在 `universal/` 作为通稿

## 工作流

### 通稿模式（推荐）

1. 在 `universal/` 创作内容
2. 完成后根据目标平台格式调整
3. 复制到目标平台目录
4. 发布后记录到两处 `published.md`
5. 定期清理已发布原文

### 直接模式

1. 直接在目标平台目录创作
2. 按平台格式要求编辑
3. 发布后记录到 `published.md`
4. 定期清理已发布原文

## 平台格式规范

| 平台 | 规范文档 |
|------|----------|
| Quaily | `docs/references/output/quaily-format.md` |
| 其他平台 | 参考各目录 `CLAUDE.md` |

## 引用资源

创作时可引用：
- `inspiration/` - 灵感素材
- `tech/` - 技术知识
- `news/` - 资讯内容
- `life-os/` - 个人经验
