---
title: "Agentic Misalignment under Controlled Incentives"
short_title: "Agentic Misalignment Evals"
track: "AI Safety"
section: "Agentic Safety"
status: "Planned"
order: 1
description: "Vary goals, private information, tools, and conflicts inside a sandbox to map when strategic harmful behavior appears."
permalink: /ai-safety/agentic-safety/agentic-misalignment-evals/
code_path: code/ai-safety/agentic-safety/agentic-misalignment-evals
results_path: results/ai-safety/agentic-safety/agentic-misalignment-evals
paper_url: "https://www.anthropic.com/research/agentic-misalignment"
reference_url: "https://github.com/anthropic-experimental/agentic-misalignment"

---

> This is a seeded outline. It becomes a full public note only after the implementation and evidence exist.

## Question

Which combinations of capability, goal conflict, oversight, and available actions are sufficient to elicit strategic misalignment in a controlled setting?

## Smallest useful replication

Build a sandboxed scenario family with harmless synthetic assets. Change one factor at a time and require the agent to choose among transparent, deceptive, and deferential actions.

## Evidence to collect

- A pre-registered scenario matrix and behavioral rubric.
- Rates and confidence intervals for each behavior across controlled factors.
- Trajectory evidence, evaluator agreement, and checks against role-play or wording artifacts.

## Public write-up target

Explain the mechanism, show the smallest implementation that makes it legible, report where the result matched or diverged, and end with what became clearer by building it.

## Open questions

- Which assumption is doing the most work?
- What result would falsify the current explanation?
- What should the next, slightly larger experiment test?
