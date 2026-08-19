---
title: "RadixAttention for Reused Agent Context"
short_title: "SGLang / RadixAttention"
track: "Frontier AI"
section: "Inference"
status: "Planned"
order: 4
description: "Add prefix-aware KV reuse with a radix tree and test how shared context changes serving efficiency."
permalink: /frontier-ai/inference/radixattention-sglang/
code_path: code/frontier-ai/inference/radixattention-sglang
results_path: results/frontier-ai/inference/radixattention-sglang
paper_url: "https://arxiv.org/abs/2312.07104"
reference_url: "https://github.com/sgl-project/sglang"
---

> This is a seeded outline. It becomes a full public note only after the implementation and evidence exist.

## Question

How much work can an inference runtime avoid when requests share system prompts, histories, branches, or tool context?

## Smallest useful replication

Build a radix-tree prefix cache that maps token prefixes to KV blocks, supports reference counts, and evicts cold prefixes. Replay branching agent-like request traces.

## Evidence to collect

- Cache correctness across inserts, splits, shared prefixes, and eviction.
- Prefix hit rate, reused tokens, TTFT, and memory occupancy.
- A trace showing when reuse helps and when cache management dominates.

## Public write-up target

Explain the mechanism, show the smallest implementation that makes it legible, report where the result matched or diverged, and end with what became clearer by building it.

## Open questions

- Which assumption is doing the most work?
- What result would falsify the current explanation?
- What should the next, slightly larger experiment test?
