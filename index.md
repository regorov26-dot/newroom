---
layout: default
title: Выпуски
---
<h1>Выпуски</h1>
<p>Это простейший сайт. Статьи сгруппированы по выпуску (поле <code>issue</code> в шапке статьи).</p>

{% assign grouped = site.posts | group_by: "issue" %}
{% for group in grouped %}
  <h2>{{ group.name }}</h2>
  <ul>
  {% for post in group.items %}
    <li><a href="{{ post.url }}">{{ post.title }}</a>
      <small>— {{ post.date | date: "%d.%m.%Y" }}</small>
    </li>
  {% endfor %}
  </ul>
{% endfor %}
