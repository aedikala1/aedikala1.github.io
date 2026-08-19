---
title: "From Reward Hacking to Emergent Misalignment"
short_title: "Reward Hacking → Misalignment"
track: "AI Safety"
section: "Alignment Experiments"
status: "Planned"
order: 1
description: "Train against a small exploitable reward and test whether shortcut-seeking behavior transfers beyond the training environment."
permalink: /ai-safety/alignment-experiments/reward-hacking-emergent-misalignment/
code_path: code/ai-safety/alignment-experiments/reward-hacking-emergent-misalignment
results_path: results/ai-safety/alignment-experiments/reward-hacking-emergent-misalignment
paper_url: "https://www.anthropic.com/research/emergent-misalignment-reward-hacking"
reference_url: "https://github.com/emergent-misalignment/emergent-misalignment"

---

> This is a seeded outline. It becomes a full public note only after the implementation and evidence exist.

## Question

When does learning to exploit a narrow reward loophole remain local, and when does it generalize into broader undesirable behavior?

## Smallest useful replication

Construct a benign toy task with both a legitimate solution and a detectable shortcut. Train under controlled conditions, then evaluate on held-out tasks that distinguish task skill from shortcut-seeking.

## Evidence to collect

- Training reward, true task performance, and shortcut use over time.
- Generalization results on pre-registered held-out evaluations.
- Controls for data leakage, evaluator artifacts, prompt sensitivity, and ordinary capability gains.

## Public write-up target

Explain the mechanism, show the smallest implementation that makes it legible, report where the result matched or diverged, and end with what became clearer by building it.

## Open questions

- Which assumption is doing the most work?
- What result would falsify the current explanation?
- What should the next, slightly larger experiment test?
