---
layout: page
title: Current Schedule
---

{% assign latest = site.posts | first %}
{% if latest %}
  <article class="post">
    <h2 class="post-title">
      <a href="{{ latest.url | relative_url }}">{{ latest.title }}</a>
    </h2>
    <span class="post-date">{{ latest.date | date_to_string }}</span>

    {{ latest.content }}
  </article>
{% else %}
  <p>No schedule posts found.</p>
{% endif %}

