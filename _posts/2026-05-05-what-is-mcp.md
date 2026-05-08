---
layout: page
title: "什么是 MCP？让 AI 真正看懂世界"
date: 2026-05-05
emoji: "🔌"
category: 学习
excerpt: "MCP（Model Context Protocol）是 Anthropic 推出的开放协议，让 AI 模型能够安全、标准化地连接外部工具和数据源。这篇笔记聊聊 MCP 是什么、为什么重要、以及如何开始使用。"
---

## 一句话理解 MCP

**MCP = AI 的「USB-C 接口」**

以前每个 AI 工具要单独对接 API —— 就像每个设备要配不同充电线。MCP 提供了一个标准协议，一次对接，所有兼容 MCP 的 AI 都能用。

## 核心概念

```
┌──────────┐     MCP      ┌──────────┐
│  AI Host │ ←──────────→ │  Server  │
│ (Claude) │   标准协议    │ (工具/DB) │
└──────────┘              └──────────┘
```

- **Host**: AI 应用（如 Claude Desktop）
- **Client**: Host 内部的 MCP 客户端
- **Server**: 暴露特定能力的服务（如文件系统、数据库、API）

## 为什么重要

1. **标准化** — 不用每个 AI 都重新发明轮子
2. **安全性** — 权限在 Server 侧控制
3. **可组合** — 不同 Server 可以组合使用

## 后续学习计划

- [ ] 搭建第一个 MCP Server
- [ ] 在 OpenClaw 中使用 MCP
- [ ] 了解社区热门 MCP Server
