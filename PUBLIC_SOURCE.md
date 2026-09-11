# KineFields: Governing-Law Recovery from Time-Integrated Neuromorphic Observations — Dataset Source

This page is the canonical source reference for the **KineFields** dataset
as distributed through the Eris/Shipd platform.

## What this dataset is

A **fully synthetic** computer-vision dataset generated programmatically
with fixed random seeds by an original generator script authored for this
dataset. No third-party images, video, text, or annotations were used.
Each episode is one 64x64 image: a **time-integrated observation** of a
fictional 2D world, rendered with a stroboscopic / event-integrating
sensor model — 12 exposure instants of 5-7 glyphs moving under a latent
per-scene vector field (drift / vortex / anchored attractor / anchored
repulsor / shear; a pulsating field type is held out for test only) with
undisclosed per-step stochastic jitter, composited with a monotone
brightness ramp so the newest instant is brightest. Each label is the
specification of the latent law itself — the discrete field family and
attributes (type / direction sector / rotation sense / anchor glyph) PLUS
continuous parameters (field strength, center coordinates) — or `absent`
for windows that provably do not identify the law. The field equations,
parameters, anchor identities, noise levels, and the latent trajectories
are never distributed as solver inputs — they can only be inferred from
pixels and the labeled training episodes.

Contents:

| Item | Count | Description |
|---|---|---|
| Episodes | 3,820 | 64x64 RGB time-integrated observations + one law specification each |
| Train | 2,100 | Labeled observation -> law specification pairs |
| Test | 1,720 | Unlabeled observations across 5 hidden families |

Hidden test families isolate an unseen field type (pulsating attractor),
an unseen weak-strength regime, an unseen high-jitter regime, and
abstention calibration on provably ambiguous windows.

## License

**CC0 1.0 Universal (Public Domain Dedication)**
https://creativecommons.org/publicdomain/zero/1.0/

The generator script and all generated artifacts are original work
released under CC0. There are no restrictions on redistribution,
modification, or commercial use.

## Provenance

- Generation: deterministic scripted simulation + rendering (fixed seeds);
  reproducible byte-for-byte from the generator.
- No personal data, no third-party imagery or text, no scraped content.
  All worlds, glyphs, fields, and labels are fictional and
  machine-generated.
- Contact: dataset author via the Eris/Shipd platform.
