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

<ul class="post-list">
  {% assign sandbox_posts = site.tags.sandbox | sort: 'date' | reverse %}
  {% if sandbox_posts and sandbox_posts != empty %}
    {% for post in sandbox_posts %}
      <li>
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        <small> — {{ post.date | date: "%d %b %Y" }}</small>
      </li>
    {% endfor %}
  {% else %}
    <li><em>No posts tagged <code>sandbox</code> yet.</em></li>
  {% endif %}
</ul>
