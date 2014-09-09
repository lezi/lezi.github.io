---
layout: page
class: home
---

A blog about *programming* and other tech stuffs


    
# Writing

   <ul id="posts">
      {% for post in site.posts limit: 5 offset: 1 %}
      {% unless post.draft %}
        <li class="post">
        {% if page.title %}
            <h2 class="posttitle"><a href="{{ page.url }}" class="articletitle">{{ page.title }}</a></h2>
        {% endif %}
        {% if post.title %}
            <h2 class="posttitle"><a href="{{ post.url }}" class="articletitle">{{ post.title }}</a></h2>
        {% endif %}
        </li>
      {% endunless %}
      {% endfor %}
    </ul>
