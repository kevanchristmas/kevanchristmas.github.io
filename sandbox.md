---
layout: page
title: Sandbox
permalink: /sandbox/
---

# 🏖️ Sandbox

Anything that doesn't make it into the MVP...
- Quick (read:halfbaked) ideas/thoughts
- Rescue animals from previous blogs
- Other etc.

<ul>
{% assign posts_sorted = site.posts | sort: 'date' | reverse %}
{% for post in posts_sorted %}
  {% assign is_sandbox = false %}
  {% for t in post.tags %}
    {% if t | downcase | strip == 'sandbox' %}
      {% assign is_sandbox = true %}
    {% endif %}
  {% endfor %}
  {% if is_sandbox %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <small>— {{ post.date | date: "%d %b %Y" }}</small>
    </li>
  {% endif %}
{% endfor %}
</ul>
