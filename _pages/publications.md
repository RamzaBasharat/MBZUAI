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

{% for i in site.data.publist %}

  <em>{{ i.authors }} </em><br />
  <span class="navy">{{ i.title }}</span><br />
  In: {{i.publisher}}
<div class="col-sm-12 clearfix">
  <a class="small-sky-btn" data-toggle="collapse" href="#{{i.abs}}" role="button" aria-expanded="false" aria-controls="{{i.abs}}">
    Abstract
  </a>
  <a class="small-sky-btn" href="{{ i.url }}" target="_blank">
    URL
  </a>
  <a class="small-sky-btn" data-toggle="collapse" href="##{{i.bibtex}}" role="button" aria-expanded="false" aria-controls="{{i.bibtex}}">
    BibTeX
  </a>
</div>


<div class="collapse" id="{{i.abs}}">
  <div class="card card-body">
    {{i.abs}}
  </div>
</div>

<div class="collapse" id="{{i.bibtex}}">
  <div class="card card-body">
   {{i.bibtex}}
  </div>
</div>

{% endfor %}