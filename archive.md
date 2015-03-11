---
layout: page
title: Archive
---

{% for post in site.posts %}
<ul class="tags">
  {% for tag in post.tags %}
    <li><a href="{{ site.baseurl }}tags.html#{{tag}}" class="tag">{{ tag }}</a></li>
  {% endfor %}
</ul>

<span>{{ post.date | date: "%m/%d/%Y" }}</span> &raquo; [ {{ post.title }} ]({{ post.url }})
{% endfor %}
