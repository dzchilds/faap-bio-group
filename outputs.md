---
layout: default
title: Outputs from the group
---

<div class="col-sm-3 col-md-3">
  <h3 class>Publications</h3>
  <span data-lorem="5s"></span>
</div>

<div class="col-sm-9 col-md-9">
  <h3>Papers</h3>
  <hr>
  <ul class="list-group">
      {% for paper in site.data.outputs.papers %}
      <li class="list-group-item">
        {% for author in paper.authors %}{{ author.name }}{% endfor %}
        ({{ paper.year }}) <em>{{ paper.title }}</em> <strong>{{ paper.journal }}</strong>
	  </li>
     {% endfor %}
  </ul>
  <h3>Books</h3>
  <hr>
</div>
