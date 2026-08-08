# Log

Append-only chronological record of every operation on this vault. The LLM appends one entry per ingest; past entries are never edited.

Entry prefix convention: `## [YYYY-MM-DD] <op> | <short title>` — grep-parseable, so `grep "^## \[" log.md | tail -5` returns the last five entries.

Example entry shape:

```markdown
## [2026-01-15] ingest | How to Do Great Work (Paul Graham)
- Created: [[2026-01-15-how-to-do-great-work]], [[paul-graham]]
- Updated: [[first-principles-thinking]]
- Contradictions: (if any)
- Follow-ups: (1–3 suggested next moves)
```

---
