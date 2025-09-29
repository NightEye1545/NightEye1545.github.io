---
layout: default
title: Projects
---

# Projects
<div class="grid grid-3">
  {% assign sorted = site.projects | sort: 'date' | reverse %}
  {% if sorted and sorted.size > 0 %}
    {% for project in sorted %}
      <div class="card">
        <h3><a href="{{ project.url }}">{{ project.title }}</a></h3>
        <p class="muted">{{ project.date | date: site.data.settings.site.date_format }}</p>
        {% if project.summary %}<p>{{ project.summary }}</p>{% endif %}
        {% if project.repo %}<p><a href="{{ project.repo }}">View on GitHub →</a></p>{% endif %}
      </div>
    {% endfor %}
  {% else %}
    <div class="card"><p class="muted">No projects yet — add a file under <code>/_projects/</code>.</p></div>
  {% endif %}
</div>
