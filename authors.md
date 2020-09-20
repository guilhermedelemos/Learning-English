---
layout: default
title: Authors
description: Full list of our authors
permalink: /authors/
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
                {% for author in site.authors %}
                <div class="col-12 col-lg-4 py-3">
                    <div class="card shadow-sm">
                        <div class="card-body">
                            <h5 class="card-title mb-3">
                                <span class="theme-icon-holder card-icon-holder mr-2">
                                    {% if author.icon %}
                                    {{ author.icon }}
                                    {% else %}
                                    <i class="fas fa-user"></i>
                                    {% endif %}
                                </span><!--//card-icon-holder-->
                                <span class="card-title-text">{{ author.name }}</span>
                            </h5>
                            <div class="card-text">
                                <p>{{ author.position }}</p>
                                <p>{{ author.content | markdownify }}</p>
                            </div>
                            <a class="card-link-mask" href="{{ author.url }}"></a>
                        </div><!--//card-body-->
                    </div><!--//card-->
                </div><!--//col-->
                {% endfor %}
            </div>
        </div>
    </div>
</div>