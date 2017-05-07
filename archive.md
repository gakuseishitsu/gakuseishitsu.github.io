---
layout: page
title: Archive
permalink: /archive/
---

一覧
<div class="posts">
  {% for post in site.posts %}
    <article class="post">

      <h1><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }} <font size="3">{{ post.date | date: "%B %e, %Y" }}</font></a></h1>
    </article>
  {% endfor %}
</div>