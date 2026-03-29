---
layout: page
title: Threat Analysis
subtitle: Breakdowns of real-world attacks and threat intelligence
---

{% assign posts = site.posts | where_exp: "post", "post.categories contains 'threat-analysis'" %}
{% if posts.size == 0 %}
  <p>No posts yet — check back soon!</p>
{% else %}
  {% for post in posts %}
    <article>
      <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
      <p>{{ post.date | date: "%B %-d, %Y" }}</p>
      <p>{{ post.excerpt }}</p>
    </article>
  {% endfor %}
{% endif %}
