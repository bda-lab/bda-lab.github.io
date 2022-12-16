---
layout: page
title: people
permalink: /people/
description:
nav: true
display_categories: [current]
horizontal: false
importance: 3
---
<div class="projects">
  {% if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
    {% for category in page.display_categories %}
      <h2 class="category">{{ category }}</h2>
      {% assign categorized_projects = site.projects | where: "category", category %}
      {% assign sorted_projects = categorized_projects | sort: "importance" %}
      <!-- Generate cards for each project -->
      {% if page.horizontal %}
        <div class="container">
          <div class="row row-cols-2">
          {% for project in sorted_projects %}
            {% include projects_horizontal.html %}
          {% endfor %}
          </div>
        </div>
      {% else %}
        <div class="grid">
          {% for project in sorted_projects %}
            {% include projects.html %}
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
        <div class="row row-cols-2">
        {% for project in sorted_projects %}
          {% include projects_horizontal.html %}
        {% endfor %}
        </div>
      </div>
    {% else %}
      <div class="grid">
        {% for project in sorted_projects %}
          {% include projects.html %}
        {% endfor %}
      </div>
    {% endif %}

  {% endif %}

  
  <b>Past iMTech PE/RE students</b> 
  <ol>
  <li>Divyam Agarwal (2022)</li>
  <li>Kautuk Raj (2022), Summer Intern 2022</li>
  <li>Srivishnu Sunku (2022)</li>
  <li>Rachna Kedigehalli (2022), Summer Intern 2022</li>
  <li>Sai Maheedhar (2022)</li>
  <li>Samaksh Dhingra (2022)</li>
  <li>Nandakishore S Menon (2022)</li>
  <li>Samaksh Dhingra (2022)</li>
  <li>Neelabh P Bhaskar (2022), Summer Intern 2022</li>
  <li>Siva Jagadesh (2022), Summer Intern 2022</li>
  </ol>
  <b>Past iMTech project students</b> 
  <ol>
  <li>Abhigna Banda (2022)</li>
  <li>Ellanti Bharath Sai (2022)</li>
  <li>Sairama Sashank Kaiyala (2022)</li>
</ol>

  <b>
Note: </b>  The PE/RE and the Project students will be graded based on: (1) Research contribution (publishing/submitting papers), (2) Consistency of their interactions with the team, (3) Understanding the overall goal of the project/research topic and their ability to make suggestions, (4) Fulfilment of the assigned tasks on time, (5) Quality of the intermediate and the final reports/presentations. 
</div>
