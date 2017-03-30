---
layout: default
title: Archives
---

# Archives
{% for post in site.posts %}
*{{ post.date | date_to_string }} <a href="{{ post.url }}">{{ post.title }}</a>
{% endfor %}
