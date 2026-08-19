---
title: "Rebuilding the SWE-agent Loop"
short_title: "SWE-agent"
track: "Frontier AI"
section: "Agents"
status: "Planned"
order: 1
description: "Build a minimal coding-agent loop and vary the interface to measure how the harness changes model capability."
permalink: /frontier-ai/agents/swe-agent/
code_path: code/frontier-ai/agents/swe-agent
results_path: results/frontier-ai/agents/swe-agent
paper_url: "https://proceedings.neurips.cc/paper_files/paper/2024/hash/5a7c947568c1b1328ccc5230172e1e7c-Abstract-Conference.html"
reference_url: "https://github.com/SWE-agent/SWE-agent"
---

> This is a seeded outline. It becomes a full public note only after the implementation and evidence exist.

## Question

How much of coding-agent performance comes from the model, and how much comes from the interface, tools, state, and feedback loop?

## Smallest useful replication

Give a model a shell, file viewer, search, patching, and tests. Run a small issue set while varying one interface choice at a time.

## Evidence to collect

- Task success and cost under each interface variant.
- Trajectory-level failure taxonomy and recovery behavior.
- Exact prompts, tool schemas, environment state, and reproducible task fixtures.

## Public write-up target

Explain the mechanism, show the smallest implementation that makes it legible, report where the result matched or diverged, and end with what became clearer by building it.

## Open questions

- Which assumption is doing the most work?
- What result would falsify the current explanation?
- What should the next, slightly larger experiment test?
