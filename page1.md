---
layout: page
title: Activities
permalink: /Activities/
---

<h1 class="page-title">Class {{ page.title | escape }}</h1>

<div class="section">
<div style="background: #ddd">
    <div class="container last-post">
        <ul class="collection">
	        {% for post in site.posts %}
		        <li class="collection-item avatar">
		          {% assign date_format = site.minima.date_format | default: "%m/%d" %}
		          {% if post.ptype == "discussion" %}
		          <div class="date-post indigo darken-4">{{ post.date | date: date_format }}</div>
		          {% elsif post.ptype == "lecture" %}
		          <div class="date-post pink darken-3">{{ post.date | date: date_format }}</div>
		          {% elsif post.ptype == "theory" %}
		          <div class="date-post deep-orange">{{ post.date | date: date_format }}</div>
		          {% elsif post.ptype == "practical" %}
		          <div class="date-post green darken-3">{{ post.date | date: date_format }}</div>
		          {% elsif post.ptype == "exam" %}
		          <div class="date-post grey darken-3">{{ post.date | date: date_format }}</div>
		          {% endif %}
		          <span class="title"><a class="post-link" href="{{ post.url | relative_url }}">{{ post.title | escape }}</a></span>
		          <p>
		             {{ post.reading | truncatewords: 8 }}
		          </p>
		          <a href="{{ post.url | relative_url }}" class="secondary-content"><i class="material-icons">navigate_next</i></a>
	        {% endfor %}
 