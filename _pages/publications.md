---
title: "MBZUAI NLP Research Group - Publications"
layout: gridlay
excerpt: "MBZUAI NLP Research Group -- Publications."
sitemap: false
permalink: /publications/
---

<h2>Publications</h2>



<h2> List of Publications </h2>
<h3> Under Review </h3>

{% for publi in site.data.publist %}

  {{ publi.title }} <br />
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>

{% endfor %}
