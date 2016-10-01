---
layout: page
title: Assignments
header: Assignments
group: navigation
---
{% include JB/setup %}


{% for category in site.categories %} 
  {% if category[0] == 'assignments' %}
  <ul>
    {% assign pages_list = category[1] %}  
    {% assign pages_limit = 5 %}  
    {% include JB/pages_list %}
  </ul>
  {% endif %}
{% endfor %}

