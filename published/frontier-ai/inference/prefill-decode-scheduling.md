---
title: "Chunked Prefill and Prefill–Decode Scheduling"
short_title: "SARATHI / DistServe"
track: "Frontier AI"
section: "Inference"
status: "Planned"
order: 5
description: "Reproduce the latency–throughput tradeoff behind chunked prefill and the separation of prefill from decode."
permalink: /frontier-ai/inference/prefill-decode-scheduling/
code_path: code/frontier-ai/inference/prefill-decode-scheduling
results_path: results/frontier-ai/inference/prefill-decode-scheduling
paper_url: "https://arxiv.org/abs/2308.16369"
reference_url: "https://github.com/microsoft/sarathi-serve"
---

> This is a seeded outline. It becomes a full public note only after the implementation and evidence exist.

## Question

How should a serving system schedule compute-heavy prefill beside bandwidth-heavy decode without starving either workload?

## Smallest useful replication

Create a baseline iteration scheduler, add chunked prefill, and optionally simulate separate prefill and decode workers. Use the same request trace for every policy.

## Evidence to collect

- TTFT, time per output token, throughput, and goodput.
- Iteration-level GPU work or a faithful resource simulation.
- Sensitivity to prompt length, generation length, load, and chunk size.

## Public write-up target

Explain the mechanism, show the smallest implementation that makes it legible, report where the result matched or diverged, and end with what became clearer by building it.

## Open questions

- Which assumption is doing the most work?
- What result would falsify the current explanation?
- What should the next, slightly larger experiment test?
