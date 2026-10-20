---
layout: page
title: Projects
permalink: /projects/
description: Research software, open-source contributions, and formalizations.
nav: true
nav_order: 1
---

<div class="research-list">
{% assign research_projects = site.projects | sort: 'importance' %}
{% for project in research_projects %}
  <article class="research-row">
    <figure class="research-visual">
      {% if project.preview_after %}<span class="spectrogram-label">Input</span>{% endif %}
      <a href="{{ project.url | relative_url }}" aria-label="{{ project.title | escape }}">
        <img src="{{ project.preview | relative_url }}" alt="{{ project.preview_alt | escape }}" width="{{ project.preview_width }}" height="{{ project.preview_height }}" loading="lazy">
      </a>
      {% if project.preview_after %}
        <span class="spectrogram-label">20 inference steps</span>
        <img src="{{ project.preview_after | relative_url }}" alt="{{ project.preview_after_alt | escape }}" width="{{ project.preview_width }}" height="{{ project.preview_height }}" loading="lazy">
      {% endif %}
      {% if project.preview_caption %}<figcaption>{{ project.preview_caption }}</figcaption>{% endif %}
    </figure>
    <div class="research-copy">
      <h3><a href="{{ project.url | relative_url }}">{{ project.title }}</a></h3>
      <p class="research-summary">{{ project.summary }}</p>
      <p class="research-links">
        {% if project.code_url %}<a href="{{ project.code_url }}">code</a><span class="separator" aria-hidden="true">·</span>{% endif %}
        {% if project.docs_url %}<a href="{{ project.docs_url }}">documentation</a><span class="separator" aria-hidden="true">·</span>{% endif %}
        <a href="{{ project.url | relative_url }}">project details</a>
      </p>
    </div>
  </article>
{% endfor %}
</div>
