---
layout: default
title: 首页
---

<div class="hero-section">
    <h1 class="hero-title">探索技术的深度</h1>
    <p class="hero-subtitle">记录学习心得，分享技术总结，让我们一起在代码的世界里不断钻研。</p>
    <a href="{{ '/notes' | relative_url }}" class="btn-primary">浏览笔记</a>
</div>

<h2 class="section-title">最新发布</h2>

{% if site.notes %}
    {% assign latest_notes = site.notes | sort: 'date' | reverse %}
    <div class="grid-2">
    {% for note in latest_notes limit:4 %}
        <article class="note-card">
            <div class="note-card-date">{{ note.date | date: "%Y-%m-%d" }}</div>
            <h3 class="note-card-title">{{ note.title }}</h3>
            <p class="note-card-excerpt">{{ note.excerpt | strip_html | truncate: 80 }}</p>
            <a href="{{ note.url }}" class="note-card-link">阅读全文</a>
        </article>
    {% endfor %}
    </div>
{% else %}
    <p>暂无笔记</p>
{% endif %}