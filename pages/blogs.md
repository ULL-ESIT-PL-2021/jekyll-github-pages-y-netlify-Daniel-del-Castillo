---
layout: single
permalink: /blogs
title: Blogs
toc: false
---

## Lista de Blogs Publicados

{% assign blogs = site.categories["blogs"] %}

<ol reversed>
{%- for blog in blogs %}
    <li>  
        <a href="{{site.baseurl}}{{ blog.url }}">{{ blog.title }}</a> 
    </li>
{%- endfor %}
</ol>