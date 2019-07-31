---
layout: page
title: 一无所知
showtag:
- ICPC模板
---
## 近期

{% for post in site.posts limit:8 %}

- [{{ post.title }}]({{ post.url }}), *{{ post.date | date:"%Y-%m-%d %H:%M:%S" }}*

{% if post.description %}

  > {{ post.description }}

{% endif %}

{% endfor %}

- [更多…](/archive)

{% for tag in page.showtag %}

## {{ tag }}

{% for post in site.tags[tag] %}

- [{{ post.title }}]({{ post.url }})

{% if post.description %}

  > {{ post.description }}

{% endif %}

{% endfor %}

{% endfor %}
