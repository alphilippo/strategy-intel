# strategy-intel

![Version](https://img.shields.io/badge/version-1.0.0-blue) ![License](https://img.shields.io/badge/license-Apache%202.0-green) ![Claude](https://img.shields.io/badge/Claude-Skill-purple)

🌍 **Français** · **[English](README.en.md)**

> Système d'analyse stratégique pour Claude : 4 modules qui transforment l'information brute en moves actionables — pas en rapports.

## Ce que ça fait

La plupart des analyses stratégiques produites par l'IA sont des SWOT génériques qu'un étudiant MBA pondrait : vrais, plausibles, inutiles. Ce qui manque :

- Du **contexte spécifique** (pas "le marché du SaaS" mais TON marché)
- Du **power mapping** (qui décide, qui bloque, qui a des intérêts contraires)
- De l'**action** (1-3 moves dans les 2 semaines, pas un plan à 5 ans)
- De l'**honnêteté sur l'incertitude** (ce qu'on sait vs ce qu'on suppose)

`strategy-intel` applique 4 principes durs :

1. **Pas d'analyse sans question stratégique** — qu'est-ce que tu dois décider ?
2. **Pas de conclusion sans niveau de confiance** — 30 % ? 70 % ? 90 % ?
3. **Pas d'output sans moves actionables** — ce que tu fais cette semaine
4. **Pas d'analyse sans liste de ce qu'il reste à vérifier** — les angles morts assumés

## Les 4 modules

| Module | Quand l'utiliser |
|---|---|
| **Competitor Teardown** | Audit d'un concurrent précis (positioning, pricing, modèle, angles morts) |
| **Market Mapping** | Cartographie d'un marché + power mapping |
| **Opportunity Scanner** | Identification de gaps, niches, timing |
| **Strategic Move Planner** | Préparation d'un move avant engagement |

## Déclencheurs

- *"Analyse <concurrent>"* → Competitor Teardown
- *"Cartographie le marché X"*, *"rapports de force"* → Market Mapping
- *"Où sont les opportunités dans X"*, *"où frapper"* → Opportunity Scanner
- *"Je vais lancer/pivoter/signer un partnership"* → Strategic Move Planner

## Composition avec l'écosystème

- **Avant un move** : `strategy-intel/strategic-move-planner` → [`thinking-os/pre-mortem`](https://github.com/alphilippo/thinking-os) (version complète)
- **Si hors cercle de compétence** : `strategy-intel` → [`thinking-os/circle-of-competence`](https://github.com/alphilippo/thinking-os)
- **Move validé** : `strategy-intel` → [`execution-os/sprint-planner`](https://github.com/alphilippo/execution-os)
- **Si marché inconnu** : `strategy-intel/market-mapping` → [`learning-os/learning-path-planner`](https://github.com/alphilippo/learning-os)

## Installation

### Claude.ai

1. Télécharge le ZIP depuis GitHub ou clone le repo
2. Dans Claude.ai : Settings → Skills → "+" → "+ Create skill" → upload le ZIP
3. Toggle ON

### Claude Code

```bash
cp -r strategy-intel ~/.claude/skills/
```

## Exemples

### Audit concurrent
> *"Y Combinator lance un programme dédié Afrique. J'anime un programme similaire (SIMBA). Analyse-les."*

→ La skill force la question stratégique, liste les sources nécessaires, analyse sur 6 dimensions, fait le power mapping, propose 3 moves différenciés.

### Recherche d'opportunité
> *"Je connais la fintech Afrique de l'Ouest, où frapper ?"*

→ 5 sources scannées, scoring quantitatif, top 1 opportunité forcée, tests d'invalidation sur 2 semaines.

### Move stratégique tendu
> *"Un gros acteur me propose un partnership exclusif 3 ans contre 40 % du revenu. Je suis tenté mais je sens un piège."*

→ Stress test en 5 étapes (pre-mortem, second-order, power mapping, réversibilité, coût d'opportunité), verdict conditionnel, contre-proposition concrète.

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
├── templates/               # 4 templates markdown
├── examples/                # 3 exemples bout-en-bout
└── tests/test-cases.md      # 11 cas de validation
```

## Skills complémentaires (écosystème complet)

- 🧠 [**thinking-os**](https://github.com/alphilippo/thinking-os) — routeur cognitif
- ⚙️ [**execution-os**](https://github.com/alphilippo/execution-os) — système d'exécution
- 📚 [**learning-os**](https://github.com/alphilippo/learning-os) — système d'apprentissage
- ⚔️ [**strategy-intel**](https://github.com/alphilippo/strategy-intel) — analyse stratégique
- 🧭 [**alignment-os**](https://github.com/alphilippo/alignment-os) — alignement personnel

Les 5 répondent à des questions différentes :
- `thinking-os` — **QUOI** faire (cadre de pensée)
- `execution-os` — **COMMENT** le faire (cadence)
- `learning-os` — **APPRENDRE** à le faire (montée en compétence)
- `strategy-intel` — **OÙ & CONTRE QUI** le faire (positionnement)
- `alignment-os` — **POURQUOI** le faire (cohérence vie/valeurs)

## Limites

- Ne remplace pas du vrai terrain (interviews clients, entretiens concurrents)
- Les données disponibles via web search ne sont jamais exhaustives
- Les inférences peuvent être biaisées — toujours les marquer
- Sur les marchés très opaques (deep-tech, defense, private equity), la skill reste en surface

## Roadmap

- **v1.0** (actuel) : 4 modules + 4 templates + routage
- **v1.1** : Module **Jobs-to-be-Done** pour cadrer l'analyse depuis l'angle client
- **v1.2** : Module **Scenario Planning** (3-5 futurs plausibles d'un marché)
- **v2.0** : Mémoire de la cartographie concurrentielle entre sessions

## Licence

Apache 2.0 — fork, adapte, republie.

## Crédits

Conçu avec Claude comme Skill Architect. Inspiré par Michael Porter (5 Forces), W. Chan Kim (Blue Ocean), Clayton Christensen (Jobs-to-be-Done), Hamilton Helmer (7 Powers), et les traditions intelligence économique / stratégie militaire (power mapping, OODA).
