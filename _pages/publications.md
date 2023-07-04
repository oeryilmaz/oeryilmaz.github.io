---
layout: archive
title: "Working Papers and Work in Progress"
permalink: /publications/
author_profile: true
---

{% include base_path %}

<h1>Working Papers</h1>
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

<h1>Work in Progress</h1>
{% for post in site.categories['work-in-progress'] %}
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
