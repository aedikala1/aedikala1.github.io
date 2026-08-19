# Frontier Notes

A low-maintenance GitHub Pages research notebook for Abishek Edikala: private rough notes in, reviewed replication write-ups out.

## Structure

```text
frontier-notes/
├── private-notes/                  # local-only; ignored by Git and Jekyll
│   ├── frontier-ai/
│   └── ai-safety/
├── published/                      # Markdown pages shown on the site
│   ├── frontier-ai/
│   └── ai-safety/
├── code/                           # runnable implementations
│   ├── frontier-ai/
│   └── ai-safety/
├── results/                        # plots, tables, eval fixtures, summaries
│   ├── frontier-ai/
│   └── ai-safety/
├── templates/                      # note template and AI synthesis prompt
├── _layouts/                       # sparse Jekyll presentation
├── assets/css/style.css
└── index.html
```

The two tracks stay separate inside every working directory but appear together on one site.

## Notes-first workflow

1. Work in the matching file under `private-notes/`.
2. Put the runnable artifact in the matching `code/` directory.
3. Put measurements, plots, and evaluation evidence in `results/`.
4. Use `templates/ai-writeup-prompt.md` to draft or revise the matching page under `published/`.
5. Verify every claim, citation, and number yourself.
6. Change `status: "Planned"` to `status: "In progress"` or `status: "Published"`, then commit.

The first five projects are intentionally ordered as:

1. FlashAttention
2. Reward hacking → emergent misalignment
3. Agentic misalignment evaluations
4. GRPO / RLVR
5. Sparse-autoencoder feature interpretability

## Privacy boundary

Files under `private-notes/` are ignored by Git, and `_config.yml` excludes the directory from the generated site. The directory README is public; the actual scratchpads are local-only.

Before the first push, verify this once:

```sh
git status --short
git check-ignore -v private-notes/frontier-ai/inference/flashattention.md
```

Never force-add a file from `private-notes/`. GitHub cannot make one directory inside a public repository private; not committing the files is the privacy mechanism.

## Preview locally

```sh
bundle install
bundle exec jekyll serve --baseurl ""
```

Then open `http://127.0.0.1:4000`.

## Publish with GitHub Pages

This site uses only GitHub Pages' built-in Jekyll features. There is no custom deployment workflow to maintain.

1. Create the public repository `aedikala1/frontier-notes`.
2. Push the `main` branch.
3. In **Settings → Pages**, choose **Deploy from a branch**, `main`, and `/(root)`.
4. Future pushes publish automatically at `https://aedikala1.github.io/frontier-notes/`.

If the repository name changes, update `baseurl`, `repository`, and `repository_url` in `_config.yml`.

## Add a topic

Mirror the same path under `private-notes/`, `published/`, `code/`, and `results/`. Start from the templates instead of inventing a new format.

