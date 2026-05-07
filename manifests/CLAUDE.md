# Instructions for Claude (and other agents)

You are operating inside the **Inter-Asia Pop wiki**, a knowledge vault about Asian media and creative industries — regional and transnational flows, aesthetics, industries, and cultural networks.

## Vault state — read this carefully

This vault is in a **hybrid state**:

- **Active contract:** `SCHEMA.md` at the root. YAML frontmatter. Flat-dir structure (`entities/`, `concepts/`, `genres/`, `movements/`, `regions/`, `timelines/`, `comparisons/`, `queries/`, `raw/`). `index.md` and `log.md` live at the root, not under `wiki/_meta/`.
- **Reference (not yet applied):** `manifests/MANIFEST.v2-reference.md` — the upgraded Foundry pattern used in sibling vaults (generative-art). Deferred pending a migration decision.
- **Active regardless of structure:** `manifests/eval.md` — evaluation questions that work against the current flat-dir layout.

**Do not restructure the vault.** `SCHEMA.md` is authoritative for directory layout and frontmatter. If the user explicitly asks you to migrate to the v2 structure, see `manifests/README.md` for the migration checklist — and confirm before moving a single file.

## Read these first, in this order

1. **`SCHEMA.md`** (root) — authoritative governance doc for this vault's current structure. Domain scope, frontmatter format, tag taxonomy, page thresholds, update policy.
2. **`index.md`** (root) — catalog of all pages. Read this before answering any query or deciding whether a new page is needed.
3. **`log.md`** (root) — chronological record. Read the last 20-30 entries to understand recent ingests.
4. **`manifests/eval.md`** — 12 stable evaluation questions. Don't answer them unless explicitly running an eval pass.
5. **`manifests/eval-usage.md`** — explains the eval loop.
6. **`manifests/MANIFEST.v2-reference.md`** — the v2 pattern. Reference only; use for ideas to borrow piecemeal (see below).

## Ideas to borrow from v2 without restructuring

The user has approved these as safe adoptions against the current SCHEMA.md structure:

- **Source tiering.** Add a `tier:` field to new raw source frontmatter, picking one of: `peer-reviewed`, `primary`, `journalism`, `secondary`, `informal`. Don't backfill old sources unless asked.
- **Contested concepts.** When two sources genuinely disagree, set `contested: true` (already in SCHEMA.md) and add a `Disagreements` section to the concept body quoting each side with attribution. Never silently pick a winner.
- **Confidence signals.** Use the `confidence: high|medium|low` field from SCHEMA.md seriously. `high` requires 2+ sources with at least one non-informal tier.
- **Eval runs.** When the user asks to "run eval" or "evaluate the vault," work through `manifests/eval.md` and rate each answer `strong`/`thin`/`missing` against the current wiki. Feed thin/missing findings into `index.md` Open Questions.

## Ideas to NOT adopt yet

Until the user explicitly approves a migration:

- Don't create `inbox/`, `sources/`, `wiki/`, `wiki/_meta/`, or `wiki/_archive/` directories.
- Don't change YAML frontmatter to the plain-key-value format (`Type: #type/concept`). Current YAML (`type: concept`) is correct.
- Don't introduce `Superseded by:` or `Last verified:` fields yet — they won't round-trip with the existing tooling.

## Hard rules

- **Never delete pages.** If a page is fully superseded, note it in log.md and flag for user review. Archival mechanics aren't defined yet in SCHEMA.md.
- **Never silently resolve contradictions.** Use `contested: true` and a `Disagreements` section.
- **Never create a page from a passing mention.** 2+ sources OR central to one source — SCHEMA.md is explicit.
- **Never break a wikilink.** If renaming, update every backlink.
- **Every new page must appear in `index.md` and `log.md`.**

## Sibling vaults

- `generative-art` — fully v2. Cross-link with `[[generative-art/wiki/Concept Title]]` if a concept here informs or is informed by one there. Read-only from this vault's perspective.
- `tiwchh` — internet/web history, same hybrid state as this vault.

## If you're unsure

Ask the user before doing anything destructive or structural. SCHEMA.md is the source of truth for this vault; `manifests/` is reference and tooling.
