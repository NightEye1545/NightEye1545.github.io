---
layout: default
title: Home
---


<div class="card" style="margin-bottom:16px">
<h1>Hey, I’m Naim.</h1>
<p class="muted">This is my dark, fast personal hub. I’ll start with Articles and add more sections later.</p>
<p style="margin-top:12px"><a href="{{ '/articles/' | relative_url }}">View Articles →</a></p>
</div>


<h2>Latest Articles</h2>
<div class="grid grid-3">
{% assign latest = site.articles | sort: 'date' | reverse | slice: 0, site.data.settings.site.items_on_home %}
{% if latest and latest.size > 0 %}
{% for post in latest %}
<div class="card">
<h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
<p class="muted">{{ post.date | date: site.data.settings.site.date_format }}</p>
{% if post.summary %}<p>{{ post.summary }}</p>{% endif %}
</div>
{% endfor %}
{% else %}
<div class="card"><p class="muted">No articles yet — coming soon.</p></div>
{% endif %}
</div>
