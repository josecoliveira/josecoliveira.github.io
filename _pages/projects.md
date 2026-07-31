---
layout: archive
title: Projects
permalink: /projects/
---

<style>
  .simple-list {
    list-style: none;
    padding: 0;
    margin: 0;
  }

  .simple-item {
    display: flex;
    gap: 0.6rem;
    padding: 0.25rem 0;
    font-size: 0.95rem;
  }

  .simple-date {
    min-width: 6rem;
    font-variant-numeric: tabular-nums;
    font-size: 0.82rem;
    flex-shrink: 0;
    margin-top: 0.1rem;
  }

  .simple-main {
    flex: 1;
  }

  .project-title a {
    text-decoration: none;
  }

  .project-title a:hover {
    text-decoration: underline;
  }

  .project-desc {
    font-size: 0.9rem;
  }
</style>

<ul class="simple-list">
  {% assign projects = site.projects | sort: 'date' | reverse %}
  {% for project in projects %}
    <li class="simple-item">
      <span class="simple-date">{{ project.date | date: "%b %Y" }}</span>
      <div class="simple-main">
        <div class="project-title"><a href="{{ project.url | relative_url }}">{{ project.title }}</a></div>
        {% if project.description %}<div class="project-desc">{{ project.description }}</div>{% endif %}
      </div>
    </li>
  {% endfor %}
</ul>
