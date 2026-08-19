---
title: "Direct Preference Optimization from the Loss"
short_title: "DPO"
track: "Frontier AI"
section: "Post-training"
status: "Planned"
order: 1
description: "Implement DPO directly on a small preference dataset and make the roles of the policy, reference model, and KL pressure visible."
permalink: /frontier-ai/post-training/dpo/
code_path: code/frontier-ai/post-training/dpo
results_path: results/frontier-ai/post-training/dpo
paper_url: "https://arxiv.org/abs/2305.18290"
reference_url: "https://github.com/eric-mitchell/direct-preference-optimization"
---

> This is a seeded outline. It becomes a full public note only after the implementation and evidence exist.

## Question

How does a classification-like preference loss recover the behavior of a KL-constrained reward optimization problem?

## Smallest useful replication

Derive and implement the per-example loss, preference-tune a small model, and compare multiple beta values against the frozen reference policy.

## Evidence to collect

- Unit tests for chosen and rejected log-probability terms.
- Preference accuracy, held-out behavior, and divergence from the reference.
- Examples showing useful movement, over-optimization, and sensitivity to data quality.

## Public write-up target

Explain the mechanism, show the smallest implementation that makes it legible, report where the result matched or diverged, and end with what became clearer by building it.

## Open questions

- Which assumption is doing the most work?
- What result would falsify the current explanation?
- What should the next, slightly larger experiment test?
