---
layout: archive
title: "Working Papers"
permalink: /publications/
author_profile: true
---

{% include base_path %}

{% for post in site.publications reversed %}
  {% if post.publication_type == 'working-papers' %}
  <div>
    <h2>{{ post.title }}</h2>
    {% comment %}
    {% if post.date %}<p>Date: {{ post.date | date: "%B %Y" }}</p>{% endif %}
    {% if post.citation %}<p>Recommended citation: {{ post.citation }}</p>{% endif %}
    {% endcomment %}
    {% if post.venue %}<p>Venue: {{ post.venue }}</p>{% endif %}
    {% if post.excerpt %}<p> {{ post.excerpt }}</p>{% endif %}
    {% if post.paperurl %}<p><a href="{{ post.paperurl }}">{{ post.linktext | default: "Download paper here" }}</a></p>{% endif %}
    <p>{{ post.content }}</p>
  </div>
  {% endif %}
{% endfor %}
