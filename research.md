---
layout: default
title: people in the group
---

<div class=row><div class="col-sm-12 col-md-12">
  <p>We apply model-based approaches to understand population
    dynamics and natural selection in laboratory and free-living
    populations. We are particularly keen to understand how
    demographic and ecological processes interact to natural shape
    selection. Some general questions that interest us include: (1)
    Can we use evolutionary game theory (aka adaptive dynamics) to
    better understand selection on the life histories of free-living
    animals and plants, or are classical approaches sufficient? (2)
    How do temporal and spatial environmental variation shape the
    dynamics of populations in a changing environment? (3) Do we need
    to account for fluctuating selection to fully understand optimal
    life-histories in natural populations? For example, when does such
    variation select evolutionary bet-hedging strategies?</p>
  <hr>
</div></div> 

<div class=row>
  <div class="col-sm-2 col-md-2">
    <h4 class="text-left">Projects</h4>
  </div>
  <div class="col-sm-10 col-md-10">
    <h4> </h4>
    <div class="text-center"><ul class="list-inline">
      <li><small>PI: Primary Investigators</small></li>
      <li><small>CI: Co-Investigators</small></li>
      <li><small>PP: Project Partners</small></li>
      <li><small>PD: Post Doctoral Research Associates</small></li>
    </ul></div>
    <br>
    {% for project in site.data.projects.current-funded %}
	<div class="thumbnail right-caption">
	  {% if project.image != null %}
       <img src="{{ site.url }}assets/images/{{ project.image }}"
	      width="100" height="100" class="img-rounded">
      {% else %}
        <img data-src="holder.js/100x100" alt="..." class="img-rounded">
      {% endif %}
      <div class="caption">
        <h4>{{ project.stitle }} <small>({{ project.when }})</small></h4>
        <h5><small>Funded by {{ project.funding }}</small></h5>
        <p>{{ project.description }}</p>
        <h5><small>
          Who is involved? 
          {% for person in project.people %}{% if person.url != null %}<a href="{{person.url}}">{{person.name}}</a>{% else %}{{person.name}}{% endif %}{% endfor %}
        </small></h5>
      </div>
    </div>
    {% endfor %}
  </div>
</div>
</div>
