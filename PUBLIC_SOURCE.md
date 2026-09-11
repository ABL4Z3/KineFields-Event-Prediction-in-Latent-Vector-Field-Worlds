# KineFields: Blind System Identification in Latent Vector-Field Worlds — Dataset Source

This page is the canonical source reference for the **KineFields** dataset
as distributed through the Eris/Shipd platform.

## What this dataset is

A **fully synthetic** computer-vision dataset generated programmatically
with fixed random seeds by an original generator script authored for this
dataset. No third-party images, video, text, or annotations were used.
Each episode is one image — a horizontal strip of 8 consecutive observed
frames (48x48 each) of a fictional 2D world in which 5-7 glyphs move under
a latent per-scene vector field (drift / vortex / anchored attractor /
anchored repulsor / shear; a pulsating field type is held out for test
only) with undisclosed per-step stochastic jitter. Each label is the
specification of the latent law itself — the discrete field family and
attributes (type / direction sector / rotation sense / anchor glyph) PLUS
continuous parameters (field strength, center coordinates) — or `absent`
for windows that provably do not identify the law.
The field equations, parameters, anchor identities, and noise levels are
never distributed as solver inputs — they can only be inferred from pixels
and the labeled training episodes.

Contents:

| Item | Count | Description |
|---|---|---|
| Episodes | 3,820 | Image strips (384x48 RGB) + one law specification each |
| Train | 2,100 | Labeled strip -> law specification pairs |
| Test | 1,720 | Unlabeled strips across 5 hidden families |

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
