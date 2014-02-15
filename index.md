---
layout: with-jumbotron
title: Fundamental and Applied Population Biology Group
---

<div class="col-sm-9 col-md-9">
  <h3 class>News and Opportunities</h3>
  <hr>
  <ul>
    {% for post in site.posts %}
      <li>
        <h4>{{ post.date | date_to_string }} 
	      <a href="{{ site.url }}{{ post.url }}index.html">{{ post.title }}</a>
        </h4>
        <p>{{ post.excerpt }}</p>
      </li>
    {% endfor %}
  </ul>
</div>

<div class="col-sm-3 col-md-3">
  <h3 class>Other Stuff</h3>
  <span data-lorem="5s"></span>
</div>
