# Prose Is Dead. Local News Isn't.

**The future infrastructure of local news.**

**Live:** https://alecmeeeker.github.io/local-ai-newsroom-ledger/

A position paper and implementation snapshot for an open-source AI infrastructure built to give independent local newsrooms what they need to survive. In active use at [Bushwick Daily](https://bushwickdaily.com) and being open-sourced in pieces as components stabilize.

The argument, in brief: the prose-based local-newsroom model is finished, two AI-driven forces (slop noise and instant content laundering) are accelerating the decline, and the only durable response is fast, systems-based, data-driven investigative reporting on subjects neither viral video nor sponsored influencers will pursue.

## Sections

- §1 — Thesis
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
