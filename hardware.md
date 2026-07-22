---
layout: default
title: PC/하드웨어
---

<h2>💻 PC/하드웨어 기사 목록</h2>

<ul>
  {% assign has_post = false %}
  {% for post in site.posts %}
    {% capture post_cat %}{{ post.category }} {{ post.categories | join: " " }}{% endcapture %}
    {% if post_cat contains "하드웨어" or post_cat contains "PC" %}
      {% assign has_post = true %}
      <li style="margin-bottom: 10px;">
        <a href="{{ post.url | relative_url }}" style="font-size: 18px; font-weight: bold;">
          {{ post.title }}
        </a>
        <span style="color: #888; font-size: 14px;">- {{ post.date | date: "%Y-%m-%d" }}</span>
      </li>
    {% endif %}
  {% endfor %}

  {% if has_post == false %}
    <li>등록된 PC/하드웨어 기사가 없습니다.</li>
  {% endif %}
</ul>
