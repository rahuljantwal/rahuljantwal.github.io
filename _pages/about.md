---
layout: splash
title: About
permalink: /about/
author_profile: true
header:
   image: "/images/header.jpg"
---

I'm a data scien

{% include base_path %} 
{% include group-by-array collection=site.posts field="tags" %}

{% for tag in group_names %} 
    {% assign posts = group_items[forloop.index0] %}
{{ tag }}
    {% for post in posts %} 
        {% include archive-single.html %} 
    {% endfor %}
{% endfor %}