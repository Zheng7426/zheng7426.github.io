---
layout: default
title: Category
permalink: /categories/
---
<h1>Categories</h1>
This is where you could find articles for various categories:
<ul>
    {% for category in site.categories %}
    <li><a href="{{ category.url }}">
    {{ category.name }} 
    {% if category.stream %}- {{ category.stream }}{% endif %}</a></li>
{% endfor %}
</ul>
