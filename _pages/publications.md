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
  
  <span class="navy">{{ publi.title }}</span><br />
  <em>{{ publi.authors }} </em><br />
  In: {{ publi.publisher }}, <i class="sky">(Submitted: {{publi.date}})</i>
  

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
  In: {{publi.publisher}}
  <div>
  <a class="custom-navy-btn" data-toggle="collapse" href="#abstract" role="button" aria-expanded="false" aria-controls="abstract">
    Abstract
  </a>

  <a class="custom-navy-btn" data-toggle="collapse" href="#bibtex" role="button" aria-expanded="false" aria-controls="bibtex">
    BibTeX
  </a>

  <a class="custom-navy-btn" data-toggle="collapse" href="#url" role="button" aria-expanded="false" aria-controls="url">
    URL
  </a>
</div>


<div class="collapse" id="abstract">
  <div class="card card-body">
    {{publi.abs}}
  </div>
</div>

<div class="collapse" id="bibtex">
  <div class="card card-body">
    {{publi.bibtex}}
  </div>
</div>

<div class="collapse" id="url">
  <div class="card card-body">
    <a href="{{publi.url}}" target="_blank" class="custom-link">{{publi.url}}</a>
  </div>
</div>

{% endfor %}