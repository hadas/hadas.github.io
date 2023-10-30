---
layout: page
permalink: /publications/
title: Publications
description: Hadas Raviv's publications
years: [2008, 2009, 2012, 2013, 2014, 2016, 2020]
nav: true
nav_order: 1
---
<!-- _pages/publications.md -->
<div class="publications">

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>

