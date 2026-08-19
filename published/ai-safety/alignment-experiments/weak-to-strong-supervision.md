---
title: "A Small Weak-to-Strong Supervision Experiment"
short_title: "Weak-to-Strong Supervision"
track: "AI Safety"
section: "Alignment Experiments"
status: "Planned"
order: 2
description: "Train a stronger student from a deliberately weaker supervisor and measure what knowledge is recovered, copied, or lost."
permalink: /ai-safety/alignment-experiments/weak-to-strong-supervision/
code_path: code/ai-safety/alignment-experiments/weak-to-strong-supervision
results_path: results/ai-safety/alignment-experiments/weak-to-strong-supervision
paper_url: "https://arxiv.org/abs/2312.09390"
reference_url: "https://github.com/openai/weak-to-strong"

---

> This is a seeded outline. It becomes a full public note only after the implementation and evidence exist.

## Question

Can a stronger model learn beyond the observable capability of a weak supervisor without simply inheriting its systematic errors?

## Smallest useful replication

Create weak and strong model roles on a task with hidden ground truth, generate weak labels or critiques, train the strong student, and compare several supervision strategies.

## Evidence to collect

- Weak supervisor, strong ceiling, imitation baseline, and weak-to-strong performance.
- Error overlap showing which supervisor mistakes transfer.
- Sensitivity to confidence, disagreement filtering, critique, and unlabeled data.

## Public write-up target

Explain the mechanism, show the smallest implementation that makes it legible, report where the result matched or diverged, and end with what became clearer by building it.

## Open questions

- Which assumption is doing the most work?
- What result would falsify the current explanation?
- What should the next, slightly larger experiment test?
