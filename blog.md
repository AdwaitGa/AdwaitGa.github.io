---
layout: default
title: "Blog"
---

<div class="row g-5 mb-5">
  <div class="col-md-12">
    <h3 class="fw-bold border-bottom pb-3 mb-5">Blog</h3>
    {% if site.posts.size == 0 %}
      <p>No posts yet.</p>
    {% endif %}
    {% for post in site.posts %}
      <p>
        <a href="{{ site.github.url }}{{ post.url }}" class="fw-bold">{{ post.title }}</a>
        <span class="text-muted"> - {{ post.date | date: "%B %-d, %Y" }}</span>
        {% if post.excerpt %}<br>{{ post.excerpt | strip_html | truncatewords: 40 }}{% endif %}
      </p>
    {% endfor %}
  </div>
</div>
