---
layout: archive
title: "Research"
permalink: /publications/
author_profile: true
---

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

{% for post in site.publications reversed %}
  <div>
    <h2>{{ post.title }}</h2>
    {% if post.date %}<p>Date: {{ post.date | date: "%B %Y" }}</p>{% endif %}
    {% if post.venue %}<p>Venue: {{ post.venue }}</p>{% endif %}
    {% if post.excerpt %}<p>Excerpt: {{ post.excerpt }}</p>{% endif %}
    {% if post.paperurl %}<p><a href="{{ post.paperurl }}">{{ post.linktext | default: "Download paper here" }}</a></p>{% endif %}
    {% if post.citation %}<p>Recommended citation: {{ post.citation }}</p>{% endif %}
    <p>{{ post.content }}</p>
  </div>
{% endfor %}
