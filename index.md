---
layout: default
title: 欢迎来到我的技术笔记博客
---

# 欢迎来到我的技术笔记博客

这是一个基于 Jekyll 的静态博客，专门用于托管和分享技术笔记。

## 特性

- 📝 **Markdown 支持**：使用 Markdown 编写笔记，简单易用
- 🚀 **实时渲染**：上传后自动生成静态网页
- 📱 **响应式设计**：在各种设备上都有良好的阅读体验
- 🔍 **SEO 友好**：支持搜索引擎优化
- 🎨 **代码高亮**：支持多种编程语言的语法高亮

## 快速开始

1. 在 `_notes` 目录下创建新的 Markdown 文件
2. 使用 YAML front matter 添加元数据
3. 提交到 GitHub，GitHub Pages 会自动构建和部署

## 最新笔记

{% if site.notes %}
{% assign latest_notes = site.notes | sort: 'date' | reverse %}
{% for note in latest_notes limit:5 %}
- [{{ note.title }}]({{ note.url }}) - {{ note.date | date: "%Y年%m月%d日" }}
{% endfor %}
{% else %}
- 暂无笔记，请添加您的第一篇技术笔记！
{% endif %}

[查看所有笔记 →](/notes)