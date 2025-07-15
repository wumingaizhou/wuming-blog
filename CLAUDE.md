# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 项目概述

这是一个基于Hugo的静态个人博客，使用PaperMod主题构建，部署在https://giserwu.top。

## 技术栈
- Hugo v0.148.0 (extended版本)
- 主题：PaperMod
- 部署：静态网站生成
- 语言：中文为主

## 目录结构
```
├── archetypes/          # 文章模板
├── content/            # 内容目录
│   ├── posts/         # 博客文章
│   ├── archives.md    # 归档页面
│   └── search.md      # 搜索页面
├── static/            # 静态资源
├── themes/            # 主题目录
│   └── PaperMod/      # PaperMod主题
├── hugo.toml          # 配置文件
└── public/            # 生成的静态文件
```

## 常用命令

### 开发服务器
```bash
hugo server -D  # 启动开发服务器，包含草稿文章
```

### 构建
```bash
hugo  # 构建静态网站到public目录
```

### 新建文章
```bash
hugo new posts/文章标题.md  # 创建新文章
```

### 清理构建
```bash
hugo --gc --minify  # 清理缓存并最小化构建
```

## 配置要点

### 主要配置 (hugo.toml)
- **baseURL**: https://giserwu.top
- **title**: 我的博客
- **theme**: PaperMod
- **分页**: 每页5篇文章
- **搜索**: 已启用JSON输出支持搜索功能
- **主题**: 支持自动/亮/暗色模式切换

### 功能特性
- ✅ 阅读时间显示
- ✅ 字数统计
- ✅ 文章导航
- ✅ 面包屑导航
- ✅ 代码复制按钮
- ✅ 目录生成
- ✅ 搜索功能
- ✅ 归档页面
- ✅ 标签系统
- ✅ 分类系统

### 社交链接
当前配置了GitHub链接：https://github.com/wumingaizhou

## 内容管理

### 文章格式
使用Markdown格式，头部包含YAML front matter：
```yaml
---
title: "文章标题"
date: 2025-07-09
draft: false
tags: ["标签1", "标签2"]
categories: ["分类"]
---
```

### 静态资源
静态图片等资源放在 `static/` 目录，可通过 `/路径` 访问。
示例：头像图片在 `static/data/face.png`，通过 `/data/face.png` 访问。

## 部署

网站已配置为静态生成，构建后的文件在 `public/` 目录，可直接部署到任何静态网站托管服务。