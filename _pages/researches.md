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
    <div style="display: flex; justify-content: space-between; align-items: center;">
        <h3 style="margin-bottom: 0.5em; margin-left: 0.2em;">Projects</h3>
    </div>
    {% include projects_layout.liquid %}
{% endif %}