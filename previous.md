---
layout: default
title: Previous Semesters
---

{% assign posts = site.posts %}
{% if posts and posts.size > 1 %}
  <div class="posts">
    {% for post in posts %}
      {% if forloop.index0 > 0 %}
        <div class="post">
          <h2 class="post-title">
            <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
          </h2>
          <span class="post-date">{{ post.date | date_to_string }}</span>
          {{ post.excerpt }}
        </div>
      {% endif %}
    {% endfor %}
  </div>
{% else %}
  <p>No previous semesters found.</p>
{% endif %}