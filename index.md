---
layout: default
title: 技术笔记
---

# 技术笔记

欢迎来到我的技术笔记博客，这里记录了我的学习心得和技术总结。

## 最新笔记

{% if site.notes %}
{% assign latest_notes = site.notes | sort: 'date' | reverse %}
<ul>
{% for note in latest_notes limit:5 %}
<li><a href="{{ note.url }}">{{ note.title }}</a> - {{ note.date | date: "%Y-%m-%d" }}</li>
{% endfor %}
</ul>
{% else %}
<p>暂无笔记</p>
{% endif %}

[查看所有笔记 →](/notes)