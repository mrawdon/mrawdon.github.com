---
layout: page
title: Home
header: Posts By Category
---
{% include JB/setup %}


{% for category in site.categories %} 
  {% if category[0] == 'home' %}
    {% for post in category[1] %} 
      {% capture includeGuts %}
      {{post.content}}
      {% endcapture %}
      {{ includeGuts | replace: '    ', ''}}
    {% endfor %}

  {% endif%}
{% endfor %}

{% for category in site.categories %} 
  {% if category[0] != 'home' %}
  <h2 id="{{ category[0] }}-ref"><a href="{{ BASE_PATH }}/{{category[0]}}-posts">{{ category[0] | join: "/" }}</a></h2>
  
  <ul>
    {% assign pages_list = category[1] %}  
    {% assign pages_limit = 5 %}  
    {% include JB/pages_list %}
  </ul>
  {% endif%}
{% endfor %}

