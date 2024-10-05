---
layout: page
permalink: /researches/
title: Researches
description: This page includes publications (including forthcoming ones) and other research-related experiences
nav: true
nav_order: 2
show_projects: true
horizontal: false
---

<!-- _pages/publications.md -->

<!-- Bibsearch Feature -->

{% include bib_search.liquid %}

<div class="publications">

{% bibliography %}

</div>


<!-- _pages/projects.md -->
{% if page.show_projects %}
    <!-- Display projects without categories -->
    {% assign sorted_projects = site.projects | sort: "importance" %}
    <!-- Generate cards for each project -->
    {% if page.horizontal %}
    <div class="container">
        <div class="row row-cols-1 row-cols-md-2">
        {% for project in sorted_projects %}
        {% include projects_horizontal.liquid %}
        {% endfor %}
        </div>
    </div>
    {% else %}
    <div class="row row-cols-1 row-cols-md-3">
        {% for project in sorted_projects %}
        {% include projects.liquid %}
        {% endfor %}
    </div>
    {% endif %}
{% endif %}

