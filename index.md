---
layout: default
title: 뉴스 블로그
---

<h2>최신 기사 목록</h2>

<ul>
  {% for post in site.posts %}
    <li style="margin-bottom: 10px;">
      <a href="{{ post.url | relative_url }}" style="font-size: 18px; font-weight: bold;">
        {{ post.title }}
      </a>
      <span style="color: #888; font-size: 14px;">- {{ post.date | date: "%Y-%m-%d" }}</span>
    </li>
  {% else %}
    <li>등록된 기사가 없습니다.</li>
  {% endfor %}
</ul>
