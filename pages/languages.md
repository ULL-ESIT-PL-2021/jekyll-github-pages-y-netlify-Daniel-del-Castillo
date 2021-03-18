---
layout: single
permalink: /languages
title: Languages
---

## List of languages mentioned in blogs


<ul>
{%- for lang in site.languages %}
    <li>  
        <a href="{{site.baseurl}}{{ lang.url }}">{{ lang.name }}</a> 
    </li>
{%- endfor %}
</ul>