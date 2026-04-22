---
name: strategy-intel
description: Système d'analyse stratégique avec 4 modules — competitor teardown (audit d'un concurrent précis), market mapping (cartographie d'un marché + power mapping), opportunity scanner (gaps, niches, timing), strategic move planner (préparation d'un lancement/partnership/pivot). Utilise cette skill dès que l'utilisateur dit "analyse ce concurrent", "audit concurrentiel", "comprendre le marché X", "cartographie du secteur", "où sont les opportunités dans X", "où frapper", "je vais lancer/pivoter/signer un partnership", "prépare mon move", "power mapping de Y", "qui décide dans ce secteur", "je veux comprendre les rapports de force". Se déclenche aussi quand l'utilisateur colle un article, un post LinkedIn, une landing page concurrent, un rapport de marché pour analyse. Chaque output inclut 1-3 moves actionables dans les 2 semaines, un niveau de confiance explicite, et les données à collecter pour affiner. Pas de SWOT naïf, pas de rapport stérile — uniquement de l'analyse orientée action.
---

# strategy-intel

Un système d'analyse stratégique qui transforme l'information brute en **moves actionables** — pas en rapports.

## Philosophie

La plupart des analyses stratégiques produites par l'IA sont des **SWOT génériques** qu'un étudiant de MBA pourrait pondre : vrais, plausibles, inutiles. Ce qui manque :

1. **Du contexte spécifique** — pas "le marché du SaaS", mais TON marché
2. **Du power mapping** — qui décide, qui bloque, qui a des intérêts contraires
3. **De l'action** — 1-3 moves dans les 2 semaines, pas un plan à 5 ans
4. **De l'honnêteté sur l'incertitude** — ce qu'on sait vs ce qu'on suppose

`strategy-intel` applique 4 principes durs :

1. **Pas d'analyse sans question stratégique** — qu'est-ce que tu dois décider ?
2. **Pas de conclusion sans niveau de confiance** — 30% ? 70% ? 90% ?
3. **Pas d'output sans moves actionables** — ce que tu fais cette semaine
4. **Pas d'analyse sans liste de ce qu'il reste à vérifier** — les angles morts assumés

## Les 4 modules

| Module | Rôle | Quand l'appeler |
|---|---|---|
| **Competitor Teardown** | Audit approfondi d'un concurrent précis (positioning, pricing, modèle, angles morts) | Tu veux comprendre un concurrent nommé |
| **Market Mapping** | Cartographie d'un marché (acteurs, forces, dynamiques) + power mapping | Tu entres dans un marché ou tu y navigues |
| **Opportunity Scanner** | Identification de gaps, niches, signaux de timing | Tu cherches où frapper |
| **Strategic Move Planner** | Préparation d'un move (lancement, pivot, partnership) | Tu vas engager des ressources significatives |

## Routage par signature

| Signature linguistique | Module |
|---|---|
| *"Analyse <nom de concurrent>"*, *"audit de <entreprise>"*, *"décortique leur offre"*, *"leur pricing"* | `competitor-teardown` |
| *"Cartographie le marché X"*, *"comprendre le secteur"*, *"qui décide dans ce marché"*, *"rapports de force"* | `market-mapping` |
| *"Où sont les opportunités dans X"*, *"quel gap exploiter"*, *"quelle niche"*, *"timing de lancement"* | `opportunity-scanner` |
| *"Je vais lancer X"*, *"je prépare un pivot"*, *"on va signer ce partnership"*, *"préparer mon move"* | `strategic-move-planner` |

### Détection implicite

Si l'utilisateur :
- **Colle du contenu brut** (article, post LinkedIn, landing page) → d'abord identifier l'intention : audit d'un concurrent ? Compréhension de marché ? Puis charger le bon module.
- Parle d'un **concurrent précis sans demander explicitement d'analyse** → proposer un `competitor-teardown`
- Décrit une **situation où plusieurs acteurs sont en jeu** → suggérer `market-mapping` avec power mapping

## Composition avec l'écosystème

- `strategy-intel` × [`thinking-os`](https://github.com/alphilippo/thinking-os) :
  - Un move identifié passe par `second-order` (effets en cascade) avant engagement
  - Un move engageant passe par `pre-mortem` (modes d'échec) avant lancement
  - Si hors cercle de compétence → `circle-of-competence` avant de décider
- `strategy-intel` × [`execution-os`](https://github.com/alphilippo/execution-os) :
  - Un move validé devient un sprint via `sprint-planner`
- `strategy-intel` × [`learning-os`](https://github.com/alphilippo/learning-os) :
  - Si un marché est trop inconnu, `learning-os/learning-path-planner` construit une montée en compétence avant l'analyse

## Données d'entrée

La skill peut analyser à partir de :

1. **Connaissance générale** (ce que Claude sait déjà)
2. **Web search** (si l'outil est disponible dans la session)
3. **Contenu collé** par l'utilisateur (articles, posts, landing pages, extraits d'études, exports LinkedIn)
4. **Recherche guidée** (la skill dit à l'utilisateur quelles données collecter et où)

**Règle** : si la skill n'a pas accès à assez de données, elle ne produit pas une analyse creuse — elle liste explicitement ce qu'il manque et comment l'obtenir.

## Procédure d'application

1. **Identifier** le module via la table de routage
2. **Demander la question stratégique** : *"Qu'est-ce que tu dois décider ou préparer avec cette analyse ?"*
3. **Charger** `modules/<module>.md`
4. **Collecter ou recevoir** les données
5. **Appliquer** rigoureusement la procédure
6. **Produire** la sortie avec : analyse + niveau de confiance + 1-3 moves actionables + liste de ce qu'il faut vérifier

## Format de sortie standard

Chaque module a son format, mais tous incluent :

- 🎯 **Question stratégique** à laquelle l'analyse répond
- 📊 **Analyse** (variable selon module)
- 📈 **Niveau de confiance** (faible / modéré / élevé + justification)
- ✅ **Moves actionables** : 1-3 actions dans les 2 prochaines semaines
- ⚠️ **Angles morts** : ce qu'on ne sait pas
- 🔬 **À vérifier** : données à collecter pour affiner

## Règles et limites

- **Pas de "je ne sais pas" dissimulé.** Si la skill manque d'info, elle le dit clairement — pas d'analyse fabriquée.
- **Pas de recommandation d'action sans validation par l'utilisateur.** La skill propose, ne décide pas.
- **Pas de jugement moral gratuit sur les concurrents.** L'analyse est factuelle — "ce concurrent utilise une stratégie X" n'est pas "ce concurrent est mauvais".
- **Respect de la confidentialité.** Si l'utilisateur donne des infos sensibles (chiffres internes, NDA), la skill ne les fait pas sortir du contexte de la conversation.
- **Pas d'illusion d'exhaustivité.** Une analyse complète sur un marché mondial demande des mois. La skill fait de l'analyse **ciblée** et le dit.

## Ressources associées

- `modules/` — 4 modules chargés à la demande
- `templates/` — templates markdown pour les outputs
- `examples/` — 3 exemples bout-en-bout
- `tests/test-cases.md` — 11 cas de validation

## Workflow type

```
1. "Un concurrent vient d'annoncer une feature" → competitor-teardown (audit)
2. Teardown révèle qu'on n'est pas sur le même créneau → confirmation positionnement
3. "Où frapper pour se différencier" → opportunity-scanner
4. Opportunity identifiée → strategic-move-planner
5. Move planifié → pre-mortem (thinking-os) avant engagement
6. Move validé → sprint (execution-os/sprint-planner)
```

Cette cadence est une suggestion — chaque utilisateur a son tempo.
