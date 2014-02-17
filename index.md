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

<div class="col-sm-9 col-md-9">
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

<div class="col-sm-3 col-md-3">
  <h3 class>Other Stuff</h3>
  <span data-lorem="5s"></span>
</div>
