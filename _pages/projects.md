---
layout: my-page
title: My Projects
permalink: /projects/
description: 
nav: true
nav_order: 2
my_special_view: true
---

<!-- This page contains a showcase of some selected projects that I undertook throughout the years. -->
<div class="projects">
  {% if page.my_special_view %}
    {% assign sorted_projects = site.projects | sort: "importance" %}
    {% for project in sorted_projects %}
      {% assign alignment = forloop.index0 | modulo: 2 | plus: 0 %}
      {% include my_projects_custom.liquid alignment=alignment %}
    {% endfor %}
  {% else %}
</div>

  <!-- pages/projects.md -->
  <div class="projects">
  {% if site.enable_project_categories and page.display_categories %}
    <!-- Display categorized projects -->
    {% for category in page.display_categories %}
    <a id="{{ category }}" href=".#{{ category }}">
      <h2 class="category">{{ category }}</h2>
    </a>
    {% assign categorized_projects = site.projects | where: "category", category %}
    {% assign sorted_projects = categorized_projects | sort: "importance" %}
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
    {% endfor %}

  {% else %}

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
  </div>
{% endif %}
