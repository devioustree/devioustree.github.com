---
layout: index
title: devioustree
---
{% include JB/setup %}

<ul class="posts">
    {% for post in site.posts %}
    {% if post.layout == "song" %}
    <li class="song">
        {{ post.content }}
        <p class="meta">{{ post.date | date_to_long_string }}</p>
    </li>
    {% else %}
    <li class="post">
        <h2><a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></h2>
        {{ post.content }}
        <p class="meta">{{ post.date | date_to_long_string }}</p>
    </li>
    {% endif %}
    {% endfor %}
</ul>


