# shenn667.github.io — staging

Static site for `https://shenn667.github.io/` (repo `shenn667/shenn667.github.io`).

Status 2026-11-21: published to GitHub (`shenn667/shenn667.github.io`, branch
`main`) and served from the repository root by GitHub Pages. Pages showcase the
current PyPI release `cited-rag v0.1.1` (70 tests); the 52-question SQE eval was
measured on v0.1.0 and remains identical on v0.1.1.

## Content

- `index.html` — home, links to `/eval/`
- `eval/index.html` — SQE eval page for cited-rag (baseline v0.1.0, current PyPI v0.1.1 / 70 tests)
  (protocol, Recall@5=1.00, MRR=0.93, correct-refusal 12/12, n=52,
  gates C1–C6, honest limitations, artifact links). The 52-question SQE eval was
  measured on v0.1.0 and remains identical on v0.1.1.
- No build step, no tracker, plain static HTML (Pages-ready).

## Links state

| Link | URL | State |
|---|---|---|
| PyPI | https://pypi.org/project/cited-rag/ | live (v0.1.1, 70 tests) |
| GitHub | https://github.com/shenn667/cited-rag | live |
| HF dataset | https://huggingface.co/datasets/SHENNN667/cited-rag-golden-52 | live (HTTP 200) |
| dev.to | https://dev.to/shenn667/zero-dependency-verified-agents-cited-or-refused-gated-in-ci-3fnh | live (HTTP 200, 2026-11-18) |
| Glama Registry | https://glama.ai/mcp/servers/shenn667/agent-context-bridge | live (HTTP 200); MCP context pillar, not cited-rag itself |

## Publish (done)

```bash
cd ~/ai_env/labs/shenn667.github.io
git remote add origin git@github.com:shenn667/shenn667.github.io.git
git push -u origin main
# Settings → Pages → Deploy from branch → main → / (root)
# https://shenn667.github.io/ and https://shenn667.github.io/eval/
```

## Verify locally

```bash
python3 -m http.server 8000 --directory ~/ai_env/labs/shenn667.github.io
# open http://localhost:8000/ and http://localhost:8000/eval/
```
