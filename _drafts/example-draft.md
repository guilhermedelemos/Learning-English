---
layout: post
author: guilherme
title: "Draft Example"
# date: 2020-09-27 03:10:00 -0000
categories: lesson
tags: ["example", "draft"]
icon: <i class="fas fa-stream"></i>
article_id: draft-example-1-e419da3b-253e-4b7b-947f-2ec318e5b0c6
sections: [
    ["draft-example-1-section-1-d7acdf81-6b69-4a40-9d2f-2a9dd00b7790", "Draft Section 1"],
    ["draft-example-1-section-2-d7acdf81-6b69-4a40-9d2f-2a9dd00b7790", "Draft Section 2"],
    
]
introduction: "Draft Example intro."
---
<article class="docs-article" id="{{ page.article_id }}">
    <header class="docs-header">
        <h1 class="docs-heading">{{ page.title }}</h1>
        <section class="docs-intro">
            <p>{{ page.introduction }}</p>
        </section>
    </header>
    <section class="docs-section" id="{{ page.sections[0][0] }}">
        <h2 class="section-heading">{{ page.sections[0][1] }}</h2>
        This is a draft #1
    </section>
    <section class="docs-section" id="{{ page.sections[1][0] }}">
        <h2 class="section-heading">{{ page.sections[1][1] }}</h2>
        This is a draft #2
    </section>
</article>
