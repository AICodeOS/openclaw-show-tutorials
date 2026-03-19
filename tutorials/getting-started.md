# 快速开始

欢迎使用 OpenClaw（龙虾）AI Agent 平台！本教程将帮助你快速上手。

## 安装

```bash
npm install -g openclaw-cli
```

## 初始化项目

```bash
openclaw init my-project
cd my-project
```

## 运行你的第一个技能

```bash
openclaw run --skill hello-world
```

运行后你会看到 Agent 自动执行任务的实时日志输出。

## 配置文件

在项目根目录创建 `openclaw.config.json`：

```json
{
  "name": "my-project",
  "skills": ["hello-world"],
  "env": {
    "API_KEY": "your-api-key"
  }
}
```

## 下一步

- 查看 [技能开发指南](/docs?slug=skill-development) 学习如何创建自定义技能
- 浏览 [技能商城](/skills) 发现更多现成技能
