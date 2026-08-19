---
title: "FlashAttention from First Principles"
short_title: "FlashAttention"
track: "Frontier AI"
section: "Inference"
status: "Planned"
order: 1
description: "Rebuild exact attention around IO-aware tiling and online softmax, then measure when memory movement becomes the bottleneck."
permalink: /frontier-ai/inference/flashattention/
code_path: code/frontier-ai/inference/flashattention
results_path: results/frontier-ai/inference/flashattention
paper_url: "https://proceedings.neurips.cc/paper/2022/hash/67d57c32e20fd0a7a302cb81d36e40d5-Abstract-Conference.html"
reference_url: "https://github.com/Dao-AILab/flash-attention"
---

> This is a seeded outline. It becomes a full public note only after the implementation and evidence exist.

## Question

How does changing the movement of attention tensors through the memory hierarchy change practical performance without changing the exact result?

## Smallest useful replication

Start with a clear reference implementation, add tiled forward attention with online softmax, then add the backward pass. Compare correctness, memory use, and runtime across sequence lengths and head dimensions.

## Evidence to collect

- Output and gradient error against a trusted reference.
- Peak memory, wall time, and achieved throughput across a fixed benchmark grid.
- A profiler trace that explains the crossover between naive and tiled attention.

## Public write-up target

Explain the mechanism, show the smallest implementation that makes it legible, report where the result matched or diverged, and end with what became clearer by building it.

## Open questions

- Which assumption is doing the most work?
- What result would falsify the current explanation?
- What should the next, slightly larger experiment test?
