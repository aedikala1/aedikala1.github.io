---
title: "A Tiny DreamerV3"
short_title: "DreamerV3"
track: "Frontier AI"
section: "World Models"
status: "Planned"
order: 1
description: "Learn latent dynamics in a small visual environment and train behavior through imagined trajectories."
permalink: /frontier-ai/world-models/dreamerv3/
code_path: code/frontier-ai/world-models/dreamerv3
results_path: results/frontier-ai/world-models/dreamerv3
paper_url: "https://arxiv.org/abs/2301.04104"
reference_url: "https://github.com/danijar/dreamerv3"
---

> This is a seeded outline. It becomes a full public note only after the implementation and evidence exist.

## Question

When can a compact latent dynamics model simulate useful futures well enough for a policy to improve inside them?

## Smallest useful replication

Use a small visual-control environment, train the world model, inspect open-loop imagined rollouts, and train actor and critic from latent imagination.

## Evidence to collect

- Reconstruction, reward, continuation, and dynamics losses.
- Predicted versus actual latent or decoded trajectories over increasing horizons.
- Control return and ablations that separate model quality from policy learning.

## Public write-up target

Explain the mechanism, show the smallest implementation that makes it legible, report where the result matched or diverged, and end with what became clearer by building it.

## Open questions

- Which assumption is doing the most work?
- What result would falsify the current explanation?
- What should the next, slightly larger experiment test?
