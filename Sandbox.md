---
layout: page
title: Sandbox
permalink: /sandbox/
---

# 🏖️ Sandbox  

Anything that doesn't make it into the MVP:
- Quick (read: half-baked) thoughts and ideas
- Rescue animals from previous blogs
- Any interesting projects or finds
- etc.

{% assign sandbox_posts = site.posts | where_exp:"p","p.tags contains 'sandbox'" %}
{% if sandbox_posts.size > 0 %}
## Latest from the Sandbox
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
      <small>— {{ post.date | date: "%d %b %Y" }}</small><br>
      <em>Tags: {{ post.tags | join: ", " }}</em>
    </li>
  {% endif %}
{% endfor %}
</ul>

{% unless site.posts %}
<em>Tag any post with <code>tags: [sandbox]</code> to show up here.</em>
{% endunless %}


