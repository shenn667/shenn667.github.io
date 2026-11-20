# shenn667.github.io — staging

Static site for `https://shenn667.github.io/` (repo `shenn667/shenn667.github.io`).

Status 2026-11-20: the repo **does not exist yet** (GitHub API → 404,
`https://shenn667.github.io/` → 404) and no GitHub credential is available
locally (`gh auth status` negative, keymaster: `GITHUB_CRED: ABSENT`).
Nothing was pushed. This directory is the publish-ready staging.

## Content

- `index.html` — home, links to `/eval/`
- `eval/index.html` — SQE eval page for cited-rag v0.1.0
  (protocol, Recall@5=1.00, MRR=0.93, correct-refusal 12/12, n=52,
  gates C1–C6, honest limitations, artifact links).
- No build step, no tracker, plain static HTML (Pages-ready).

## Links state

| Link | URL | State |
|---|---|---|
| PyPI | https://pypi.org/project/cited-rag/ | live (v0.1.0 verified) |
| GitHub | https://github.com/shenn667/cited-rag | live |
| HF dataset | https://huggingface.co/datasets/shenn667/cited-rag-golden-52 | per spec; publication in parallel (may 404 until public) |
| dev.to | https://dev.to/shenn667/zero-dependency-verified-agents-cited-or-refused-gated-in-ci-3fnh | live (2026-11-18, found via search) |
| Glama Registry | — | **TODO**: no listing found; cited-rag is a CLI, not an MCP server. See `TODO(glama, founder)` comment in `eval/index.html`. |

## Publish (founder, needs GitHub auth)

```bash
cd ~/ai_env/labs/shenn667.github.io
git init -b main  # already initialised if committed
gh repo create shenn667/shenn667.github.io --public --source=. --push
# Settings → Pages → Deploy from branch → main → / (root). Then:
# https://shenn667.github.io/ and https://shenn667.github.io/eval/
```

## Verify locally

```bash
python3 -m http.server 8000 --directory ~/ai_env/labs/shenn667.github.io
# open http://localhost:8000/ and http://localhost:8000/eval/
```
