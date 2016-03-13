---
layout: data
title: Moji spolužiaci
desc: Kontaktujte kohokoľvek, kedykoľvek, odkiaľkolvek
permalink: /cvicenia/
---

<ul>
{% for cv_hash in site.data.cvicenia %}
	<div class="newcolumn">
	{% assign cv = cv_hash[1] %}
		<br>
		<li class="sk">{{ cv.name }} (Počet študentov: {{ cv.members | size }})</li>
		<ul>
			{% for member in cv.members %}
			<li class="lst">
			<a href="mailto:{{ member.email }}">{{ member.name }}</a>
			</li>
			{% endfor %}
		</ul>
{% endfor %}
	</div>
</ul>