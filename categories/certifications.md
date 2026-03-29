---
layout: page
title: Certifications
subtitle: Study notes, tips, and reviews for security certifications
---

{% assign posts = site.posts | where_exp: "post", "post.categories contains 'certifications'" %}
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
