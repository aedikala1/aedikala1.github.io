---
title: "PagedAttention by Building a KV-Cache Allocator"
short_title: "PagedAttention"
track: "Frontier AI"
section: "Inference"
status: "Planned"
order: 2
description: "Build a block-based KV allocator and continuous batcher to make fragmentation, scheduling, and throughput concrete."
permalink: /frontier-ai/inference/pagedattention/
code_path: code/frontier-ai/inference/pagedattention
results_path: results/frontier-ai/inference/pagedattention
paper_url: "https://doi.org/10.1145/3600006.3613165"
reference_url: "https://github.com/vllm-project/vllm"
---

> This is a seeded outline. It becomes a full public note only after the implementation and evidence exist.

## Question

What changes when KV cache is managed as non-contiguous blocks instead of one contiguous allocation per request?

## Smallest useful replication

Implement a tiny allocator with logical-to-physical block tables, request growth, block reuse, and continuous batching. Drive it with synthetic request traces before integrating a small model.

## Evidence to collect

- Allocator invariants and stress tests under request churn.
- Reserved versus used KV memory for contiguous and paged allocation.
- Throughput and latency under the same arrival and sequence-length traces.

## Public write-up target

Explain the mechanism, show the smallest implementation that makes it legible, report where the result matched or diverged, and end with what became clearer by building it.

## Open questions

- Which assumption is doing the most work?
- What result would falsify the current explanation?
- What should the next, slightly larger experiment test?
