---
layout: page
title: "从 0 到 1 搭建个人知识网站"
date: 2026-05-07
emoji: "🌐"
category: 创作
excerpt: "用 GitHub Pages + Jekyll 搭建「知庚」个人知识库的全流程记录。从注册 GitHub、安装 Git 和 gh CLI，到推送代码、启用 Pages，一步步走过来。"
---

## 为什么做网站

需要一个**随时随地可访问、多 Agent 可读取**的知识沉淀空间。

对比了几个方案：

| 方案 | 成本 | 灵活度 | 选择 |
|------|------|--------|------|
| Notion | 免费 | 中 | ❌ 封闭 |
| Obsidian Publish | $8/月 | 高 | ❌ 付费 |
| GitHub Pages | **¥0** | 最高 | ✅ |

## 技术栈

```
GitHub Pages ← Jekyll ← Markdown ← Agent 生成
```

## 搭建步骤

1. **注册 GitHub** → 用户名 `zhoug`
2. **安装 Git** → 命令行版本控制
3. **安装 gh CLI** → GitHub 命令行工具
4. **创建仓库** → `zhoug/mw-learning`
5. **搭建 Jekyll** → 选择 minima 主题 + 自定义样式
6. **启用 Pages** → Settings → Pages → master 分支
7. **绑定域名** → `https://zhoug.github.io/mw-learning/`

## 踩坑记录

- `gh auth login` 多次超时 → 换 PAT token 方式
- GitHub Pages 404 → 添加 `index.html`
- 443 端口间歇不通 → 公司网络限制

## 关键收获

> 一个党务工作者，不写代码，靠 Agent 对话就搭出了网站。
> 
> 这就是 AI 时代的可能性。
