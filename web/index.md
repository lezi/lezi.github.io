---
layout: page
class: category
description: HTML, CSS, Javascript and other web related stuffs.
---
# HTML, CSS, Javascript and other web related stuffs


<ul id="posts">
      {% for post in site.categories.web %}
      {% unless post.draft %}
        <li class="post">
      
        {% if post.title %}
            <h2 class="posttitle"><a href="{{ post.url }}" class="articletitle">{{ post.date | date:"%d/%m/%Y" }} - {{ post.title }}</a></h2>
            
        {% endif %}
        </li>
      {% endunless %}
      {% endfor %}
    </ul>