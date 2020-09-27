---
author: guilherme
title: "Irregular Verbs List"
date: 2020-09-19 21:43:00 -0300
categories: lesson
tags: ["irregular", "verbs", "lesson"]
icon: <i class="fas fa-stream"></i>
article_id: irregular-verbs-78be42cd-43a5-49b7-9f48-7fbf44c9f5fc
sections: [
    ["irregular-verbs-list-db9264dd-337f-4726-9001-4f662e9c95f2", "List"]
]
introduction: "An extensive list of irregular verbs."
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
        <table class="table table-striped">
            <colgroup>
                <col class="col-md-2">
                <col class="col-md-2">
                <col class="col-md-3">
                <col class="col-md-5">
                <col class="col-md-2">
            </colgroup>
            <thead>
                <tr lang="en">
                    <th class="text-nowrap ">Base Form</th>
                    <th class="text-nowrap">Past Tense</th>
                    <th class="text-nowrap">Past Participle</th>
                    <th class="text-nowrap">Portuguese Translation</th>
                    <th class="text-nowrap">Multiple Meaning</th>
                </tr>
            </thead>
            {% for verb in site.data.irregularVerbs %}
            <tr>
                <td><em>{{ verb.baseForm }}</em></td>
                <td><em>{{ verb.pastTense }}</em></td>
                <td><em>{{ verb.pastParticiple }}</em></td>
                <td>{{ verb.portuguese }}</td>
                <td class="text-center">{% if verb.multipleMeaning %}<span class="badge badge-danger">Yes</span>{% else %}&nbsp;{% endif %}</td>
            </tr>
            {% endfor %}
        </table>
    </section>
</article>
