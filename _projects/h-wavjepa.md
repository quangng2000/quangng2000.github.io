---
layout: page
title: H-WavJEPA
description: Hierarchical audio representation learning across three temporal scales.
importance: 0
summary: Hierarchical audio representation research with three learned latent spaces, EMA targets, and a PyTorch Lightning + Hydra training workflow.
preview: /assets/img/research/h-wavjepa-three-latent-spaces.png
preview_alt: Proposed H-WavJEPA architecture with fine, intermediate, and coarse latent spaces, separate predictors, EMA targets, and per-level losses.
preview_width: 1586
preview_height: 992
preview_caption: Proposed forecasting design; illustrative horizons.
code_url: https://github.com/quangng2000/h-wavjepa
docs_url: https://github.com/quangng2000/h-wavjepa/blob/main/docs/ARCHITECTURE.md
---

H-WavJEPA explores learning audio representations in separate latent spaces at fine, intermediate, and coarse temporal scales. The research question is whether distinct spaces improve longer-range audio understanding while retaining useful local detail.

The repository includes a hierarchical masked-prediction prototype, EMA targets, real-WAV training, checkpoint resume, evaluation, and embedding extraction, organized with PyTorch Lightning and Hydra. It is a research implementation with no pretrained weights or established benchmark gains.

<figure class="research-visual">
  <a href="{{ page.preview | relative_url }}">
    <img src="{{ page.preview | relative_url }}" alt="{{ page.preview_alt | escape }}" width="{{ page.preview_width }}" height="{{ page.preview_height }}" loading="lazy">
  </a>
  <figcaption>Proposed three-space forecasting architecture. The 80 / 320 / 1,280 ms horizons and token counts are illustrative; the implemented prototype uses masked prediction. Select the figure to view it at full size.</figcaption>
</figure>

The proposed extension gives each level its own future predictor and compares the hierarchy with a shared-space model using the same horizons. The diagram describes this research direction rather than a demonstrated result.

[Source code and quickstart](https://github.com/quangng2000/h-wavjepa) · [Architecture and current scope](https://github.com/quangng2000/h-wavjepa/blob/main/docs/ARCHITECTURE.md)
