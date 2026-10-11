---
layout: default
title: "Notes"
permalink: /notes/
---

<div class="row g-5 mb-5">
  <div class="col-md-12">
    <h3 class="fw-bold border-bottom pb-3 mb-4">Collections</h3>
    {% for c in site.data.collections %}
      <h4 class="mt-4"><a href="{{ site.github.url }}/notes/{{ c.slug }}/">{{ c.title }}</a></h4>
      <p class="text-muted">{{ c.description }}</p>
    {% endfor %}

    <h3 class="fw-bold border-bottom pb-3 mb-4 mt-5">All Notes</h3>
    {% if site.posts.size == 0 %}
      <p>No notes yet.</p>
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
