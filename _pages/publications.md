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
<h3 id="patents"> Patents </h3>

{% for i in site.data.patents %}

  <em>{{ i.authors }} </em><br />
  {{ i.title }} <br />
  <span class="sky">{{ i.patent-id }}</span>

{% endfor %}

<h3 id="list-of-all-publications"> List of all Publications </h3>

{% assign limited_publist = site.data.publist | slice: 0, 5 %}
  {% for publi in limited_publist %}
    <div class="publication-item">
      {{ publi.title }} <br />
      <em>{{ publi.authors }} </em><br />
      <a href="{{ publi.link.url }}">{{ publi.link.display }}</a>
    </div>
{% endfor %}

<button id="see-more-btn" onclick="loadMorePublications()">See More</button>


{% for publi in site.data.publist | slice: 0, 5 %}

  {{ publi.title }} <br />
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>

{% endfor %}

<div>
  <a class="btn btn-primary" data-toggle="collapse" href="#collapseExample" role="button" aria-expanded="false" aria-controls="collapseExample">
    Link with href
  </a>
  <button class="btn btn-primary" type="button" data-toggle="collapse" data-target="#collapseExample" aria-expanded="false" aria-controls="collapseExample">
    Button with data-target
  </button>
</div>
<div class="collapse" id="collapseExample">
  <div class="card card-body">
    Anim pariatur cliche reprehenderit, enim eiusmod high life accusamus terry richardson ad squid. Nihil anim keffiyeh helvetica, craft beer labore wes anderson cred nesciunt sapiente ea proident.
  </div>
</div>