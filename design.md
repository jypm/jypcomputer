---
layout: default
title: 디자인/그래픽
---

<h2>🎨 디자인/그래픽 기사 목록</h2>

<ul>
  {% for post in site.categories['디자인/그래픽'] %}
    <li style="margin-bottom: 10px;">
      <a href="{{ post.url | relative_url }}" style="font-size: 18px; font-weight: bold;">
        {{ post.title }}
      </a>
      <span style="color: #888; font-size: 14px;">- {{ post.date | date: "%Y-%m-%d" }}</span>
    </li>
  {% else %}
    <li>등록된 디자인/그래픽 기사가 없습니다.</li>
  {% endfor %}
</ul>
