---
layout: default
title: Algebra | Olymplex
date: 2021-08-16 12:00:00 -0400
permalink: /mathematical-olympiads/algebra/
---
<h1>Algebra Content</h1>
<p><a href="https://example.com">Olymplex</a> > <a href="https://example.com">Mathematical Olympiads</a> > <a href="https://example.com">Algebra</a></p>
{% for topic in site.data.algebra_topic_list %}
{% capture topic_name %}{{ topic | first }}{% endcapture %}
{% assign page_topic = site.data.algebra_topic_list[topic_name] %}
  <ul class="actions fit big">
  <li><a href="{{ site.baseurl }}{{ page.permalink}}olym-{{ forloop.index | plus:0 }}a" class="button fit big">Olym {{ forloop.index | plus:0 }}A. {{ page_topic.name }}</a></li>
  </ul>
{% endfor %}
