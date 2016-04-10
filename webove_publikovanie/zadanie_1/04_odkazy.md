---
layout: tags
title: Odkazy
permalink: /odkazy/
---

{% capture tags %}
  {% for tag in site.tags %}
    {{ tag[0] }}
  {% endfor %}
{% endcapture %}
{% assign sortedtags = tags | split:' ' | sort %}

{% for tag in sortedtags %}
  <h3 id="{{ tag | escape }}">#{{ tag }}</h3>
  <ul class="pos">
	  {% for post in site.tags[tag] %}
			<li class="lst"><a href="{{site.baseurl}}{{ post.url }}">{{ post.title }}</a></li>
	  {% endfor %}
  </ul>
{% endfor %}