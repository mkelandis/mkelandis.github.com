---
layout: page
title:    
tagline: code. musings.
---
{% include JB/setup %}

Topics:

* Software Engineering
* Music
* Guitars and Amplifiers  

## Latest Posts

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

