---
layout: default
---
{% for post in site.posts limit:5 %}
## [{{ post.title }}]({{ post.url }})
###### {{ post.date | date_to_string }}
{{ post.content }}
{% endfor %}

---
[Older Posts](archives)
