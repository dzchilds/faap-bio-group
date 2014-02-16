---
layout: new-default
title: people in the group
---

<div class=row>
  <div class="col-sm-2 col-md-2">
    <h4>Overview</h4>
  </div>
  <div class="col-sm-10 col-md-10">
    <h4> </h4>
	<p><span data-lorem="1p"></p>
  </div>
</div> 

<div class=row>
  <div class="col-sm-2 col-md-2">
    <h4>Projects</h4>
  </div>
  <div class="col-sm-10 col-md-10">
    <h4> </h4>
    {% for project in site.data.projects.funded %}
	<div class="thumbnail right-caption">
	  {% if project.image != null %}
       <img src="{{ site.url }}assets/images/{{ project.image }}"
	      width="100" height="100" class="img-rounded">
      {% else %}
        <img data-src="holder.js/100x100" alt="..." class="img-rounded">
      {% endif %}
      <div class="caption">
        <h4>{{ project.stitle }}</h4>
        <h5>{{ project.funding }}</h5>
        <h5><small>
		    Collaborators:
			  {% for collaborator in project.collaborators %}
			    {% if collaborator.url != null %}
				   <a href="{{ collaborator.url }}">{{ collaborator.name }}</a>
                {% else %}
                  {{ collaborator.name }}
			    {% endif %}
			  {% endfor %}
        </small></h5>
        <p>{{ project.description }}<a href="#"> Find out more</a></p>
      </div>
    </div>
	{% endfor %}
  </div>
</div> 
