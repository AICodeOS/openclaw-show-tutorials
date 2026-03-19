# 龙虾秀 AI Agent 技能教程

> 🦞 [openclaw.show](https://openclaw.show) 的配套教程仓库

本仓库存放龙虾秀（OpenClaw Show）平台的 AI Agent 技能开发教程，前端运行时通过远程 fetch 加载这些内容。

## 目录结构

```
├── index.json              # 教程索引（标题、分类、slug）
├── tutorials/              # 教程 Markdown 文件
│   ├── getting-started.md
│   └── skill-development.md
└── README.md
```

## 本地开发

```bash
npx serve -p 4000 --cors .
```

启动后在 `http://localhost:4000` 提供静态文件服务，配合前端项目的 `VITE_DOCS_BASE_URL=http://localhost:4000` 使用。

## 如何贡献新教程

1. 在 `tutorials/` 目录下编写 `.md` 文件
2. 在 `index.json` 中添加对应条目：

```json
{
  "title": "教程标题",
  "slug": "文件名（不含 .md）",
  "category": "分类名"
}
```

3. 提交后 GitHub Actions 会自动同步到阿里云 OSS

## 许可证

MIT
