---
title: "News"
layout: textlay
excerpt: "MBZUAI NLP Research Group"
sitemap: false
permalink: /allnews.html
---

<h2>News</h2>

{% for article in site.data.news %}
<p>{{ article.date }} <br> {{ article.headline | markdownify}}</p>
<br>
{% endfor %}
