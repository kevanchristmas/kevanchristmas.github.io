---
layout: page
title: Sandbox
permalink: /sandbox/
---

# 🏖️ Sandbox  
A playful space for fun extras, small experiments, and odd little ideas.

{% assign sandbox_posts = site.posts | where_exp:"p","p.tags contains 'sandbox'" %}
{% if sandbox_posts.size > 0 %}
## Latest from the Sandbox
<ul>
  {% for post in sandbox_posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <small>— {{ post.date | date: "%d %b %Y" }}</small>
      <br>
      <em>Tags: {{ post.tags | join: ", " }}</em>
    </li>
  {% endfor %}
</ul>
{% else %}
<em>Tag any post with <code>tags: [sandbox]</code> to show up here.</em>
{% endif %}


