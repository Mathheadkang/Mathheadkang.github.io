---
layout: page
title: Blog
permalink: /blog/
---

Here are my research notes and articles:

<img src="{{ site.baseurl }}/assets/images/background.jpg" alt="background" width="200">

<ul>
  {% for post in site.posts %}
    <li>
      <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
      <h2>
        <a class="post-link" href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
      </h2>
    </li>
  {% endfor %}
</ul>
