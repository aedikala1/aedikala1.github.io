---
title: "Speculative Decoding from the Sampling Equations"
short_title: "Speculative Decoding"
track: "Frontier AI"
section: "Inference"
status: "Planned"
order: 3
description: "Implement exact draft-and-verify sampling and locate the regimes where extra draft work becomes a real speedup."
permalink: /frontier-ai/inference/speculative-decoding/
code_path: code/frontier-ai/inference/speculative-decoding
results_path: results/frontier-ai/inference/speculative-decoding
paper_url: "https://proceedings.mlr.press/v202/leviathan23a.html"
---

> This is a seeded outline. It becomes a full public note only after the implementation and evidence exist.

## Question

How can a cheap draft model propose several tokens while a target model preserves its original output distribution exactly?

## Smallest useful replication

Implement the acceptance and correction rules directly, test them on toy distributions, then pair small draft and target models and sweep proposal length.

## Evidence to collect

- Distributional tests showing the sampler matches the target.
- Acceptance rate, tokens per target pass, latency, and speedup.
- Failure regimes where draft overhead or poor agreement removes the benefit.

## Public write-up target

Explain the mechanism, show the smallest implementation that makes it legible, report where the result matched or diverged, and end with what became clearer by building it.

## Open questions

- Which assumption is doing the most work?
- What result would falsify the current explanation?
- What should the next, slightly larger experiment test?
