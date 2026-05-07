---
layout: page
icon: fas fa-heart
order: 2
title: Life
---

{% assign life_posts = site.posts | where_exp: "post", "post.categories contains 'Life'" | sort: "date" | reverse %}

{% for post in life_posts %}
  <article class="post-preview">
    <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
    <p class="post-meta">📅 {{ post.date | date: "%b %d, %Y" }} {% if post.tags %} | 🏷️ {{ post.tags | join: ", " }}{% endif %}</p>
  </article>
{% endfor %}
