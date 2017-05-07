---
layout: page
title: Archive
permalink: /archive/
---

一覧
<div class="posts">
    <ul>
        {% for post in site.posts %}
            <li>
            <article class="post">
            <a href="{{ site.baseurl }}{{ post.url }}"><font size="3">{{ post.date | date: "%B %e, %Y" }}</font> : {{ post.title }}</a>
            </article>
            </li>
        {% endfor %}
    </ul>
</div>