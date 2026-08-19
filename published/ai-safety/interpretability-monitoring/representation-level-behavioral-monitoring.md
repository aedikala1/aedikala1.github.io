---
title: "Hidden-State Probes versus Output-Only Monitoring"
short_title: "Representation-Level Monitoring"
track: "AI Safety"
section: "Interpretability & Monitoring"
status: "Planned"
order: 2
description: "Compare representation-level probes with output monitors on a deliberately planted, controlled behavior."
permalink: /ai-safety/interpretability-monitoring/representation-level-behavioral-monitoring/
code_path: code/ai-safety/interpretability-monitoring/representation-level-behavioral-monitoring
results_path: results/ai-safety/interpretability-monitoring/representation-level-behavioral-monitoring
paper_url: "https://www.anthropic.com/research/global-workspace"
reference_url: "https://github.com/anthropics/jacobian-lens"

---

> This is a seeded outline. It becomes a full public note only after the implementation and evidence exist.

## Question

Can internal representations reveal an upcoming behavior that remains ambiguous or absent in the model's visible output?

## Smallest useful replication

Plant or fine-tune a benign synthetic trigger-response behavior in a small open model. Train hidden-state probes and output-only monitors on matched data, then evaluate under distribution shift.

## Evidence to collect

- Detection AUROC, precision–recall, calibration, and lead time.
- Generalization to paraphrases, unseen triggers, and behavior-preserving output changes.
- Probe controls for lexical shortcuts, layer selection, and capability confounds.

## Public write-up target

Explain the mechanism, show the smallest implementation that makes it legible, report where the result matched or diverged, and end with what became clearer by building it.

## Open questions

- Which assumption is doing the most work?
- What result would falsify the current explanation?
- What should the next, slightly larger experiment test?
