---
layout: chapter
title: Learn
permalink: /learn/
---
{% assign filtered_posts = site.posts | where: 'categories', 'lesson' | sort: 'date' %}
<div class="docs-wrapper">
    <div id="docs-sidebar" class="docs-sidebar">
        <div class="top-search-box d-lg-none p-3">
            <form class="search-form">
                <input type="text" placeholder="Search the docs..." name="search" class="form-control search-input">
                <button type="submit" class="btn search-btn" value="Search"><i class="fas fa-search"></i></button>
            </form>
        </div>
        <nav id="docs-nav" class="docs-nav navbar">
            <ul class="section-items list-unstyled nav flex-column pb-3">
                {% for post in filtered_posts %}
                <li class="nav-item section-title mt-3">
                    <a class="nav-link scrollto active" href="#{{ post.article_id }}">
                        <span class="theme-icon-holder mr-2">{% if post.icon %}{{ post.icon }}{% else %}<i class="fas fa-map-signs"></i>{% endif %}</span>{{ post.title }}
                    </a>
                </li>
                {% for section in post.sections %}
                <li class="nav-item"><a class="nav-link scrollto" href="#{{ section[0] }}">{{ section[1] }}</a></li>
                {% endfor %}
                {% endfor %}
            </ul>
        </nav><!--//docs-nav-->
    </div><!--//docs-sidebar-->
    <div class="docs-content">
        <div class="container">
            {% for post in filtered_posts %}
            {{ post.content }}
            {% endfor %}
            {% include footer.html %}
        </div> 
    </div>
</div><!--//docs-wrapper-->