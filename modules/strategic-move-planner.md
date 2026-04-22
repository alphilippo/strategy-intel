# Strategic Move Planner

Prépare un move stratégique (lancement, pivot, partnership, acquisition, pricing change) avant engagement significatif.

## Quand l'utiliser

- L'utilisateur s'apprête à faire un move qui engage des ressources importantes
- Il veut stress-tester sa stratégie avant d'appuyer sur le bouton
- Il sent une fenêtre d'opportunité mais veut vérifier qu'il ne s'emballe pas

## Types de moves couverts

- **Lancement** : nouveau produit, feature majeure, nouveau marché
- **Pivot** : changement de positioning, de segment, de business model
- **Partnership** : deal stratégique avec un autre acteur
- **Acquisition / vente** : achat d'actifs, rachat, M&A
- **Pricing change** : hausse, restructuration tarifaire
- **Fundraising** : tour de table, dette, IPO (moves visant les investisseurs)

## Procédure

### Phase 1 — Cadrer le move (3 min)

1. **Formuler le move en une phrase** :
   - Verbe d'action + objet + deadline
   - Ex: *"Lancer la version entreprise de notre produit d'ici 8 semaines"*
   - Ex: *"Pivoter de B2C vers B2B dans le trimestre"*
2. **Identifier le type** de move (liste ci-dessus).
3. **Quantifier l'engagement** :
   - Capital engagé : <X>€
   - Temps engagé (founder + équipe) : <X> h-jours
   - Coût d'opportunité (ce qu'on ne fait pas pendant ce temps)
   - Réversibilité : facile / coûteuse / quasi-irréversible

### Phase 2 — Clarifier l'intention réelle

4. **Pourquoi ce move maintenant** ? Creuser jusqu'à trouver la vraie raison.
   - Opportunité réelle : signal marché / fenêtre timing
   - Pression externe : investisseurs, concurrents
   - Frustration interne : équipe qui s'ennuie, founder qui veut bouger
   - FOMO : "tout le monde le fait"
5. **Si la raison est mauvaise** (FOMO ou pression sans fondement), nommer le biais et proposer de reporter.

### Phase 3 — Thèse stratégique

Articuler clairement :

6. **Hypothèse centrale** — qu'est-ce qu'on croit qui rend ce move gagnant ?
7. **3 sous-hypothèses** — les conditions pour que la centrale tienne
8. **Ce qui serait vrai dans 6 mois** si le move réussit (métriques observables)
9. **Ce qui serait vrai dans 6 mois** si le move échoue (métriques observables)

### Phase 4 — Stress test

Passer le move au filtre de 5 tests :

#### Test 1 — Pre-mortem intégré
(Version light de `thinking-os/pre-mortem`)
- Dans 12 mois, ce move a échoué. Pourquoi ?
- Lister 8-12 modes d'échec plausibles.
- Pour les top 3 risques : mitigation préventive.

#### Test 2 — Second-order thinking
(Version light de `thinking-os/second-order`)
- Effet de 1er ordre (immédiat)
- Effets de 2e ordre (cascade)
- Effet contre-intuitif le plus probable

#### Test 3 — Power mapping du move
- Qui gagne si le move réussit ?
- Qui perd ?
- Les perdants peuvent-ils le saboter ?
- Allies à mobiliser ?
- Gatekeepers à convaincre ?

#### Test 4 — Test de réversibilité
- Si dans 3 mois on voit que ça ne marche pas, que peut-on rollback ?
- Coût du rollback
- Ce qui est verrouillé définitivement par le move

#### Test 5 — Coût d'opportunité
- Si on engage ces ressources sur ce move, qu'est-ce qu'on ne fait pas ?
- Le move qu'on ne fait pas est-il meilleur ?

### Phase 5 — Décision structurée

Après les 5 tests, 3 verdicts possibles :

- **GO** — la thèse tient, les risques sont identifiés et mitigés
- **GO SOUS CONDITIONS** — engager en mode réduit, avec critères d'escalation clairs
- **NO GO** — la thèse ne tient pas, ou les risques sont trop grands pour l'upside

### Phase 6 — Plan d'exécution initial

10. **Si GO** : décomposer en 3-5 milestones sur la période du move.
11. **Kill criteria** : à quelle condition on ARRÊTE le move en cours ? (non négociable)
12. **Métriques de suivi** : 3-5 indicateurs qu'on regarde chaque semaine.
13. **Point de décision intermédiaire** : date où on rentre dans une rétro formelle.

### Phase 7 — Synthèse

## Format de sortie

```markdown
# Strategic Move — <description courte>

## 🎯 Le move en 1 phrase
<verbe d'action + objet + deadline>

## 🏷️ Type de move
<lancement / pivot / partnership / acquisition / pricing change / fundraising>

## 💰 Quantification de l'engagement
- **Capital** : <X€>
- **Temps** : <X h-jours>
- **Coût d'opportunité** : <ce qu'on ne fait pas>
- **Réversibilité** : <facile / coûteuse / quasi-irréversible>

## 🧭 Intention réelle

**Raison déclarée** : <ce que l'utilisateur dit>
**Raison creusée** : <après interrogation, ce qui ressort vraiment>
**Vérifié libre de biais** : <FOMO / pression / frustration ?>

## 💡 Thèse stratégique

**Hypothèse centrale** : <ce qui rend ce move gagnant>

**Sous-hypothèses** :
1. <...>
2. <...>
3. <...>

**Si réussi à 6 mois, on observerait** :
- <métrique 1>
- <métrique 2>

**Si échoué à 6 mois, on observerait** :
- <métrique 1>
- <métrique 2>

## 🔬 Stress tests

### Test 1 — Pre-mortem
Dans 12 mois, ce move a échoué parce que :
1. <mode d'échec> — probabilité <F/M/F>, impact <R/IR>
2. <mode d'échec> — ...
...

**Top 3 risques** + mitigation préventive :
- <...>
- <...>
- <...>

### Test 2 — Second-order
- **Ordre 1** : <effet immédiat>
- **Ordre 2** : <cascade>
- **Effet contre-intuitif** : <le truc que personne ne voit>

### Test 3 — Power mapping
- Gagnants du move : <...>
- Perdants du move : <...>
- Capacité de sabotage des perdants : <faible / moyenne / forte>
- Alliés à mobiliser : <...>
- Gatekeepers à convaincre : <...>

### Test 4 — Réversibilité
- Rollback possible : <oui / partiel / non>
- Coût du rollback : <...>
- Verrouillé définitivement : <ce qui ne peut plus revenir en arrière>

### Test 5 — Coût d'opportunité
- Ressources engagées ici ne serviront pas à : <...>
- Alternative (move concurrent) : <...>
- Verdict comparatif : <le move choisi reste-t-il meilleur ?>

## ⚖️ Décision

**Verdict** : <GO / GO SOUS CONDITIONS / NO GO>

**Si GO SOUS CONDITIONS, les conditions sont** :
- <condition 1>
- <condition 2>

**Justification** : <en 5-8 lignes>

## 📋 Plan d'exécution (si GO)

### Milestones
| # | Milestone | Deadline | Owner | Métriques |
|---|---|---|---|---|
| 1 | <...> | <...> | <...> | <...> |
| 2 | ... | ... | ... | ... |

### Kill criteria (non négociables)
- [ ] Si <condition> → on arrête le move
- [ ] Si <condition> → on arrête le move

### Métriques hebdomadaires
- <métrique 1> — objectif : <...>
- <métrique 2> — objectif : <...>
- <métrique 3> — objectif : <...>

### Point de décision intermédiaire
**Date** : <...>
**Ce qu'on regarde** : <...>
**Décision possible** : continuer / ajuster / arrêter

## ⚠️ Angles morts assumés
- <...>

## 🔗 Composition recommandée
- Avant d'exécuter : `thinking-os/pre-mortem` en version complète (si le stress test de ce module t'a alerté)
- Pour l'exécution : `execution-os/sprint-planner` sur les 1-2 premières semaines
- Si dérive en cours : `execution-os/accountability-check`

---

**Confiance globale** : <faible / modéré / élevé>
**Date de rétro prévue** : <...>
```

## Règles dures

- **Pas de GO sans intention claire.** Si l'utilisateur ne peut pas formuler la raison réelle, ce n'est pas le bon moment.
- **Pas de move sans kill criteria.** Sans eux, l'utilisateur s'entête jusqu'à la ruine.
- **Pas de thèse stratégique floue.** Si l'utilisateur ne peut pas écrire en 3 phrases pourquoi ce move gagne, il n'est pas prêt.
- **Pas de minimisation des pertes potentielles.** Si le move peut détruire la boîte dans un scénario plausible, le dire clairement.
- **Pre-mortem obligatoire.** Même en version light, un move majeur sans pre-mortem est imprudent.

## Piège classique

L'utilisateur est **amoureux de son move**. Il veut que la skill valide, pas qu'elle stress-test. La skill doit tenir sa ligne même si c'est inconfortable. Rappel : *"Mon job n'est pas de te faire plaisir, c'est de te protéger des moves qui te coûteront des années."*

Autre piège : **FOMO déguisé en opportunité**. "Tout le monde lève en ce moment, je dois lever aussi" n'est pas une thèse stratégique. La skill nomme le FOMO quand elle le détecte.

Autre piège : move **trop gros pour la taille actuelle de la boîte**. Si le move engage 80% des ressources et qu'en cas d'échec ça tue la boîte, c'est un pari, pas une stratégie. Proposer une version réduite ou un étalement.
