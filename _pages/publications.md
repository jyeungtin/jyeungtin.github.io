---
layout: page
permalink: /publications/
title: publications
description: publications by categories in reversed chronological order. 
years: ['Forthcoming', 2023, 2022]
nav: true
nav_order: 2
---
## In prepration
I am currently working with colleagues from within the Netherlands and beyond on projects about journalism, fact-checking, elections in Indonesia and veracity judgement.

<!-- _pages/publications.md -->
<div class="publications">

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f {{ site.scholar.bibliography }} -q @*[year={{y}}]* %}
{% endfor %}

</div>
