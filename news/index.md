---
layout: default
title: PyWPS Blog
description: project blog and news
keywords: news, blog, development, announcements
---

# Archive [![RSS]({{site.baseurl}}/images/rss.png)]({{site.baseurl}}/feed.xml)

<ul>
  {% for post in site.posts %}
    <li>{{ post.date | date_to_long_string }} - <a href="{{site.baseurl}}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

