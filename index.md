---
layout: default
title: Home
---

<div id="home">
  <h2>Recent Posts</h2>
    <ul class="posts">
      {% for post in site.posts %}
	<li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ post.url }}">{{ post.title }}</a></li>
      {% endfor %}
  </ul>
</div>
