---
layout: default
title: Jekyll博客搭建指南
date: 2024-11-23
author: manredeshanxiren
tags: [Jekyll, GitHub Pages, 教程]
---

# Jekyll博客搭建指南

本文记录如何使用Jekyll和GitHub Pages搭建个人技术博客。

## 环境准备

### 1. 安装Ruby和Jekyll

```bash
# 安装Ruby（macOS）
brew install ruby

# 安装Jekyll
gem install jekyll bundler
```

### 2. 创建新项目

```bash
# 创建新的Jekyll站点
jekyll new my-blog
cd my-blog

# 本地预览
bundle exec jekyll serve
```

## 项目结构

```
my-blog/
├── _config.yml      # 配置文件
├── _posts/          # 博客文章
├── _layouts/        # 布局模板
├── _includes/      # 可重用组件
├── assets/         # 静态资源
└── index.md        # 主页
```

## GitHub Pages部署

### 1. 创建GitHub仓库

- 仓库名格式：username.github.io
- 设置为公开仓库

### 2. 推送代码

```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/username/username.github.io.git
git push -u origin main
```

### 3. 启用GitHub Pages

1. 进入仓库设置
2. 选择Pages选项
3. 选择部署分支（通常为main）
4. 选择根目录（/）

## 自定义配置

### _config.yml示例

```yaml
title: 我的技术博客
description: 记录技术学习和实践
baseurl: ""
url: "https://username.github.io"

# 主题设置
theme: minima

# 插件
plugins:
  - jekyll-feed
  - jekyll-seo-tag

# 集合
collections:
  notes:
    output: true
    permalink: /notes/:path/
```

## 常用命令

```bash
# 本地开发
bundle exec jekyll serve

# 构建静态文件
bundle exec jekyll build

# 清理并重新构建
bundle exec jekyll clean && bundle exec jekyll build
```

## 注意事项

1. **文件命名**：使用YYYY-MM-DD-title.md格式
2. **Front Matter**：每个文件开头需要YAML元数据
3. **图片资源**：放在assets/images目录下
4. **自定义域名**：可配置CNAME文件指向自定义域名

## 总结

Jekyll + GitHub Pages是搭建个人技术博客的绝佳组合，具有以下优势：

- ✅ 完全免费
- ✅ 版本控制
- ✅ 自动部署
- ✅ 支持Markdown
- ✅ 高度可定制