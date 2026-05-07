# Wiki Schema: Inter-Asia Pop

## Domain

This wiki covers Asian media and creative industries, with emphasis on regional and transnational circulation, flows, aesthetics, and cultural networks.

Scope includes:
- Film, television, music, animation, and visual media from Asia
- Regional production hubs and industries (Japan, South Korea, Hong Kong, Taiwan, China, Southeast Asia, South Asia, etc.)
- Transnational flows: circulation, adaptation, fandom, piracy, streaming
- Aesthetics and genres (City Pop, Wamono, Enka, K-pop, J-drama, anime, etc.)
- Artists, producers, directors, and creative practitioners
- Studios, labels, production companies, and distribution networks
- Technology platforms and infrastructure (streaming, social media, fan communities)
- Critical theory: soft power, cultural export, adjacency, regional adjacency
- Institutions, festivals, and market structures
- Fan cultures and user-generated content

## Conventions

- **File names:** lowercase, hyphens, no spaces (e.g., `city-pop.md`, `lee-ji-eun.md`)
- **Every wiki page** starts with YAML frontmatter (see Frontmatter section below)
- **Wikilinks:** Use `[[wikilinks]]` to connect pages. Minimum 2 outbound links per page.
- **When updating a page**, always bump the `updated` date.
- **Every new page** must be added to `index.md` under the correct section.
- **Every action** must be appended to `log.md`.
- **Provenance markers:** On pages synthesizing 3+ sources, append `^[raw/articles/source-file.md]` at the end of paragraphs whose claims come from a specific source.

## Frontmatter

```yaml
---
title: Page Title
created: YYYY-MM-DD
updated: YYYY-MM-DD
type: entity | concept | comparison | query | timeline | genre | movement | region
tags: [from taxonomy below]
sources: [raw/articles/source-name.md]
confidence: high | medium | low
contested: false
---
```

**Fields:**
- `title`: Page title
- `created`: Date the page was created (YYYY-MM-DD)
- `updated`: Date the page was last modified (YYYY-MM-DD)
- `type`: One of entity, concept, comparison, query, timeline, genre, movement, region
- `tags`: Array of tags from the taxonomy (see below)
- `sources`: Array of paths to raw files this page draws from
- `confidence`: high = well-supported across multiple sources; medium = single strong source or emerging consensus; low = opinion, speculative, or weakly supported
- `contested`: true if there are genuinely contradictory claims about this topic; false otherwise

## raw/ Frontmatter

Raw source files also get a small frontmatter block:

```yaml
---
source_url: https://example.com/article
ingested: YYYY-MM-DD
sha256: <hex digest of body only>
---
```

## Tag Taxonomy

Add new tags here BEFORE using them on pages.

**Regions & Countries:**
- japan
- south-korea
- hong-kong
- taiwan
- china
- mainland-china
- southeast-asia
- south-asia
- transnational
- diaspora
- east-asia

**Media & Genres:**
- film
- television
- music
- animation
- anime
- manga
- web-series
- documentary
- live-action
- drama
- comedy
- horror
- romance

**Music Genres & Aesthetics:**
- city-pop
- enka
- j-pop
- k-pop
- c-pop
- wamono
- folk
- experimental
- electronic
- hip-hop

**Industries & Infrastructure:**
- studio
- label
- production-company
- streaming-platform
- broadcaster
- distributor
- festival
- market

**Practitioners:**
- director
- composer
- musician
- actor
- producer
- screenwriter
- voice-actor
- animator
- designer

**Concepts & Theory:**
- soft-power
- cultural-export
- circulation
- adaptation
- localization
- fandom
- piracy
- adjacent
- regional-adjacency
- transnational
- diaspora-media
- postcolonial
- aesthetics
- network

**Meta:**
- comparison
- timeline
- movement
- genre
- controversy
- history

## Page Thresholds

- **Create a page** when an entity/concept/region appears in 2+ sources OR is central to one source
- **Add to existing page** when a source mentions something already covered
- **DON'T create a page** for passing mentions or minor details
- **Split a page** when it exceeds ~200 lines — break into sub-topics with cross-links
- **Archive a page** when its content is fully superseded — move to `_archive/`, remove from index

## Entity Pages (Artists, Studios, Platforms, Regions)

One page per notable entity. Include:
- Overview / what it is
- Key facts, dates, and history
- Notable works or achievements (if applicable)
- Regional/transnational connections ([[wikilinks]])
- Impact or influence
- Tags and sources

## Genre & Aesthetic Pages

One page per genre or aesthetic tradition. Include:
- Definition and characteristics
- Historical origins and development
- Key artists/creators
- Notable works and examples
- Regional variations or adaptations
- Cross-regional circulation
- Related genres ([[wikilinks]])
- Sources

## Region Pages

One page per region or country. Include:
- Overview of media/creative industries
- Key genres and aesthetics
- Major studios, labels, broadcasters
- Historical development
- Regional adjacencies and transnational connections ([[wikilinks]])
- Sources

## Comparison Pages

Side-by-side analyses. Include:
- What is being compared and why
- Dimensions of comparison (table format preferred)
- Verdict or synthesis
- Related entities/concepts ([[wikilinks]])
- Sources

## Timeline Pages

Chronological records of events, releases, or developments. Include:
- Entries in chronological order
- Key figures, works, or market events
- Links to relevant entity/genre/region pages
- Brief context for each entry

## Movement Pages

Characteristic entries:
- Definition and era
- Key figures and institutions
- Aesthetic or industry characteristics
- Representative works
- Transnational impact
- Related movements ([[wikilinks]])

## Update Policy

When new information conflicts with existing content:
1. Check the dates — newer sources generally supersede older ones
2. If genuinely contradictory, note both positions with dates and sources
3. Mark the contradiction in frontmatter: `contradictions: [page-name]`
4. Set `contested: true`
5. Flag for user review
