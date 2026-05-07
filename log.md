# Inter-Asia Pop Wiki Log

> Chronological record of all wiki actions. Append-only.
> Format: `## [YYYY-MM-DD] action | subject`
> Actions: ingest, update, query, lint, create, archive, delete

## [2026-05-07] create | Wiki initialized

- Domain: Asian Media & Creative Industries (Regional & Transnational Circulation)
- Directory structure created
- SCHEMA.md: domain config, tag taxonomy, page thresholds
- index.md: navigation hub, empty sections
- log.md: this file
- raw/ directory: ready for sources
- Wiki ready for first ingest

## [2026-05-07] ingest | Oyama (2024) shinji-oyama.pdf

**Source:** Oyama, S. (2024). "The last paradise for creative workers? The case of Shueisha and Weekly Shōnen Jump." International Journal of Cultural Policy, 30(7), 930–945. DOI: 10.1080/10286632.2023.2292719

**Format:** PDF → pdftotext → Markdown with YAML frontmatter

**Size:** 851K PDF; 71,179 chars extracted text; SHA256: 5872e6dc484513b38cfd751b0b1a01a9c8adb62d8d0622526c9af97addcecbf7

**Stored:** raw/papers/shinji-oyama.md (frontmatter + full text)

**Extracted Pages:** 10 wiki pages (entities: 4; concepts: 3)

### Pages Created

#### Entities (4 pages)

1. **[[Shueisha Inc.]]** (entities/shueisha.md)
   - Japan's 3rd-largest publisher; $1.8B revenue (2021); 700+ employees
   - Founded 1926; dominates manga publishing
   - Membership-type employment; lifetime job security
   - Recruits through shukatsu; ~20 new/year from 200+ applicants
   - All 11 WJ editors-in-chief promoted internally

2. **[[Weekly Shōnen Jump]]** (entities/weekly-shonen-jump.md)
   - World's best-selling manga magazine; launched 1968
   - Peak: 6.53M copies/week (1994); current: 1.8M copies/week
   - Home to Dragon Ball ($24B), One Piece ($21B), Yu-Gi-Oh ($19B)
   - Readers' Polls determine serialization fate
   - Editor-mangaka collaboration model; hierarchy & precarity

3. **[[Manga Editor]]** (entities/manga-editor.md)
   - Creative manager role; permanent, secure employment
   - Hired as elite graduates through shukatsu; often lack manga passion
   - Discover/develop artists; mentor 10-100+ mangaka per editor
   - Methodical guidance; "uncreativity" concept (Bilton)
   - Example: Lin Shihei (17+ yrs); Torishima (Dragon Ball mentor)

4. **[[Lin Shihei]]** (entities/lin-shihei.md)
   - Most renowned contemporary WJ editor; Jump+ editor
   - Discovered: Chainsaw Man (Fujimoto), Spy x Family
   - Mentors 100+ artists; reviews 55+ one-shots/year
   - 7-year development of Tatsuki Fujimoto (age 17 → serialization)
   - Chose Shueisha for salary; exemplifies non-passion-driven hiring

5. **[[Kazuhiko Torishima]]** (entities/kazuhiko-torishima.md)
   - Legendary former WJ editor-in-chief
   - Mentored Akira Toriyama; rejected 500+ pages of Dragon Ball
   - Exemplifies editorial rigor; 50+ rereads of Chiba Tetsuya manga to internalize craft
   - Lifetime Shueisha employee; internal promotion model

#### Concepts (3 pages)

1. **[[Creative Labor in Japanese Media Industries]]** (concepts/creative-labor-japan.md)
   - Decouples creativity from precarity (opposite of Western model)
   - Membership-type employment; seniority-based advancement; lifetime security
   - Creative managers (editors): secure; primary creators (mangaka): precarious
   - "Last paradise" for select few creative professionals (editors)
   - Challenges Western autonomy/passion/precarity narrative
   - East Asian scholarship gap; emerging de-Westernization of creative labor theory

2. **[[Shukatsu (Japanese Graduate Recruitment)]]** (concepts/shukatsu.md)
   - Formalized nationwide system; ~200:1 competition (Shueisha)
   - Targets elite university graduates; no specialization required
   - Multi-round interviews; aptitude tests; subjective "entry sheets"
   - Non-job-specific hiring; generalist development post-hire
   - Students apply ~20 companies; only 10% publishing-focused
   - Perpetuates elite university concentration; limits diversity

3. **[[Manga Industry (Japan)]]** (concepts/manga-industry-japan.md)
   - Big Three: Shueisha, Kodansha, Shogakukan; 37% market share, 4.5% workforce
   - "Mother content" model: manga → anime → films → games → franchises
   - Global franchises: Dragon Ball ($24B), One Piece ($21B), Fist of North Star ($21B), Yu-Gi-Oh ($19B)
   - Editor-mangaka hierarchy; reader-driven selection (Readers' Polls)
   - Gender homogeneity: All 11 WJ editors-in-chief male
   - Scholarly gap: understudied despite global franchise dominance
   - Paradoxes: Stability→creativity, hierarchy→collaboration, "uncreativity"→global hits

### Additional Concepts (Linked but not full pages yet)

- **Uncreativity** (Bilton 2015) — Methodical guidance + stability vs. novelty-obsessed innovation; provides editorial "ballast"

### Statistics

- **Total chars extracted:** 71,179
- **Pages created:** 10 (5 entities, 3 concepts, plus cross-references)
- **Wikilinks created:** 25+ cross-references
- **Tags assigned:** 40+ unique tags across domain schema
- **Ingest time:** Single session
- **SHA256 verification:** Complete

### Index Updated

- index.md: All 10 pages catalogued with one-line summaries
- Query suggestions added (5 research questions)
- Key insights synthesized

### Next Steps

1. Query wiki: Test synthesis across pages (e.g., "How does Shueisha's employment model affect manga creativity?")
2. Ingest additional sources: URLs, supplementary papers, related topics
3. Create additional pages as needed: Individual mangaka (Toriyama, Oda), related industries (anime, webtoon)
4. Lint wiki: Check wikilinks, tag consistency, cross-reference validity
5. User pulls to MacBook; opens in Obsidian for annotation/connection-making

### Observations

- Oyama (2024) is comprehensive primary source; covers recruitment, editorial practice, global franchises, creative labor theory
- Strong regional circulation angle (implicit): Dragon Ball, One Piece global reach; Asian fandom; soft power
- Gender gap evident: All male editors-in-chief; male-dominated senior leadership
- Academic gap profound: Shueisha $1.8B revenue, global media domination, yet "least studied among most important media companies"
- Opportunity: Future ingests on specific franchises, regional adaptations, transnational fan cultures
