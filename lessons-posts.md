---
layout: page
title: Lessons
header: Lessons
group: navigation
---
{% include JB/setup %}


{% for category in site.categories %} 
  {% if category[0] == 'lessons' %}
  <ul>
    {% assign pages_list = category[1] %}  
    {% assign pages_limit = 5 %}  
    {% include JB/pages_list %}
  </ul>
  {% endif %}
{% endfor %}

