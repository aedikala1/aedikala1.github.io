# Private notes

This is the local working area for rough thoughts, copied excerpts, dead ends, experiment logs, and unreviewed interpretations.

- `frontier-ai/` mirrors the public systems and capability replications.
- `ai-safety/` mirrors the public safety experiments.
- Everything below this directory except this README and its `.gitignore` is ignored by Git.
- The site generator also excludes this directory.

Do not force-add files from here. A public write-up belongs in the matching path under `published/`.

The intended handoff is:

```text
private-notes/<track>/<section>/<topic>.md
+ code/<track>/<section>/<topic>/
+ results/<track>/<section>/<topic>/
                         ↓
               AI-assisted synthesis
                         ↓
published/<track>/<section>/<topic>.md
                         ↓
             human technical review
```
