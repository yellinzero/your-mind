# 内容输出系统

## 定位

对外输出知识、分享内容的工作区。包含通稿和各平台专属内容。

## 目录结构

```
output/
├── universal/      # 通稿（跨平台通用内容）
├── quaily/         # Quaily Newsletter
├── xiaohongshu/    # 小红书
├── wechat/         # 微信公众号
├── substack/       # Substack
├── long-video/     # 长视频（B站/YouTube）
└── short-video/    # 短视频（抖音/Reels）
```

## 工作流

### 通稿模式

1. 在 `universal/` 创作内容
2. 根据目标平台格式调整
3. 复制到目标平台目录
4. 发布后记录到 `published.md`
5. 定期清理已发布原文

### 直接模式

1. 在目标平台目录直接创作
2. 发布后记录到 `published.md`
3. 定期清理已发布原文

## 各平台说明

| 目录 | 平台 | 内容类型 |
|------|------|----------|
| `universal/` | 通用 | 跨平台通稿 |
| `quaily/` | Quaily | Newsletter 长文 |
| `xiaohongshu/` | 小红书 | 图文笔记 |
| `wechat/` | 微信公众号 | 公众号文章 |
| `substack/` | Substack | Newsletter |
| `long-video/` | B站/YouTube | 长视频脚本 |
| `short-video/` | 抖音/Reels | 短视频脚本 |

## 可用工具

| 工具 | 用途 |
|------|------|
| `blog-assistant` skill | 根据主题生成文章提纲 |
| `/commit` command | 提交保存 |

## 引用资源

写作时可引用：
- `inspiration/` - 灵感素材
- `tech/` - 技术知识
- `life-os/` - 个人经验和思考
