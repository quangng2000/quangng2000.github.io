# Research image sources

These assets illustrate Quang Nguyen's linked projects. Repository images are
copied without modification; the SVGs are original diagrams of documented
project concepts.

## TEMF + WavJEPA-Nat (FiLM)

- File: `temf-wavjepa-film.gif` (800 × 600).
- Source: [film-temf-scm-preview.gif](https://github.com/quangng2000/temf-wavjepa-film/blob/main/docs/media/film-temf-scm-preview.gif).
- Context: [repository README](https://github.com/quangng2000/temf-wavjepa-film/blob/main/README.md)
  and [animation notes](https://github.com/quangng2000/temf-wavjepa-film/blob/main/docs/animation/README.md).
- This animation is a **toy numerical illustration of the method**, not output
  from a trained speech-restoration model. Its waveform and context visualizations
  must not be described as measured model results. Preserve the complete frame
  when displaying it, including its explanatory labels.

## RMFSR

- `rmfsr-input.png` (640 × 240): unchanged copy of
  [sample-01/input-rms-matched.png](https://github.com/quangng2000/rmfsr/blob/main/docs/assets/spectrograms/sample-01/input-rms-matched.png).
- `rmfsr-nfe20.png` (640 × 240): unchanged copy of
  [sample-01/nfe20-rms-matched.png](https://github.com/quangng2000/rmfsr/blob/main/docs/assets/spectrograms/sample-01/nfe20-rms-matched.png).
- Context: [listening-gallery documentation](https://github.com/quangng2000/rmfsr/blob/main/docs/README.md)
  and [sample provenance and settings](https://github.com/quangng2000/rmfsr/blob/main/docs/results.json).
- These are linear-frequency, log-magnitude STFT images from the gallery's first
  sample, with RMS-matched playback gain and a shared color scale. Label them
  “Input” and “20 steps” if shown together.
- The gallery documents a 145,000-update production EMA checkpoint with offline
  WavJEPA conditioning. These examples do not establish real-time performance,
  comparative restoration quality, or a TEMF/FiLM result. The gallery's source
  degraded recording comes from the [paper authors' demonstration](https://sebraun-msr.github.io/realtimemeanflowspeechrestoration/).

## Cajal compiler

- File: `cajal-pipeline.svg` (520 × 320).
- Original static diagram summarizing the implemented pipeline described in
  [Compiling Programs to Transformers](https://github.com/quangng2000/riftco-transformer/blob/main/docs/COMPILING_TO_TRANSFORMERS.md).
- The diagram illustrates the supported bilinear linear-attention lowering path:
  Cajal-lite program → linear type checker → multilinear map → programmed linear
  attention. Other documented lowering paths include dense and unary linear
  computation.
- Programmed linear attention here uses an identity kernel. The diagram does
  not claim that it is learned softmax attention, that arbitrary programs compile
  into attention, or that compiler correctness has a machine-checked proof.

## ELBO in Lean 4

- File: `lean-elbo.svg` (520 × 300).
- Original static mathematical illustration based on the
  [project README](https://github.com/quangng2000/lean-elbo/blob/main/README.md).
- It shows the exact ELBO decomposition and resulting lower bound for finite,
  strictly positive distributions. The graphic makes no claim about continuous
  distributions, model training, or numerical experiments.

## SMC steering

- File: `smc-steering.svg` (520 × 320).
- Original conceptual diagram for the owner's local `smc-steering` research
  prototype, documented in its README as “CTL and twisted SMC with GPT-2 Medium
  and Laya.”
- Shows learned-twist proposals, importance weighting, and adaptive particle
  resampling. Particle sizes and paths are schematic, not experimental results.
- No public repository has been identified for this project. The project entry
  links to its website overview, not to an unrelated SMC repository or the
  reference authors' implementation.
