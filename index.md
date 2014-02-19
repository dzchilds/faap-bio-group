---
layout: with-jumbotron
title: Fundamental and Applied Population Biology Group
---

{% for post in site.posts %}
<div class="modal fade" id="{{ forloop.index | prepend: "modal_id" }}" tabindex="-1" role="dialog" aria-labelledby="myModalLabel" aria-hidden="true">
  <div class="modal-dialog">
    <div class="modal-content">
      <div class="modal-header">
        <button type="button" class="close" data-dismiss="modal" aria-hidden="true">&times;</button>
        <h4 class="modal-title" id="myModalLabel">{{ post.title }}</h4>
      </div>
      <div class="modal-body">
        {{ post.content }}
      </div>
      <div class="modal-footer">
        <button type="button" class="btn btn-default" data-dismiss="modal">Close</button>
      </div>
    </div>
  </div>
</div>
{% endfor %}

<div class="row">
  <div class="col-sm-4 col-md-4 text-center">
	<div class="well well-small"><h4><i class="fa fa-male fa-2x fa-fw"></i>People<h4></div>
  </div>
  <div class="col-sm-4 col-md-4 text-center">
	<div class="well"><h4><i class="fa fa-bug fa-2x fa-fw"></i>Research<h4></div>
  </div>
  <div class="col-sm-4 col-md-4 text-center">
	<div class="well"><h4><i class="fa fa-book fa-2x fa-fw"></i>Publications<h4></div>
  </div>
</div>

<div class="row"> 
    <p class="text-center"><br></p>
</div>

<div class="row">
<div class="col-sm-8 col-md-8">
  <h3 class>News and Opportunities</h3>
  <hr>
  <ul class="list-unstyled">
    {% for post in site.posts %}
      <li>
        <h4><a data-toggle="modal" data-target="{{ forloop.index | prepend: "#modal_id" }}">{{ post.title }}</a> <small>{{ post.date | date_to_string }}</small></h4>
        <p>{{ post.excerpt }}</p>
      </li>
      {% endfor %}
  </ul>
</div>
<div class="col-sm-4 col-md-4">
  <div class="well">
    <h4> Contact us </h4>
    <span data-lorem="8s"></span>
    <br>
    <h5 class="text-left"><i class="fa fa-twitter fa-lg fa-fw"></i>&nbsp;dylan_childs</h5>
    <h5 class="text-left"><i class="fa fa-envelope-o fa-lg fa-fw"></i>&nbsp;d.childs@sheffield.ac.uk</h5>
    <h5 class="text-left"><i class="fa fa-phone fa-lg fa-fw"></i>&nbsp;(+44)&nbsp;(0)114&nbsp;222&nbsp;4313</h5>
  </div>
</div>
</div>

