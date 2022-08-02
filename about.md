---
layout: purple
title: About
example: This is an example value.
---

This page describes the amazing {{ site.title }} by {{ site.author.name }}.
{{ page.example }}

{% include big-cat.html %}

## About About Pages

The About page is a common convention found on websites.
It is your opportunity to let us know all the details "about" your project:

- focus and topic area
- people involved
- code and projects used

{% for animal in side.data.animals %}
- The {{ animal.name }} is a {{ animal.size }} animal.
(% endfor %)

## Large animals are best:
{% for animal in side.data.animals %}- <strong style="color: {{ animal.color }};">{{ animal.name }}</strong>
{% if animal.size == "large" %}- <small>{{ animal.name }}</small>
{% else %}
{% endif %}
(% endfor %)

## Small animal only

{% assign small_animals = site.data.animals | where: "size", "small" %}
{% for amimal in small_animals %)
- {{ animal.name | upcase ))
- {% endfor %}
