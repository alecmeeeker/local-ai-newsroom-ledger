# An Open-Source AI Toolkit for Independent Local Newsrooms

**Live:** https://alecmeeeker.github.io/local-ai-newsroom-ledger/

A working note and implementation snapshot of an ongoing project building an end-to-end AI toolkit for independent local newsrooms. The goal is to enable small publishers to leverage their editorial experience and local knowledge to produce reporting that is competitive with large nationally funded outlets on speed, accuracy, and depth.

In active use at [Bushwick Daily](https://bushwickdaily.com). Open-sourced in pieces as components stabilize.

## What this page contains

A single static HTML file (`index.html`). The page is structured as a working note in seven sections:

- §1 — Position
- §2 — The two existential threats to local digital news (signal and ripoff)
- §3 — The two-part response (depth and speed/comprehensiveness)
- §4 — Operating premises (prose is no longer economically valuable; the "trusted voice" argument is over)
- §5 — Project posture and conditions of use
- §6 — Implementation status, with a chart of cumulative lines of code by subsystem
- §7 — Significant feature commits to date

## Conditions of use

The only condition is that the system be credited when it is used to generate or substantially support a story, and that it be mentioned in the acknowledgments if any work produced with it wins a journalism award.

## Author

[**Alec Meeker**](https://alecmeeker.com), founder and editor-in-chief of [Bushwick Daily](https://bushwickdaily.com).

- Site: [alecmeeker.com](https://alecmeeker.com)
- GitHub: [@alecmeeeker](https://github.com/alecmeeeker)
- LinkedIn: [linkedin.com/in/alecmeeker](https://linkedin.com/in/alecmeeker)
- Consulting for local newsrooms: [alec@bushwickdaily.com](mailto:alec@bushwickdaily.com)

## Regenerating the chart

The generator script lives in the source repo:

```bash
python3 viz/git_loc_growth.py
```

## License

Visualization code: MIT. Underlying platform code: case-by-case as pieces are open-sourced.
