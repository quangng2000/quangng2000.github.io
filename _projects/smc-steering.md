---
layout: page
title: SMC Steering with Learned Twisting Functions
description: Probabilistic language-model steering with contrastive twist learning and sequential Monte Carlo.
importance: 3
summary: Inference-time language-model steering with learned twisting functions, importance weighting, and adaptive sequential Monte Carlo resampling.
preview: /assets/img/research/smc-steering.svg
preview_alt: A learned twisting function guides sequence proposals, followed by importance weighting and adaptive resampling.
preview_width: 520
preview_height: 320
---

A research prototype exploring inference-time language-model steering with learned twisting functions and sequential Monte Carlo (SMC).

This implementation studies the approach introduced by Zhao et al. in [Probabilistic Inference in Language Models via Twisted Sequential Monte Carlo](https://arxiv.org/abs/2404.17546).

The implementation trains a twisting function through **contrastive twist learning (CTL)** while keeping the base language model frozen. PyTorch/Pyro experiments use GPT-2 Medium and Qwen3-0.6B, with terminal review-scoring objectives.

The experiments compare unsteered generation, terminal-score weighting, twisted sequential importance sampling (SIS), and twisted SMC. Fixed-length and end-of-sequence variants track effective sample size, particle ancestry, and terminal scores to examine weight concentration and resampling behavior.

This is experimental research on sampling and steering; the current validation does not establish an improvement in text quality.
