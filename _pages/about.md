---
layout: default
title: About
permalink: /
---

<div class="post research-home">
  <header class="post-header">
    <div class="identity-row">
      <h1 class="post-title">Quang Nguyen</h1>
      <a class="identity-social" href="https://github.com/quangng2000" aria-label="GitHub profile"><i class="fa-brands fa-github" aria-hidden="true"></i></a>
    </div>
    <p class="desc">ML research</p>
  </header>

  <section class="research-intro" aria-labelledby="short-bio">
    <h2 class="research-section-heading" id="short-bio">Short bio</h2>
    <p>I'm Quang Nguyen. My research explores how symbolic structure and learned representations can work together in machine learning.</p>
    <p>I build research software connecting typed programs to transformers, generative models to speech restoration, and formal proofs to the mathematical foundations of learning. My current work includes the Cajal compiler, TEMF with WavJEPA and FiLM conditioning, language-model steering with learned twisting functions and sequential Monte Carlo, and an ELBO formalization in Lean 4.</p>
  </section>

  <section aria-labelledby="research-interests">
    <h2 class="research-section-heading" id="research-interests">Research interests</h2>
    <ul class="research-interests">
      <li>Neuro-symbolic learning and program-to-transformer compilation</li>
      <li>Generative speech restoration and audio representation learning</li>
      <li>Probabilistic inference and language-model steering with twisted SMC</li>
      <li>Formal methods and mathematical foundations of machine learning</li>
    </ul>
  </section>

  <section aria-labelledby="selected-work">
    <h2 class="research-section-heading" id="selected-work">Research projects</h2>
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
  </section>
</div>
