# Foundry v2 — reference docs (NOT active for this vault)

This vault currently uses `SCHEMA.md` + flat-dir structure (entities/, concepts/, genres/, movements/, regions/, timelines/, comparisons/, queries/, raw/). That is still the active contract.

The files in this directory are reference-only:

- `MANIFEST.v2-reference.md` — the upgraded Foundry MANIFEST from the generative-art vault. Adds source tiering, conflict handling, freshness/re-ingest, pruning, voice anchor, query→concept promotion, sibling-vault linking, and an eval loop. Kept here so the ideas are visible without forcing a restructure. If we later migrate this vault to the Foundry pattern, this is the target.
- `eval.md` — domain-tailored evaluation questions for Inter-Asia Pop. Safe to use now against the existing vault structure — the questions don't care whether the underlying directories are called `wiki/` or live at the root.
- `eval-usage.md` — explains what the eval questions are for and how the `/foundry-eval` loop works.
- `CLAUDE.md` — older v1 copy of the Foundry MANIFEST, kept for historical reference. Superseded by `MANIFEST.v2-reference.md`.

## Status

- Active schema: `/root/interasia-pop/SCHEMA.md`
- Reference schema (not applied): `MANIFEST.v2-reference.md`
- Decision on migration: **deferred**

## If you decide to migrate

This vault already has 25+ pages, a 24KB log, and a populated index. Restructuring to `inbox/sources/wiki/` would require:

1. Moving `raw/` contents into `sources/` (and rewriting frontmatter to plain key-value format)
2. Moving `entities/concepts/genres/movements/regions/timelines/comparisons/` into `wiki/`
3. Moving `index.md`, `log.md` into `wiki/_meta/`
4. Rewriting every page's YAML frontmatter to the plain-key-value form (`Type: #type/concept` instead of `type: concept`)
5. Adding `Tier:` to every source, `Confidence:` to every concept
6. Updating every wikilink that used path prefixes

Non-trivial but mechanical. Worth doing only if you want the v2 features (conflict tracking, source tiering, eval loop) enough to justify the churn. You can adopt *just the eval loop* today without restructuring — that's what `eval.md` here enables.
