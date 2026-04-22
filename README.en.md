# strategy-intel

![Version](https://img.shields.io/badge/version-1.0.0-blue) ![License](https://img.shields.io/badge/license-Apache%202.0-green) ![Claude](https://img.shields.io/badge/Claude-Skill-purple)

🌍 **[Français](README.md)** · **English**

> A strategic analysis system for Claude: 4 modules that turn raw information into actionable moves — not reports.

## What it does

Most AI strategic analysis produces generic SWOT that any MBA student could write: accurate, plausible, useless. What's missing:

- **Specific context** (not "the SaaS market" but YOUR market)
- **Power mapping** (who decides, who blocks, who has conflicting interests)
- **Action** (1-3 moves in the next 2 weeks, not a 5-year plan)
- **Honesty about uncertainty** (what we know vs. what we assume)

`strategy-intel` applies 4 hard principles:

1. **No analysis without a strategic question** — what do you need to decide?
2. **No conclusion without a confidence level** — 30%? 70%? 90%?
3. **No output without actionable moves** — what you do this week
4. **No analysis without a list of what to verify** — acknowledged blind spots

## The 4 modules

| Module | When to use |
|---|---|
| **Competitor Teardown** | Audit of a specific competitor (positioning, pricing, model, blind spots) |
| **Market Mapping** | Market cartography + power mapping |
| **Opportunity Scanner** | Identify gaps, niches, timing |
| **Strategic Move Planner** | Prepare a move before committing |

## Triggers

- *"Analyze <competitor>"* → Competitor Teardown
- *"Map the X market"*, *"power dynamics"* → Market Mapping
- *"Where are the opportunities in X"*, *"where to strike"* → Opportunity Scanner
- *"I'm going to launch/pivot/sign a partnership"* → Strategic Move Planner

## Composition with the ecosystem

- **Before a move**: `strategy-intel/strategic-move-planner` → [`thinking-os/pre-mortem`](https://github.com/alphilippo/thinking-os) (full version)
- **If outside circle of competence**: `strategy-intel` → [`thinking-os/circle-of-competence`](https://github.com/alphilippo/thinking-os)
- **Validated move**: `strategy-intel` → [`execution-os/sprint-planner`](https://github.com/alphilippo/execution-os)
- **If market is unknown**: `strategy-intel/market-mapping` → [`learning-os/learning-path-planner`](https://github.com/alphilippo/learning-os)

## Installation

### Claude.ai

1. Download the ZIP from GitHub or clone the repo
2. In Claude.ai: Settings → Skills → "+" → "+ Create skill" → upload the ZIP
3. Toggle ON

### Claude Code

```bash
cp -r strategy-intel ~/.claude/skills/
```

## Examples

### Competitor audit
> *"Y Combinator is launching a program dedicated to Africa. I run a similar program (SIMBA). Analyze them."*

→ The skill forces the strategic question, lists required sources, analyzes across 6 dimensions, does power mapping, proposes 3 differentiated moves.

### Opportunity search
> *"I know West Africa fintech well, where should I strike?"*

→ 5 sources scanned, quantitative scoring, top 1 opportunity forced, invalidation tests over 2 weeks.

### Tense strategic move
> *"A big player is proposing a 3-year exclusive partnership for 40% of revenue. I'm tempted but I sense a trap."*

→ 5-step stress test (pre-mortem, second-order, power mapping, reversibility, opportunity cost), conditional verdict, concrete counter-proposal.

## Structure

```
strategy-intel/
├── SKILL.md
├── README.md + README.en.md
├── CHANGELOG.md
├── modules/
│   ├── competitor-teardown.md
│   ├── market-mapping.md
│   ├── opportunity-scanner.md
│   └── strategic-move-planner.md
├── templates/               # 4 markdown templates
├── examples/                # 3 end-to-end examples
└── tests/test-cases.md      # 11 validation cases
```

## Complementary skills (full ecosystem)

- 🧠 [**thinking-os**](https://github.com/alphilippo/thinking-os) — cognitive router
- ⚙️ [**execution-os**](https://github.com/alphilippo/execution-os) — execution system
- 📚 [**learning-os**](https://github.com/alphilippo/learning-os) — learning system
- ⚔️ **strategy-intel** — strategic analysis (this repo)

The 4 skills answer different questions:
- `thinking-os` — **WHAT** to do (thinking frame)
- `execution-os` — **HOW** to do it (cadence)
- `learning-os` — **HOW TO LEARN** it (skill building)
- `strategy-intel` — **WHERE & AGAINST WHOM** to do it (positioning)

## Limitations

- Doesn't replace real fieldwork (customer interviews, competitor meetings)
- Data available via web search is never exhaustive
- Inferences may be biased — always marked as such
- On very opaque markets (deep-tech, defense, private equity), the skill stays surface-level

> **Note**: Content in French (modules, templates, examples) is currently the reference version. English translation of module bodies is on the roadmap.

## Roadmap

- **v1.0** (current): 4 modules + 4 templates + routing
- **v1.1**: **Jobs-to-be-Done** module for customer-angle framing
- **v1.2**: **Scenario Planning** module (3-5 plausible market futures)
- **v2.0**: Persistent memory of competitive mapping between sessions

## License

Apache 2.0 — fork, adapt, republish.

## Credits

Built with Claude as Skill Architect. Inspired by Michael Porter (5 Forces), W. Chan Kim (Blue Ocean), Clayton Christensen (Jobs-to-be-Done), Hamilton Helmer (7 Powers), and the competitive intelligence / military strategy traditions (power mapping, OODA).
