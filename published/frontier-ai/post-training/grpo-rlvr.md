---
title: "GRPO and RLVR on a Tiny Verifiable Task"
short_title: "GRPO / RLVR"
track: "Frontier AI"
section: "Post-training"
status: "Planned"
order: 2
description: "Train a small policy against exact rewards and watch its strategy, entropy, response length, and accuracy change."
permalink: /frontier-ai/post-training/grpo-rlvr/
code_path: code/frontier-ai/post-training/grpo-rlvr
results_path: results/frontier-ai/post-training/grpo-rlvr
paper_url: "https://arxiv.org/abs/2402.03300"
reference_url: "https://github.com/deepseek-ai/DeepSeek-Math"
---

> This is a seeded outline. It becomes a full public note only after the implementation and evidence exist.

## Question

What does group-relative advantage estimation do to a reasoning policy when rewards can be checked exactly?

## Smallest useful replication

Use arithmetic, Countdown, or another tiny verifier-backed environment. Sample response groups, compute relative advantages, apply GRPO updates, and retain complete training traces.

## Evidence to collect

- Reward, accuracy, entropy, KL, and response length over training.
- Examples of strategy change rather than only aggregate score change.
- Ablations for group size, verifier quality, clipping, and reward normalization.

## Public write-up target

Explain the mechanism, show the smallest implementation that makes it legible, report where the result matched or diverged, and end with what became clearer by building it.

## Open questions

- Which assumption is doing the most work?
- What result would falsify the current explanation?
- What should the next, slightly larger experiment test?
