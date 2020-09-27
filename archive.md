---
layout: blank
title: Archive
permalink: /archive/
---
{% assign filtered_posts = site.posts | sort: 'date' %}
<table>
    <thead>
        <tr>
            <th>Date</th>
            <th>Category</th>
            <th>Title</th>
            <th>Tags</th>
        </tr>
    </thead>
    <tbody>
        {% for post in filtered_posts %}
        <tr>
            <td>{{ post.date }}</td>
            <td>{{ post.categories }}</td>
            <td><a href="{{ post.url }}">{{ post.title }}</a></td>
            <td>{{ post.tags }}</td>
        </tr>
        {% endfor %}
    </tbody>
</table>
