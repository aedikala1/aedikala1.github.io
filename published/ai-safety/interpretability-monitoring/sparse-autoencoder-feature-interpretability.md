---
title: "Finding and Steering Features with a Sparse Autoencoder"
short_title: "Feature Interpretability"
track: "AI Safety"
section: "Interpretability & Monitoring"
status: "Planned"
order: 1
description: "Extract sparse features from a small open model, interpret selected features, and test their causal effect with interventions."
permalink: /ai-safety/interpretability-monitoring/sparse-autoencoder-feature-interpretability/
code_path: code/ai-safety/interpretability-monitoring/sparse-autoencoder-feature-interpretability
results_path: results/ai-safety/interpretability-monitoring/sparse-autoencoder-feature-interpretability
paper_url: "https://transformer-circuits.pub/2024/scaling-monosemanticity/"
reference_url: "https://github.com/openai/sparse_autoencoder"

---

> This is a seeded outline. It becomes a full public note only after the implementation and evidence exist.

## Question

Do sparse features correspond to stable, causally meaningful computations rather than merely interpretable correlations?

## Smallest useful replication

Collect activations, train a sparse autoencoder, select features with a pre-defined discovery process, generate activating examples, and intervene during inference.

## Evidence to collect

- Reconstruction quality, sparsity, feature frequency, and dead-feature rates.
- Blind or semi-blind interpretation checks on held-out activations.
- Dose-response intervention curves and specificity controls.

## Public write-up target

Explain the mechanism, show the smallest implementation that makes it legible, report where the result matched or diverged, and end with what became clearer by building it.

## Open questions

- Which assumption is doing the most work?
- What result would falsify the current explanation?
- What should the next, slightly larger experiment test?
