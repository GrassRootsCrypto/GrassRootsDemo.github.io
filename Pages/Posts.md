---
permalink: Pages/Posts/
title: "My Services"
layout: splash
last_modified_at: 2017-10-20T12:42:38-04:00
---

<h3 class="archive__subtitle">Recent Posts</h3>

{% if paginator %}
  {% assign posts = paginator.posts %}
{% else %}
  {% assign posts = site.posts %}
{% endif %}

{% assign entries_layout = page.entries_layout | default: 'list' %}
<div class="entries-{{ entries_layout }}">
  {% for post in posts %}
    {% include archive-single.html type=entries_layout %}
  {% endfor %}
</div>


{% include paginator.html %}


