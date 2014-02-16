---
layout: new-default
title: people in the group
---

<div class="col-sm-3 col-md-3">
  <h4 class>Who are we?</h4>
  <hr>
  <h5>Group Leader</h5>
  <p>Dylan Childs</p>
  <hr>
  <h5>PhD Students</h5>
    {% for person in site.data.people.phd-current %}
	  <p>{{ person.name }}</p>
    {% endfor %}
</div>

<div class="col-sm-9 col-md-9">
  <h4>Current members</h4>
  <hr>
  <div class="thumbnail right-caption">
    <img data-src="holder.js/150x150" alt="..." class="img-circle">
    <div class="caption">
      <h4>Dylan Childs <small>Group Leader</small></h4>
      <p><span data-lorem="4s"></span><a href="#"> Find out more</a></p>
    </div>
  </div>
  {% for person in site.data.people.phd-current %}
  <div class="thumbnail right-caption">
    <img data-src="holder.js/150x150" alt="..." class="img-circle">
    <div class="caption">
      <h4>{{ person.name }} <small>PhD Student</small></h4>
      <p>{{ person.about }}<a href="#"> Find out more</a></p>
    </div>
  </div>
  {% endfor %}      	
  <h4>Positions Available</h4>
  <hr>
  <div class="thumbnail right-caption">
    <img data-src="holder.js/160x160" alt="..." class="img-circle">
    <div class="caption">
      <h4>Post Doc <small>Starting May 2014</small></h4>
      <p><span data-lorem="4s"></span><a href="#"> Find out more</a></p>
    </div>
  </div>
</div>
