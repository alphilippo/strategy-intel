# Contributing to strategy-intel

Merci de vouloir contribuer. `strategy-intel` est une skill Claude open-source — les contributions bienvenues améliorent les modules existants ou ajoutent de nouveaux frameworks d'analyse stratégique rigoureux.

## Les 3 types de contributions bienvenues

### 1. Amélioration des modules existants

Signale avec un prompt + sortie obtenue + proposition si :
- Un module analyse sans forcer la question stratégique
- Un module produit des inférences non marquées
- Un module sort plus de 3 moves
- Un module oublie les angles morts

### 2. Nouveaux modules

Critères :
- **Unique** — pas de doublon avec les 4 existants
- **Actionable** — produit des moves, pas un rapport
- **Testable** — au moins 5 cas de test

Candidats bienvenus :
- **Jobs-to-be-Done Analyzer** (cadrage depuis l'angle client)
- **Scenario Planning** (3-5 futurs plausibles d'un marché)
- **Pricing Strategy Designer** (analyse et proposition de pricing)
- **Partnership Negotiator** (préparation de négociation spécifique)

### 3. Data / ressources

Références fiables de rapports de marché, bases de données concurrentielles, sources de dealflow africain / émergent — bienvenues en PR.

## Ce qu'on refuse

- Frameworks à la mode sans rigueur (genre "lean canvas" appliqué naïvement)
- SWOT sous toutes ses formes
- Motivation marketing ("c'est le moment d'attaquer !")
- Prédictions péremptoires

## Style

- Inférences toujours marquées
- Niveaux de confiance explicites
- Sources nommées précisément
- Moves actionables en 2 semaines

## Process

1. Fork
2. Branche `feat/<module>` ou `fix/<bug>`
3. Ajouter 3+ cas de test si nouveau module
4. PR avec description + exemple de sortie
