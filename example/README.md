# Example — one real ingest, file by file

This folder is the vault contract (`CLAUDE.md` §3.1) executed once for real, against a public essay: Paul Graham's *How to Do Great Work* (2023). Every file is what the model produced, shown at its real vault path. Read it before your first ingest so you know what "done" looks like — and can push back when the model produces less.

**How the ingest started:** the operator saved the essay text to `raw/2026-05-04-how-to-do-great-work.md` and said *"ingest this."* (Pasting the URL works identically — the model fetches and reads it in full either way.) The raw file isn't reproduced here; the full essay lives at https://paulgraham.com/greatwork.html. Every quote in these pages was verified verbatim against the live essay when this example was built. The ingest date is illustrative.

## Reading order

| File | What it is |
|---|---|
| `wiki/sources/2026-05-04-how-to-do-great-work.md` | The source page — the hub: TL;DR, key claims, verbatim quotes, open questions |
| `wiki/entities/paul-graham.md` | Entity fan-out: the author, with a dated section citing the source |
| `wiki/concepts/curiosity-as-compass.md` | Concept fan-out: the essay's motivation thesis |
| `wiki/concepts/work-that-compounds.md` | Concept fan-out: the compounding thesis |
| `index-additions.md` | The exact lines added to `index.md`, and where they slot |
| `log-entry.md` | The exact entry appended to `log.md` |

## What to notice

- **Quotes are verbatim, with location.** When the model can't produce the exact words, it paraphrases *outside* quotation marks.
- **The source page is a hub.** It links out to every page it spawned; every fan-out page links back with a dated heading (`## From [[2026-05-04-how-to-do-great-work]]`), so each page carries its own provenance trail.
- **"Updated: (none)" in the log is honest, not lazy.** A cold-start ingest has nothing to cross-reference yet. Links are made when real, never to hit a quota.
- **Open questions become the reading queue.** The source page queues a counter-source on problem selection — the vault deciding what it wants to read next.

This is a single cold-start ingest: one source page, three fan-out pages. In a live vault with a dense graph, a typical ingest touches 5–15 pages. The full kit (Undercroft Core) continues this exact vault for two more ingests, where the compounding shows up — cross-source appends under dated headings, a flagged contradiction, and a live schema change.
