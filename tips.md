---
layout: default
title: Tips
permalink: /tips/
---
<div class="page-header theme-bg-dark py-5 text-center position-relative">
    <div class="theme-bg-shapes-right"></div>
    <div class="theme-bg-shapes-left"></div>
    <div class="container">
        <h1 class="page-heading single-col-max mx-auto">{{ page.title }}</h1>
        {% if page.description %}<div class="page-intro single-col-max mx-auto">{{ page.description }}</div>{% endif %}
    </div>
</div>

<div class="page-content">
    <div class="container">
        <div class="docs-overview py-5">
            <div class="row justify-content-center">
                {% assign filtered_posts = site.posts | where: 'categories', 'tips' | sort: 'date' | reverse %}
                {% for post in filtered_posts %}
                <div class="col-12 col-lg-4 py-3">
                    <div class="card shadow-sm">
                        <div class="card-body">
                            <h5 class="card-title mb-3">
                                <span class="theme-icon-holder card-icon-holder mr-2">
                                    {% if post.icon %}
                                    {{ post.icon }}
                                    {% else %}
                                    <i class="far fa-newspaper"></i>
                                    {% endif %}
                                </span><!--//card-icon-holder-->
                                <span class="card-title-text">{{ post.title }}</span>
                            </h5>
                            <div class="card-text">
                                {{ post.excerpt | strip_html | truncatewords: 10 }}
                            </div>
                            <a class="card-link-mask" href="{{ post.url }}"></a>
                        </div><!--//card-body-->
                    </div><!--//card-->
                </div><!--//col-->
                {% endfor %}
            </div>
        </div>
    </div>
</div>
