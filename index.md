---
layout: default
title: 欢迎来到我的技术笔记博客
---

<div class="hero-section">
    <h1>欢迎来到我的技术笔记博客</h1>
    <p>这是一个基于 Jekyll 的现代化静态博客，专门用于托管和分享技术笔记。在这里，您可以记录学习心得、技术总结和项目经验。</p>
    <a href="/notes" class="cta-button">开始探索笔记 →</a>
</div>

<div class="feature-card">
    <h2>✨ 核心特性</h2>
    <ul>
        <li><strong>📝 Markdown 支持</strong>：使用 Markdown 编写笔记，简单易用</li>
        <li><strong>🚀 实时渲染</strong>：上传后自动生成静态网页</li>
        <li><strong>📱 响应式设计</strong>：在各种设备上都有良好的阅读体验</li>
        <li><strong>🔍 SEO 友好</strong>：支持搜索引擎优化</li>
        <li><strong>🎨 代码高亮</strong>：支持多种编程语言的语法高亮</li>
    </ul>
</div>

<div class="feature-card">
    <h2>🚀 快速开始</h2>
    <ol>
        <li>在 <code>_notes</code> 目录下创建新的 Markdown 文件</li>
        <li>使用 YAML front matter 添加元数据</li>
        <li>提交到 GitHub，GitHub Pages 会自动构建和部署</li>
    </ol>
</div>

<div class="notes-section">
    <h2>📚 最新笔记</h2>
    {% if site.notes %}
    {% assign latest_notes = site.notes | sort: 'date' | reverse %}
    <ul class="notes-list">
        {% for note in latest_notes limit:5 %}
        <li>
            <a href="{{ note.url }}">{{ note.title }}</a>
            <span style="color: #718096; font-size: 0.9rem;"> - {{ note.date | date: "%Y年%m月%d日" }}</span>
        </li>
        {% endfor %}
    </ul>
    {% else %}
    <p style="color: #718096; text-align: center; padding: 2rem;">暂无笔记，请添加您的第一篇技术笔记！</p>
    {% endif %}
    <div style="text-align: center; margin-top: 2rem;">
        <a href="/notes" class="cta-button">查看所有笔记</a>
    </div>
</div>