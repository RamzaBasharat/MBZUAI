---
title: "MBZUAI NLP Research Group - Publications"
layout: gridlay
excerpt: "MBZUAI NLP Research Group -- Publications."
sitemap: false
permalink: /publications/
---

<h2>Publications</h2>

Jump to [Under Review Articles](#under-review-articles), [Patents](#patents), [List of All Publications](#list-of-all-publications).

<h3 id="under-review-articles"> Under Review Articles </h3>

{% for publi in site.data.under_review %}
  
  <em>{{ publi.authors }} </em><br />
  <span class="navy">{{ publi.title }}</span><br />
  In: {{ publi.publisher }}, <i>(Submission Date: {{publi.date}})</i>
<div class="row" style="margin-bottom:3px;padding-bottom:0px">
  <div class="col-sm-12 clearfix">
  <a class="small-sky-btn" data-toggle="collapse" href="#abs-{{ forloop.index }}" role="button" aria-expanded="false" aria-controls="abs-{{ forloop.index }}">
    Abstract
  </a>
</div>
</div>
<div class="collapse" id="abs-{{ forloop.index }}">
    {{publi.abs}}
</div>

{% endfor %}

<h3 id="patents"> Patents </h3>

{% for i in site.data.patents %}

  <em>{{ i.authors }} </em><br />
  {{ i.title }} <br />
  <span class="sky">{{ i.patent-id }}</span>

{% endfor %}

<h3 id="list-of-all-publications"> List of all Publications </h3>

{% for publi in site.data.publist %}

  <em>{{ publi.authors }} </em><br />
  <span class="navy">{{ publi.title }}</span><br />
  In: {{publi.publisher}}, <i>(Publication Date: {{ publi.date }})</i>
<div class="row" style="margin-bottom=5px">
  <div class="col-sm-12 clearfix">
  <a class="small-sky-btn" data-toggle="collapse" href="#abstract-{{ forloop.index }}" role="button" aria-expanded="false" aria-controls="abstract-{{ forloop.index }}">
    Abstract
  </a>
  <a class="small-sky-btn" href="{{ publi.url }}" target="_blank">
    URL
  </a>
  <a class="small-sky-btn" data-toggle="collapse" href="#bibtex-{{ forloop.index }}" role="button" aria-expanded="false" aria-controls="bibtex-{{ forloop.index }}">
    BibTeX
  </a>
{% if publi.pdf %}
  <a class="small-sky-btn" href="{{ publi.pdf }}" target="_blank">PDF</a>
{% endif %}
</div>
</div>

<div class="collapse" id="abstract-{{ forloop.index }}">
    {{publi.abs}}
</div>

<div class="collapse" id="bibtex-{{ forloop.index }}">
   <pre>{{publi.bibtex}}</pre>
</div>
{% endfor %}