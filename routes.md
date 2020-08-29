---
layout: default
title: Bicycle Routes
---

<div class="post">
	<h1 class="pageTitle">Bicycle Routes1</h1>
	<img src="{{ '/assets/img/touring.jpg' | prepend: site.baseurl }}" alt="">
<ul>
  {% for post in site.pages %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>

 {% for link in site.navigation %}{% assign current = nil %}{% if page.url contains link.url or forloop.first and page.url == '/' or page.url == 'index.html' %}{% assign current = 'current' %}{% endif %}
                 <li class="element {% if forloop.first %}first{% endif %} {{ current }} {% if forloop.last %}last{% endif %}">
                     <a href="{{ link.url | prepend: site.baseurl }}">{{ link.title }}</a>
                 </li> 
                 {% endfor %}


	
  	
</div>
