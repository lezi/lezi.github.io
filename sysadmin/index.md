---
layout: page
class: category
description: Linux, command line, system administration.
---
# Sysadmin


<ul id="posts">
      {% for post in site.categories.dev %}
      {% unless post.draft %}
        <li class="post">
      
        {% if post.title %}
            <h2 class="posttitle"><a href="{{ post.url }}" class="articletitle">{{ post.date | date:"%d/%m/%Y" }} - {{ post.title }}</a></h2>
            
        {% endif %}
        </li>
      {% endunless %}
      {% endfor %}
    </ul>