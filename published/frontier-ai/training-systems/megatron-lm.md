---
title: "Tensor and Pipeline Parallelism on a Small Cluster"
short_title: "Megatron-LM"
track: "Frontier AI"
section: "Training Systems"
status: "Planned"
order: 1
description: "Implement the essential communication patterns behind tensor and pipeline parallel training and measure the bubbles."
permalink: /frontier-ai/training-systems/megatron-lm/
code_path: code/frontier-ai/training-systems/megatron-lm
results_path: results/frontier-ai/training-systems/megatron-lm
paper_url: "https://arxiv.org/abs/1909.08053"
reference_url: "https://github.com/NVIDIA/Megatron-LM"
---

> This is a seeded outline. It becomes a full public note only after the implementation and evidence exist.

## Question

What communication and idle time are physically introduced when one transformer no longer fits or runs efficiently on one device?

## Smallest useful replication

Split linear layers across two or more devices, implement the required collectives, then pipeline transformer stages with microbatches.

## Evidence to collect

- Numerical equivalence with the single-device model.
- Communication volume and time for each collective.
- Pipeline utilization, bubble size, throughput, and sensitivity to microbatch count.

## Public write-up target

Explain the mechanism, show the smallest implementation that makes it legible, report where the result matched or diverged, and end with what became clearer by building it.

## Open questions

- Which assumption is doing the most work?
- What result would falsify the current explanation?
- What should the next, slightly larger experiment test?
