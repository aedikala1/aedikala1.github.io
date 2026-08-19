---
title: "Discovering Behavioral Differences between Checkpoints"
short_title: "Behavioral Diffing"
track: "AI Safety"
section: "Interpretability & Monitoring"
status: "Planned"
order: 3
description: "Automatically search for behavior regions where two closely related checkpoints diverge, then validate the discovered differences."
permalink: /ai-safety/interpretability-monitoring/behavioral-diffing/
code_path: code/ai-safety/interpretability-monitoring/behavioral-diffing
results_path: results/ai-safety/interpretability-monitoring/behavioral-diffing
paper_url: "https://www.anthropic.com/research/diff-tool"

---

> This is a seeded outline. It becomes a full public note only after the implementation and evidence exist.

## Question

Can an automated search find meaningful model changes that a fixed benchmark and a hand-written prompt set would miss?

## Smallest useful replication

Create or select two nearby checkpoints with a known controlled difference, generate candidate prompts, score divergence, cluster behaviors, and validate discoveries on fresh prompts.

## Evidence to collect

- Recovery rate for planted differences and false-discovery controls.
- Novel, reproducible behavior clusters beyond the seed prompts.
- Comparisons against random prompts, fixed benchmarks, and output-distance baselines.

## Public write-up target

Explain the mechanism, show the smallest implementation that makes it legible, report where the result matched or diverged, and end with what became clearer by building it.

## Open questions

- Which assumption is doing the most work?
- What result would falsify the current explanation?
- What should the next, slightly larger experiment test?
