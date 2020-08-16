---
title: Blog Archive
layout: home
---

{% assign sorted_posts = site.posts | sort: "date" | reverse %}
{% for post in sorted_posts %}
### [{{ post.title }}]({{ post.url }}) - {{ post.date | date: "%B %-d, %Y" }}
{{ post.description }}
---
{% endfor %}
