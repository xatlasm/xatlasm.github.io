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
<div>
  <span style="float: left;"><a href="{{ post.url }}">{{ post.title }}</span>
  <span style="float: right;">{{ post.date | date_to_string }}</span>
</div>
<div style="clear: both;"></div>​
{% endfor %}
