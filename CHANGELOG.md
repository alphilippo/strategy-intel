# Changelog — strategy-intel

All notable changes to this project are documented here.

Format based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).
This project adheres to [Semantic Versioning](https://semver.org/).

## [1.0.0] — 2026-04-21

### Initial release

First public release of `strategy-intel` — a strategic analysis system skill for Claude with 4 modules.

### Added

#### Core routing system
- `SKILL.md` with module router and linguistic signature triggers
- Composition principle with the ecosystem (`thinking-os`, `execution-os`, `learning-os`)
- Guidance on data sources (general knowledge, web search, pasted content, user collection)

#### 4 strategic modules
- `competitor-teardown` — audit across 6 dimensions (value prop, pricing/model, distribution, product, team, trajectory), mini power mapping, differential analysis, 1-3 moves with confidence levels
- `market-mapping` — cartography across 7 actor categories (incumbents, challengers, niches, entrants, substitutes, adjacents, platforms), full power mapping (decision makers, gatekeepers, influencers, blockers, natural allies), 5 Forces adaptation, timing signals
- `opportunity-scanner` — 5 sources (client frustrations, under-served segments, out-of-product workflows, timing signals, unusual crossroads), quantitative scoring (problem reality, size, WTP, fit, timing, access), forced top 1 choice, 2-week invalidation tests
- `strategic-move-planner` — covers launches, pivots, partnerships, acquisitions, pricing changes, fundraising; 5 stress tests (pre-mortem, second-order, power mapping, reversibility, opportunity cost), GO / GO-UNDER-CONDITIONS / NO-GO verdict, kill criteria

#### Templates (reusable markdown)
- Competitor teardown template
- Market mapping template
- Opportunity scanner template
- Strategic move template

#### Documentation & validation
- 3 end-to-end examples (competitor teardown of YC Africa vs SIMBA, opportunity scan in West Africa fintech, exclusive partnership move stress test)
- 11 test cases with expected module routing + red flags
- Apache 2.0 license

### Design principles enforced
- No analysis without a strategic question
- Inferences marked explicitly (vs observations)
- No peremptory predictions (no "they'll fail in 6 months")
- Max 3 actionable moves per output
- Explicit confidence levels on every conclusion
- Blind spots acknowledged, verification list provided

### Known limitations in v1.0
- Trigger descriptions and module content are French-first
- English translation of module bodies on roadmap
- Deep research on opaque markets remains limited
- No persistent memory of competitive mapping between sessions

### Tested on
- Claude Opus 4.7
- Claude Sonnet 4.6

---

## [Unreleased]

### Planned for v1.1
- Jobs-to-be-Done module for customer-angle framing

### Planned for v1.2
- Scenario Planning module (3-5 plausible market futures)

### Planned for v2.0
- Persistent memory of competitive mapping between sessions
