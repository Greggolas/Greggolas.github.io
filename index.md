---
title: Home
layout: home
---

# Latest Posts
{% assign sorted_posts = site.posts | sort: "date" | reverse %}
{% for post in sorted_posts limit:3 %}
### [{{ post.title }}]({{ post.url }})
#### {{ post.date | date: "%B %-d, %Y" }}
{{ post.content }}
---
{% endfor %}

### [Older Posts](/blog)