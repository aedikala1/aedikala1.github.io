---
title: "Latent Video Prediction with a Tiny V-JEPA"
short_title: "V-JEPA 2"
track: "Frontier AI"
section: "World Models"
status: "Planned"
order: 2
description: "Predict masked future representations in a controlled video world and test what physical variables the latent space captures."
permalink: /frontier-ai/world-models/v-jepa-2/
code_path: code/frontier-ai/world-models/v-jepa-2
results_path: results/frontier-ai/world-models/v-jepa-2
paper_url: "https://arxiv.org/abs/2506.09985"
reference_url: "https://github.com/facebookresearch/vjepa2"
---

> This is a seeded outline. It becomes a full public note only after the implementation and evidence exist.

## Question

Can representation prediction learn motion and object dynamics without spending capacity on exact pixel reconstruction?

## Smallest useful replication

Generate a small moving-object video dataset, train context and target encoders with a latent predictor, then probe position, velocity, and persistence.

## Evidence to collect

- Latent prediction loss on held-out motion regimes.
- Linear or lightweight probes for controlled physical variables.
- Comparisons with pixel prediction and ablations of mask geometry and prediction horizon.

## Public write-up target

Explain the mechanism, show the smallest implementation that makes it legible, report where the result matched or diverged, and end with what became clearer by building it.

## Open questions

- Which assumption is doing the most work?
- What result would falsify the current explanation?
- What should the next, slightly larger experiment test?
