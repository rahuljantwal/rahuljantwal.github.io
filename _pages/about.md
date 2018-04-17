---
layout: archive
title: About
permalink: /about/
author_profile: true
header:
   image: "/images/header.jpg"
   cta_label: "More Info" 
---

I am a graduate student at The University of Chicago.

{% include base_path %} 
{% include group-by-array collection=site.posts field="tags" %}

{% for tag in group_names %} 
    {% assign posts = group_items[forloop.index0] %}
{{ tag }}
    {% for post in posts %} 
        {% include archive-single.html %} 
    {% endfor %}
{% endfor %}