---
layout: archive
title: "Working Papers"
permalink: /working-papers/
author_profile: true
---

{% include base_path %}

{% for post in site.categories['working-papers'] %}
  <div>
    <h2>{{ post.title }}</h2>
    {% if post.date %}<p>Date: {{ post.date | date: "%B %Y" }}</p>{% endif %}
    {% if post.citation %}<p>Recommended citation: {{ post.citation }}</p>{% endif %}
    {% if post.venue %}<p>Venue: {{ post.venue }}</p>{% endif %}
    {% if post.excerpt %}<p> {{ post.excerpt }}</p>{% endif %}
    {% if post.paperurl %}<p><a href="{{ post.paperurl }}">{{ post.linktext | default: "Download paper here" }}</a></p>{% endif %}
    <p>{{ post.content }}</p>
  </div>
{% endfor %}
