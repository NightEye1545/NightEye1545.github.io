---
layout: default
title: Articles
---


# Articles
<div class="grid grid-3">
{% assign sorted = site.articles | sort: 'date' | reverse %}
{% if sorted and sorted.size > 0 %}
{% for post in sorted %}
<div class="card">
<h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
<p class="muted">{{ post.date | date: site.data.settings.site.date_format }}</p>
{% if post.summary %}<p>{{ post.summary }}</p>{% endif %}
</div>
{% endfor %}
{% else %}
<div class="card"><p class="muted">Nothing here yet. Add a file to <code>/_articles/</code>.</p></div>
{% endif %}
</div>
