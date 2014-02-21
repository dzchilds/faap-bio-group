---
layout: with-jumbotron
title: Fundamental and Applied Population Biology Group
post-limit: 5
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

<div class="well text-center">
      We are a part of the <a href="http://www.sheffield.ac.uk/aps">
      Department of Animal and Plant Sciences</a> at the
      <a href="http://www.sheffield.ac.uk">University of
      Sheffield</a>
</div>

<div class="row">
<div class="col-sm-8 col-md-8">
  <h3 class>News and Opportunities</h3>
  <hr>
  <ul class="list-unstyled">
    {% for post in site.posts limit:page.post-limit %}
      <li>
        <h4><a data-toggle="modal" data-target="{{ forloop.index | prepend: "#modal_id" }}">{{ post.title }}</a> <small>{{ post.date | date_to_string }}</small></h4>
        <p>{{ post.excerpt }}</p>
      </li>
    {% endfor %}
	<hr>
	{% if site.posts.size > page.post-limit %}
	  <p class="text-center"><a href="{{ site.url}}news/index.html">Old News</a></p>
	{% endif %}
  </ul>
  <br>
</div>
<div class="col-sm-4 col-md-4">
  <div class="well">
    <h3> Contact us </h3>
	<p class="text-justify">The group leader is Dylan Childs. You should contact him if you
	  would like discuss opportunities such as PhDs or fellowship support.
    <br><br>
    <p class="text-left"><i class="fa fa-twitter-square fa-lg fa-fw"></i>&nbsp;dylan_childs</p>
    <p class="text-left"><i class="fa fa-google-plus-square fa-lg fa-fw"></i>&nbsp;d.childs@sheffield.ac.uk</p>
    <p class="text-left"><i class="fa fa-phone fa-lg
	fa-fw"></i>&nbsp;(+44)&nbsp;(0)114&nbsp;222&nbsp;4313</p>
	<br>
	<p class="text-left">
       <small>Department of Animal and Plant Sciences<br>University of Sheffield<br>Sheffield, S10 2TN, UK</small>
	</p>
  </div>
</div>
</div>

<div class="row">
  <p>{{ paginator.posts }}</p>
</div>
