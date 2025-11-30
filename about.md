---
layout: default
title: 关于
---

<div class="note-content">

# 关于这个博客

这是一个基于 Jekyll 构建的静态技术笔记博客，专门用于记录和分享技术学习过程中的心得体会。

## 技术栈

- **静态网站生成器**: Jekyll
- **样式**: 自定义 CSS
- **代码高亮**: Rouge
- **部署**: GitHub Pages

## 使用方法

### 1. 创建新笔记

在 `_notes` 目录下创建新的 Markdown 文件，文件名格式为：

```
YYYY-MM-DD-标题.md
```

### 2. 添加元数据

在每个笔记文件的开头添加 YAML front matter：

```yaml
---
layout: note
title: 笔记标题
date: YYYY-MM-DD
author: 作者名称
tags: [标签1, 标签2]
---
```

### 3. 编写内容

使用 Markdown 语法编写笔记内容，支持：

- 标题、列表、表格
- 代码块和语法高亮
- 图片和链接
- 数学公式（LaTeX）

### 4. 部署

将代码推送到 GitHub 仓库，启用 GitHub Pages 即可自动部署。

## 本地开发

如果您想在本地预览和测试：

```bash
# 安装依赖
bundle install

# 启动本地服务器
bundle exec jekyll serve

# 访问 http://localhost:4000
```

## 自定义

您可以根据需要修改以下文件来自定义博客：

- `_config.yml`: 博客配置
- `_layouts/`: 布局模板
- `assets/css/`: 样式文件
- `_notes/`: 笔记内容

## 许可证

本博客内容采用 [知识共享署名 4.0 国际许可协议](http://creativecommons.org/licenses/by/4.0/) 进行许可。

</div>