# KineFields: Event Prediction in Latent Vector-Field Worlds — Dataset Source

This page is the canonical source reference for the **KineFields** dataset
as distributed through the Eris/Shipd platform.

## What this dataset is

A **fully synthetic** computer-vision dataset generated programmatically
with fixed random seeds by an original generator script authored for this
dataset. No third-party images, video, text, or annotations were used.
Each episode is one image — a horizontal strip of 6 consecutive observed
frames (48x48 each) of a fictional 2D world in which 4-6 glyphs move under
a latent per-scene vector field (drift / vortex / anchored attractor /
anchored repulsor / shear; a pulsating field type is held out for test
only) with undisclosed per-step stochastic jitter. Each label is an event
token over the unobserved future of the same world (first object to exit
the frame, count inside a central disc at the horizon, relative exit
order, or the outcome of a counterfactual removal of the field's anchor
glyph), or `absent` for questions referencing a nonexistent object. The
field parameters, anchor identities, noise realizations, and future frames
are never distributed — they can only be inferred from pixels and the
labeled training episodes.

Contents:

| Item | Count | Description |
|---|---|---|
| Episodes | 4,860 | Image strips (288x48 RGB) + one question each |
| Train | 2,600 | Labeled episode -> event token pairs |
| Test | 2,260 | Unlabeled episodes across 7 hidden families |

Hidden test families isolate an unseen field type, an unseen prediction
horizon (beyond any training episode), counterfactual anchor removal, and
abstention calibration.

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
  All worlds, glyphs, fields, and questions are fictional and
  machine-generated.
- Contact: dataset author via the Eris/Shipd platform.
