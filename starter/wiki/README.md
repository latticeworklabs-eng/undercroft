# wiki/ — the LLM-owned layer

Everything in this folder is written and maintained by the LLM under the contract in the vault's `CLAUDE.md`. You read these pages (Obsidian's graph view and backlinks make this layer shine); you don't hand-edit them. If a page is wrong, tell the model — it fixes the page *and* whatever bookkeeping the fix touches.

Subfolders, created on first use:

| Folder | Contains |
|---|---|
| `sources/` | One page per ingested source — TL;DR, key claims, verbatim quotes, open questions. Date-prefixed: `2026-01-15-slug.md`. |
| `entities/` | People, organizations, products, places, things. One per page, accreting dated sections as new sources mention them. |
| `concepts/` | Ideas, frameworks, theories, topics. Same accretion rule. |

Every page carries YAML frontmatter and cites its sources with `[[wikilinks]]`. Pages that exist only as a mention start as stubs (`status: stub`) — deliberate gaps made visible.

The full kit adds `syntheses/` and `queries/` (populated by its QUERY and LINT operations) plus the rolling hot-cache file, worked examples, and the operations manual.
