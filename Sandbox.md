---
layout: page
title: Sandbox
permalink: /sandbox/
---

# 🏖️ Sandbox  

A bunch of things that don't make it into the MVP...

- Quick (read:half-baked) ideas and thoughts
- Weird interests/projects
- Random rescue animals from previous blogs
- etc.

---

{% assign sandbox_posts = site.posts | where_exp:"p","p.categories contains 'sandbox'" %}
{% if sandbox_posts.size > 0 %}
## Latest from the Sandbox
<ul>
  {% for post in sandbox_posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <small>— {{ post.date | date: "%d %b %Y" }}</small>
    </li>
  {% endfor %}
</ul>
{% else %}
<em>Tag any post with <code>categories: [sandbox]</code> to have it show up here.</em>
{% endif %}

