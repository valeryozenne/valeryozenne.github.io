---
layout: page
menutitle: NEWS
permalink: /news/
---


# News (short version)


<ul class="news-feed">
      {% assign news_posts = site.posts | where: "type", "news" %}
      {% for post in news_posts %}
      <li class="news-item">
        <span class="news-date">{{ post.date | date: "%b %Y" }}</span>
        <span class="news-title">
          <a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
          {% assign title_down = post.title | downcase %}
          {% if title_down contains "joining" or title_down contains "welcome" %}
            <span class="news-badge news-badge--new">TEAM</span>
          {% elsif title_down contains "anr" or title_down contains "grant" or title_down contains "accepted" %}
            <span class="news-badge news-badge--grant">GRANT</span>
          {% elsif title_down contains "conference" or title_down contains "presenting" or title_down contains "attending" %}
            <span class="news-badge news-badge--conf">CONF</span>
          {% elsif title_down contains "release" or title_down contains "software" or title_down contains "code" %}
            <span class="news-badge news-badge--new">CODE</span>       
          {% endif %}
        </span>
      </li>
      {% endfor %}
</ul>


# News (long version)

<ul class="post-list">
  {% for post in site.posts %}
  {% if post.type == "news" %}
  <li>
    <h2>{{ post.title }}
    <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span></h2>
    {{ post.content }}
  </li>
  {% endif %}
  {% endfor %}
</ul>


<!---

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

-->

