---
layout: single
permalink: /blogs
title: Blogs
---

## List of published blogs

{% assign blogs = site.categories["blogs"] %}

<ul reversed>
{%- for blog in blogs %}
    <li>  
        <a href="{{site.baseurl}}{{ blog.url }}">{{ blog.title }}</a> 
    </li>
{%- endfor %}
</ul>