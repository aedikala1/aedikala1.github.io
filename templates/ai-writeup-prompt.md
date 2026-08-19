# AI write-up prompt

Turn the rough working material for `<topic>` into a clear public research note.

Read:

- `private-notes/<track>/<section>/<topic>.md`
- `code/<track>/<section>/<topic>/`
- `results/<track>/<section>/<topic>/`
- the current `published/<track>/<section>/<topic>.md`
- the primary sources linked in that public page

Update only `published/<track>/<section>/<topic>.md`.

Use this structure unless the evidence suggests a better one:

1. What problem is being solved?
2. Core mechanism
3. My minimal implementation
4. Experiment
5. Results
6. Where my result matched or diverged
7. What I understand now
8. What surprised me
9. Open questions

Rules:

- Treat the rough notes as unverified working material, not ground truth.
- Do not invent runs, numbers, citations, implementation details, or conclusions.
- Tie every empirical claim to a specific artifact under `results/`.
- Distinguish reproduced results, observations, interpretations, and speculation.
- Preserve negative results and meaningful failure modes.
- Prefer a small concrete explanation over a literature-summary voice.
- Keep unresolved uncertainty explicit.
- Leave a visible `TODO` where evidence is missing.
- Do not change the status to `Published`; Abishek does that after technical review.

