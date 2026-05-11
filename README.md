# The Commit & Ledger

**Live:** https://alecmeeeker.github.io/local-ai-newsroom-ledger/

An interactive visualization of every commit pushed to a working **local AI newsroom platform** — the engine behind [Bushwick Daily](https://bushwickdaily.com). Daily lines-of-code growth across nine subsystems: scrapers, vector store, multi-agent pipeline, editor HITL UI, publish stack, and the supporting infrastructure.

Ten months. One operator. ~880,000 lines.

## What this is

A single-page chart. No build step. No backend.

- Data: real `git ls-tree` + `git cat-file --batch` snapshots, one per day with a commit (127 days), counted exactly — not approximate.
- Chart: [Chart.js](https://www.chartjs.org/) via CDN, with annotations for 22 milestone commits.
- Type: [Fraunces](https://fonts.google.com/specimen/Fraunces) (display serif, variable optical size) + [JetBrains Mono](https://www.jetbrains.com/lp/mono/).
- Aesthetic: newsroom wire / financial-terminal hybrid — paper cream, ink black, oxblood accent.

## Why it exists

Local journalism is being gutted while general-purpose AI eats the rest of the internet. This codebase is a one-person wager that a properly engineered newsroom — not another LLM wrapper — can produce more original local reporting, faster and cheaper, than the model that killed the alt-weekly.

The platform is open-sourced piece by piece so other local outlets can fork, adapt, and survive.

## Who built it

[**Alec Meeker**](https://alecmeeker.com) — founder and editor-in-chief of Bushwick Daily.

- Site: [alecmeeker.com](https://alecmeeker.com)
- GitHub: [@alecmeeeker](https://github.com/alecmeeeker)
- LinkedIn: [linkedin.com/in/alecmeeker](https://linkedin.com/in/alecmeeker)

## Regenerating the data

The `index.html` in this repo is a static snapshot. The generator script lives in the source repo. To rebuild from a fresh commit history:

```bash
python3 viz/git_loc_growth.py
```

Runs in ~20 seconds and writes a new `loc_growth.html` with the latest sample.

## License

Visualization code: MIT. Underlying platform code: case-by-case.
