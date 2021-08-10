---
layout: default
title: Combinatorics | Olymplex
date: 2021-08-16 12:00:00 -0400
permalink: /mathematical-olympiads/combinatorics/
---
<h1>Combinatorics Content</h1>
<p><a href="https://ramaniumx.github.io/phantom-jekyll-theme/">Olymplex</a> > <a href="https://ramaniumx.github.io/phantom-jekyll-theme/mathematical-olympiads/">Mathematical Olympiads</a> > <a href="https://ramaniumx.github.io/phantom-jekyll-theme/mathematical-olympiads/combinatorics/">Combinatorics</a><p>
{% for topic in site.data.combinatorics_topic_list %}
{% capture topic_name %}{{ topic | first }}{% endcapture %}
{% assign page_topic = site.data.combinatorics_topic_list[topic_name] %}
  <ul class="actions fit big">
  <li><a href="{{ site.baseurl }}{{ page.permalink}}olym-{{ forloop.index | plus:0 }}c" class="button fit big">Olym {{ forloop.index | plus:0 }}C. {{ page_topic.name }}</a></li>
  </ul>
{% endfor %}
