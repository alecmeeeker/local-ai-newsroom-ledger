# The Commit & Ledger

**Live:** https://alecmeeeker.github.io/local-ai-newsroom-ledger/

An interactive visualization of daily lines-of-code growth across an AI tooling project I am building for small newsrooms.

## What this is

A single HTML page. No build step. No backend.

The chart traces the growth of a codebase that includes scrapers for regional news sources, a pgvector store that indexes the corpus, a multi-agent pipeline that triages stories and produces draft copy, an editor review UI for human approval, and a publish stack that posts to WordPress and Instagram.

Bushwick Daily uses parts of this toolkit for specific editorial workflows. The publication is not run by the code. The code is one of the tools the publication uses.

## The mission

To save local journalism by giving small newsrooms the tools they need to leverage their human editorial experience and local knowledge, so local reporting can be as fast, accurate, and deep as the work coming out of large nationally funded outlets.

Small newsrooms already have the editorial experience and the local knowledge. They do not always have the engineering. I am building these tools to close that gap.

## How the chart works

The numbers are real, not estimates.

The generator runs `git ls-tree` once per calendar day with a commit (127 days in the current dataset), collects the union of unique blob hashes (4,113 unique blobs), and reads each one through `git cat-file --batch` to count its lines exactly. Files are bucketed into nine subsystems (frontend, api, agents, scrapers, rag_core, migrations, infra, docs, other) by path. Milestones are auto-detected from feat-prefixed commits with a meaningful net diff.

End-to-end generation runs in about twenty seconds.

## Who built it

[**Alec Meeker**](https://alecmeeker.com), founder and editor-in-chief of Bushwick Daily. I built this with **Claude Code** as my dev partner along the way.

- Site: [alecmeeker.com](https://alecmeeker.com)
- GitHub: [@alecmeeeker](https://github.com/alecmeeeker)
- LinkedIn: [linkedin.com/in/alecmeeker](https://linkedin.com/in/alecmeeker)

## Regenerating the data

The `index.html` in this repo is a static snapshot. The generator script lives in the source repo. To rebuild from a fresh commit history:

```bash
python3 viz/git_loc_growth.py
```

## License

Visualization code: MIT. Underlying platform code: case-by-case as pieces are open-sourced.
