---
layout: page
title: RE-USE Apple
description: Offline speech enhancement on Apple silicon with Swift, MLX, and Metal.
importance: -1
summary: An independent Apple port of NVIDIA NemotronLabs RE-USE, with a shared Swift/MLX/Metal engine for a Mac CLI and an iPhone/iPad app target.
preview: /assets/img/research/reuse-apple.svg
preview_alt: Recorded audio passes through a shared Swift, MLX, and Metal RE-USE engine to produce enhanced audio, with Mac and iPhone/iPad interfaces.
preview_width: 520
preview_height: 320
preview_caption: Shared inference engine; GPU inference verified on M4 Pro.
code_url: https://github.com/quangng2000/reuse-apple
docs_url: https://github.com/quangng2000/reuse-apple/blob/main/docs/architecture.md
---

RE-USE Apple brings the pretrained 9.61M-parameter NVIDIA NemotronLabs RE-USE model to Apple silicon. It uses Swift, MLX, and Metal for offline speech enhancement, with a Mac command-line tool and an iPhone/iPad recording and import app sharing the same inference engine.

<figure class="research-visual">
  <img src="{{ page.preview | relative_url }}" alt="{{ page.preview_alt | escape }}" width="{{ page.preview_width }}" height="{{ page.preview_height }}" loading="lazy">
  <figcaption>A conceptual view of the shared inference pipeline and platform interfaces.</figcaption>
</figure>

The port includes a fused Metal Mamba scan, verified model downloads, audio conversion, and overlapping inference windows. After setup, audio processing stays on the device and produces 16 kHz mono WAV files.

## Validation

Actual GPU inference is verified on an M4 Pro. The packaged tool produced byte-for-byte identical output to the validated Swift/Metal prototype and processed a four-second diagnostic clip in approximately 2.3 seconds, excluding model loading and file I/O. Checks also cover short inputs, silence, stereo resampling, and recordings spanning multiple inference windows.

The unsigned ARM64 iPhone/iPad build passes. Physical-device installation, performance, memory, and thermal behavior remain untested; the Mac timing is not a phone benchmark or a live-streaming claim.

## Model and attribution

This is an independent port of [NVIDIA NemotronLabs RE-USE](https://huggingface.co/nvidia/NVIDIA-NemotronLabs-RE-USE). NVIDIA developed and trained the model; this project adapts inference and application packaging for Apple platforms. The pinned checkpoint permits commercial use under OpenMDW-1.1, with its license and attribution notices retained.

[Code and quickstart](https://github.com/quangng2000/reuse-apple) · [Validation details](https://github.com/quangng2000/reuse-apple/blob/main/docs/validation.md) · [RE-USE paper](https://arxiv.org/abs/2603.02641)
