---
layout: archive
title: "Working Papers"
permalink: /publications/working-papers/
author_profile: true
---

{% include base_path %}

<h2>Working Papers</h2>
{% for post in site.publications %}
  {% if post.category == 'Working Papers' %}
    <div>
      <h3>{{ post.title }}</h3>
      {% if post.venue %}<p>Venue: {{ post.venue }}</p>{% endif %}
      {% if post.excerpt %}<p>{{ post.excerpt }}</p>{% endif %}
      {% if post.paperurl %}<p><a href="{{ post.paperurl }}">{{ post.linktext | default: "Download paper here" }}</a></p>{% endif %}
      <p>{{ post.content }}</p>
    </div>
  {% endif %}
{% endfor %}

<h2>Work in Progress</h2>
{% for post in site.publications %}
  {% if post.category == 'Work in Progress' %}
    <div>
      <h3>{{ post.title }}</h3>
      {% if post.venue %}<p>Venue: {{ post.venue }}</p>{% endif %}
      {% if post.excerpt %}<p>{{ post.excerpt }}</p>{% endif %}
      {% if post.paperurl %}<p><a href="{{ post.paperurl }}">{{ post.linktext | default: "Download paper here" }}</a></p>{% endif %}
      <p>{{ post.content }}</p>
    </div>
  {% endif %}
{% endfor %}
