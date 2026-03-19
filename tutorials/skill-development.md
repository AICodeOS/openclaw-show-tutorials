# 技能开发指南

学习如何为 OpenClaw 平台开发自定义 AI Agent 技能。

## 技能结构

每个技能是一个独立的目录，包含以下文件：

```
my-skill/
├── skill.json       # 技能元数据
├── index.ts         # 入口文件
├── actions/         # 动作定义
│   └── main.ts
└── tests/           # 测试
    └── main.test.ts
```

## 定义技能元数据

```json
{
  "name": "my-skill",
  "version": "1.0.0",
  "description": "我的第一个技能",
  "tags": ["自动化"],
  "author": "your-name"
}
```

## 编写技能逻辑

```typescript
import { defineSkill, Action } from 'openclaw-sdk'

export default defineSkill({
  name: 'my-skill',

  actions: [
    {
      name: 'greet',
      description: '发送问候',
      async execute(ctx) {
        const name = ctx.input.name || 'World'
        ctx.log(`Hello, ${name}!`)
        return { success: true, message: `Greeted ${name}` }
      },
    },
  ],
})
```

## 测试技能

```bash
openclaw test my-skill
```

## 发布到商城

```bash
openclaw publish my-skill
```

发布后，其他用户就可以在技能商城中找到并使用你的技能了。
