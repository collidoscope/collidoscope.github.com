---
published: true
layout: default
title: Blog
weight: 5
show: true
---

<h1>Mein Blog Space</h1>
<h2>Posts</h2>
<ul class="posts">{% for post in site.posts %}{% if post.published != false %}
<li>
  <span>
    {{ post.date | date_to_string }}
  </span>
  &raquo; <a href="{{ post.url }}">{{ post.title }}</a>
</li>
{% endif %}{% endfor %}</ul>
