---
layout: page
title: Archive
---

{% for post in site.posts %}
<span>{{ post.date | date: "%m/%d/%Y" }}</span> &raquo; [ {{ post.title }} ]({{ post.url }})
{% endfor %}
