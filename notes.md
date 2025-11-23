---
layout: default
title: 技术笔记列表
---

# 技术笔记列表

这里是我所有的技术笔记，按时间倒序排列。

{% if site.notes %}
{% assign sorted_notes = site.notes | sort: 'date' | reverse %}

{% for note in sorted_notes %}
<div class="note-item">
    <h2><a href="{{ note.url }}">{{ note.title }}</a></h2>
    <div class="note-meta">
        <time datetime="{{ note.date | date_to_xmlschema }}">{{ note.date | date: "%Y年%m月%d日" }}</time>
        {% if note.author %}
            <span class="note-author">作者: {{ note.author }}</span>
        {% endif %}
        {% if note.tags %}
            <div class="note-tags">
                {% for tag in note.tags %}
                    <span class="tag">{{ tag }}</span>
                {% endfor %}
            </div>
        {% endif %}
    </div>
    {% if note.excerpt %}
        <p class="note-excerpt">{{ note.excerpt }}</p>
    {% endif %}
</div>
<hr>
{% endfor %}
{% else %}
<p>暂无技术笔记，请添加您的第一篇技术笔记！</p>
{% endif %}

<style>
.note-item {
    margin-bottom: 2rem;
}

.note-item h2 {
    margin-bottom: 0.5rem;
}

.note-item h2 a {
    text-decoration: none;
    color: #333;
}

.note-item h2 a:hover {
    color: #007bff;
}

.note-meta {
    color: #666;
    font-size: 0.9rem;
    margin-bottom: 0.5rem;
}

.note-author {
    margin-left: 1rem;
}

.note-tags {
    margin-top: 0.5rem;
}

.tag {
    background-color: #e9ecef;
    padding: 0.2rem 0.5rem;
    border-radius: 3px;
    margin-right: 0.5rem;
    font-size: 0.8rem;
    color: #666;
}

.note-excerpt {
    color: #666;
    font-style: italic;
}

hr {
    border: none;
    border-top: 1px solid #e9ecef;
    margin: 2rem 0;
}
</style>