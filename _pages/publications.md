---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% include base_path %}

## Working Papers

{% for post in site.publications reversed %}
  {% if post.category == "Working Papers" %}
    <div>
      <h2>{{ post.title }}</h2>
      {% if post.venue %}<p>Venue: {{ post.venue }}</p>{% endif %}
      {% if post.excerpt %}<p> {{ post.excerpt }}</p>{% endif %}
      {% if post.paperurl %}<p><a href="{{ post.paperurl }}">{{ post.linktext | default: "Download paper here" }}</a></p>{% endif %}
      <p>{{ post.content }}</p>
    </div>
  {% endif %}
{% endfor %}

## Work in Progress

{% for post in site.publications reversed %}
  {% if post.category == "Work in Progress" %}
    <div>
      <h2>{{ post.title }}</h2>
      {% if post.venue %}<p>Venue: {{ post.venue }}</p>{% endif %}
      {% if post.excerpt %}<p> {{ post.excerpt }}</p>{% endif %}
      {% if post.paperurl %}<p><a href="{{ post.paperurl }}">{{ post.linktext | default: "Download paper here" }}</a></p>{% endif %}
      <p>{{ post.content }}</p>
    </div>
  {% endif %}
{% endfor %}
