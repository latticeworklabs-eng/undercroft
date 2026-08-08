# raw/ — the human-owned layer

Drop source material here: articles saved as markdown, papers, transcripts, exported highlights, book chapters. This is the only layer you write to.

**Rules:**

- **Immutable once ingested.** The LLM reads files here but never edits them — and neither should you after ingest. If a source contains an error, the correction is filed on the source's wiki page (`wiki/sources/…`), never patched into the original. Provenance beats tidiness.
- **Naming:** kebab-case, descriptive: `how-to-do-great-work.md`, `attention-is-all-you-need.pdf`. The LLM handles date-prefixing on the wiki side.
- **Images** that belong to a source go in `raw/assets/`.
- URLs don't need a file — paste the link in chat and say "ingest this"; the model fetches it and records the URL in the source page's frontmatter.

To ingest: add the file, then tell the model **"ingest raw/your-file.md"**. It runs the full checklist in `CLAUDE.md` §3.1.
