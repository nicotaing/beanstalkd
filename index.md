---
layout: app
title: About
---

##Stay tuned
{% for post in site.posts limit:2 %}

### {{ post.date | date_to_long_string }}

[{{ post.title }}](/beanstalkd{{ post.url }})

{% endfor %}

[More news...](news.html){: .more-news}



