# Institutional Brain — Interactive Demo

A single-file, working static demo of the AI-Powered Institutional Brain — a memory layer for organizations that stores decisions, protocols, and outcomes as a linked knowledge graph, and cites its sources for every recommendation.

**Live demo:** https://gnarlyjock45.github.io/institutional-brain-demo/

## What's in the demo

Three interactive views over the same dataset:

- **Memory Graph** — force-directed graph of ~42 nodes (healthcare) or ~38 nodes (logistics), clustered by category. Hover for tooltips, click for a detail panel with linked memories.
- **Memory Bank** — card view of the same data with importance, category, expandable decision context, and full sources. Filterable, sortable, searchable.
- **Chat** — pre-populated exchanges showing answers with citations. Hover any "*X memories referenced*" footer to see the actual source cards; click *View →* to jump into the Bank.

A **Healthcare ↔ Logistics** toggle in the top bar swaps the underlying dataset to demonstrate that the architecture is sector-agnostic.

## Run it locally

It's a single HTML file. Either open `index.html` directly in a browser, or serve the folder:

```sh
python -m http.server 8765
# then visit http://localhost:8765/
```

## Stack

D3 v7 (graph), Tailwind play CDN (styling), Alpine.js (reactivity), Lucide (icons) — all loaded from CDN. No build step.

## Honesty note

The chat input is intentionally disabled — only the scripted exchanges run, and they cite the same memories shown in the Graph and Bank views. The displayed stats are hand-authored from the dataset, not computed from live activity.
