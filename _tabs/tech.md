---
layout: page
icon: fas fa-laptop-code
order: 1
title: Tech
---

{% assign tech_posts = site.posts | where_exp: "post", "post.categories contains 'Tech'" | sort: "date" | reverse %}

{% for post in tech_posts %}
  <article class="post-preview">
    <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
    <p class="post-meta">📅 {{ post.date | date: "%b %d, %Y" }} {% if post.tags %} | 🏷️ {{ post.tags | join: ", " }}{% endif %}</p>
  </article>
{% endfor %}
