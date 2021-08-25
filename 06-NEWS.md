---
layout: page
menutitle: NEWS
permalink: /news/
---


# News

<ul class="post-list">
  {% for post in site.posts limit:5 %}
  {% if post.type == "news" %}
  <li>
    <h2>{{ post.title }}
    <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span></h2>
    {{ post.content }}
  </li>
  {% endif %}
  {% endfor %}
</ul>



