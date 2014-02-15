---
layout: new-default
title: Outputs from the group
---

<div class=row>
  <div class="col-sm-2 col-md-3">
    <h3> Papers</h3>
  </div>

  <div class="col-sm-9 col-md-9">
    <h3> </h3>
    <ul class="list-group">
      {% for paper in site.data.outputs.papers %}
      <li class="list-group-item">
         {% for author in paper.authors %}{{ author.name }}{% endfor %}
         ({{ paper.year }}) <em>{{ paper.title }}</em> <strong>{{ paper.journal }}</strong>
      </li>
       {% endfor %}
    </ul>
  </div>
</div>

<div class=row>
  <div class="col-sm-2 col-md-3">
    <h3> Books</h3>
  </div>
  <div class="col-sm-9 col-md-9">
    <h3> </h3>
    <ul class="list-group">
      <li class="list-group-item">
	    
      </li>
    </ul>
  </div>
</div>
