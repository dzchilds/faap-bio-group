---
layout: default
title: Outputs from the group
---

<div class="col-sm-12 col-md-12">
<div class=row>
  <div class="col-sm-2 col-md-2">
    <h4 class="text-center"> Papers</h4>
  </div>
  <div class="col-sm-10 col-md-10">
    <h4> </h4>
    <ul>
      {% for paper in site.data.outputs.papers %}
      <li >
         {% for author in paper.authors %}{{ author.name }}{% endfor %}
         ({{ paper.year }}) <em>{{ paper.title }}</em> <strong>{{ paper.journal }}</strong>
      </li>
       {% endfor %}
    </ul>
  </div>
</div>

<div class=row>
  <div class="col-sm-2 col-md-2">
    <h4 class="text-center"> Books</h4>
  </div>
  <div class="col-sm-10 col-md-10">
    <h4> </h4>
    <ul class="list-group">
      <li class="list-group-item">
      </li>
    </ul>
  </div>
</div>
</div>
