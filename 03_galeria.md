---
layout: gal
title: Galéria
permalink: /galeria/
---

{% for gallery in site.data.galleries %}
{:.galeria}
- [{{ gallery.description }}]({{ gallery.id }})
{% endfor %}