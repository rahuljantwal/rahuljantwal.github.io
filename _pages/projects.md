---
layout: archive
permalink: /machine-learning/
title: Projects by tags
author_profile: true
header:
    images: "/images/header.jpg"
---

{% include base_path %} 
{% include group-by-array collection=site.posts field="tags" %}

{% for tag in group_names %} 
    {% assign posts = group_items[forloop.index0] %}
{{ tag }}
    {% for post in posts %} 
        {% include archive-single.html %} 
    {% endfor %}
{% endfor %}