---
title: "Activation-Aware Quantization in Practice"
short_title: "AWQ / SmoothQuant"
track: "Frontier AI"
section: "Inference"
status: "Planned"
order: 6
description: "Quantize a small model, measure the damage, then test whether activation-aware scaling recovers quality efficiently."
permalink: /frontier-ai/inference/awq-smoothquant/
code_path: code/frontier-ai/inference/awq-smoothquant
results_path: results/frontier-ai/inference/awq-smoothquant
paper_url: "https://arxiv.org/abs/2306.00978"
reference_url: "https://github.com/mit-han-lab/llm-awq"
---

> This is a seeded outline. It becomes a full public note only after the implementation and evidence exist.

## Question

Why are some channels disproportionately important under low-bit quantization, and when does equivalent scaling map to an actual hardware win?

## Smallest useful replication

Implement a simple weight-only baseline, collect activation statistics, add AWQ-style scaling, and compare with a small SmoothQuant experiment if time permits.

## Evidence to collect

- Perplexity or task accuracy before and after each quantization method.
- Model size, peak memory, latency, and any kernel constraints.
- Layer and channel analyses that explain where quantization error concentrates.

## Public write-up target

Explain the mechanism, show the smallest implementation that makes it legible, report where the result matched or diverged, and end with what became clearer by building it.

## Open questions

- Which assumption is doing the most work?
- What result would falsify the current explanation?
- What should the next, slightly larger experiment test?
