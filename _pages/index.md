---
layout: page
title: Home
id: home
permalink: /
---

# 생각 정리를 위한 블로그 🌱

<p style="padding: 3em 1em; background: #f5f7ff; border-radius: 4px;">
  내가 사는 방식에 대한 생각을 정리하기 위한 블로그
</p>


<strong>최근 업데이트</strong>

<ul>
  {% assign recent_notes = site.notes | sort: "last_modified_at_timestamp" | reverse %}
  {% for note in recent_notes limit: 5 %}
    <li>
      {{ note.last_modified_at | date: "%Y-%m-%d" }} — <a class="internal-link" href="{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>

<style>
  .wrapper {
    max-width: 46em;
  }
</style>
