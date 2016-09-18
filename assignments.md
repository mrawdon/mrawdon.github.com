---
layout: page
title: Assignments
header: Assignments
group: navigation
---
{% include JB/setup %}


{% for category in site.categories %} 
  {% if category[0] == 'assignments' %}
    <h2 id="{{ category[0] }}-ref"><a href="{{ BASE_PATH }}/{{category[0]}}">{{ category[0] | join: "/" }}</a></h2>
    
    <ul>
      {% assign pages_list = category[1] %}  
      {% assign pages_limit = 5 %}  
      {% include JB/pages_list %}
    </ul>
  {% endif %}
{% endfor %}

