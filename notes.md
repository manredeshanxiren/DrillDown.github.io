---
layout: default
title: 技术笔记列表
permalink: /notes/
---

<div class="hero-section" style="padding: 40px 0; text-align: left;">
    <h1 class="hero-title" style="font-size: 2.5rem; margin-bottom: 1rem;">所有笔记</h1>
    <p class="hero-subtitle" style="margin: 0; font-size: 1.1rem;">按时间倒序排列的技术积累。</p>
</div>

{% if site.notes %}
    {% assign sorted_notes = site.notes | sort: 'date' | reverse %}
    <div class="grid-2">
    {% for note in sorted_notes %}
        <article class="note-card">
            <div class="note-card-date">{{ note.date | date: "%Y-%m-%d" }}</div>
            <h3 class="note-card-title">{{ note.title }}</h3>
            <p class="note-card-excerpt">{{ note.excerpt | strip_html | truncate: 100 }}</p>
            
            {% if note.tags %}
            <div style="margin-bottom: 16px; display: flex; gap: 8px; flex-wrap: wrap;">
                {% for tag in note.tags %}
                    <span style="background: #f1f5f9; padding: 2px 8px; border-radius: 4px; font-size: 0.8rem; color: var(--text-muted);">#{{ tag }}</span>
                {% endfor %}
            </div>
            {% endif %}
            
            <a href="{{ note.url }}" class="note-card-link">阅读全文</a>
        </article>
    {% endfor %}
    </div>
{% else %}
    <div style="text-align: center; padding: 40px; color: var(--text-muted);">
        <p>暂无技术笔记，请添加您的第一篇技术笔记！</p>
    </div>
{% endif %}