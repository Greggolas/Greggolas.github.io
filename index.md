---
title: Home
layout: home
---

## About

Hi, I'm Gregg! I use this space to document work that I'm doing to better myself as a developer. 

If that interests you, feel free to poke around!


## The Latest
{% assign sorted_posts = site.posts | sort: "date" | reverse %}
{% for post in sorted_posts limit:3 %}
### [{{ post.title }} ({{ post.date | date: "%B %-d, %Y" }})]({{ post.url }})
{{post.content | strip_html | truncatewords:100  }}
[read more]({{ post.url }})

---
{% endfor %}