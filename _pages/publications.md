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

  <div id="accordion">
    <div class="card">
      <div class="card-header" id="abs">
        <h5 class="mb-0">
          <button class="btn btn-link" data-toggle="collapse" data-target="#collapseOne" aria-expanded="true" aria-controls="collapseOne">
            Click here to view abstract...
          </button>
        </h5>
      </div>  
      <div id="abs" class="collapse show" aria-labelledby="headingOne" data-parent="#accordion">
        <div class="card-body">
          Anim pariatur cliche reprehenderit, enim eiusmod high life accusamus terry richardson ad squid. 3 wolf moon officia aute, non cupidatat skateboard dolor brunch. Food truck quinoa nesciunt laborum eiusmod. Brunch 3 wolf moon tempor, sunt aliqua put a bird on it squid single-origin coffee nulla assumenda shoreditch et. Nihil anim keffiyeh helvetica, craft beer labore wes anderson cred nesciunt sapiente ea proident. Ad vegan excepteur butcher vice lomo. Leggings occaecat craft beer farm-to-table, raw denim aesthetic synth nesciunt you probably haven't heard of them accusamus labore sustainable VHS.
        </div>
      </div>
   </div>
  </div>

{% endfor %}

<h3 id="patents"> Patents </h3>

{% for i in site.data.patents %}

  <em>{{ i.authors }} </em><br />
  {{ i.title }} <br />
  <span class="sky">{{ i.patent-id }}</span>

{% endfor %}

<h3 id="list-of-all-publications"> List of all Publications </h3>

{% for publi in site.data.publist%}

  <em>{{ publi.authors }} </em><br />
  <span class="navy">{{ publi.title }}</span><br />
  In: <span class="sky">{{publi.link.display}}</span>

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