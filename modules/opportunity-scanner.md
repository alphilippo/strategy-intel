# Opportunity Scanner

Identifie des gaps exploitables, des niches sous-servies, et des signaux de timing.

## Quand l'utiliser

- L'utilisateur cherche **où frapper** — un angle pour lancer, pivoter, ou étendre
- Il a identifié un marché mais pas son positionnement précis
- Il soupçonne qu'il y a une niche que personne ne sert bien
- Il a des signaux faibles et veut les transformer en hypothèse stratégique

## Philosophie

Une "opportunité" n'existe pas dans l'absolu. Une opportunité, c'est :
- **Un problème réel** (pas supposé)
- **Vécu par un segment identifiable** (pas "tout le monde")
- **Mal résolu par les solutions actuelles** (gap observable)
- **Avec un timing qui devient favorable** (tech, régulation, comportement)
- **Accessible depuis nos forces** (pas n'importe quelle opportunité — la bonne pour NOUS)

Sans les 5 conditions, ce n'est pas une opportunité — c'est un fantasme.

## Procédure

### Phase 1 — Cadrer le périmètre (3 min)

1. **Marché / espace** : où on cherche ? (déjà cadré si `market-mapping` fait avant)
2. **Contraintes de l'utilisateur** : compétences, capital, temps, réseau disponibles
3. **Horizon** : 6 mois ? 2 ans ? 5 ans ?
4. **Question centrale** : *"Quelle est l'opportunité la plus prometteuse pour MOI dans ce marché ?"*

### Phase 2 — Les 5 sources d'opportunités

Pour chaque source, creuser :

#### Source 1 — Frustrations clients observables
5. Où les clients se plaignent publiquement ?
   - Reviews négatives des leaders (G2, Capterra, Amazon, App Store)
   - Threads Reddit / Twitter / LinkedIn
   - Tickets support publics
6. **Pattern à chercher** : plaintes **récurrentes** sur un même sujet chez **plusieurs leaders**.

#### Source 2 — Segments mal servis
7. Qui les leaders ne veulent pas servir ?
   - Trop petits (PME, freelances)
   - Trop spécifiques (secteurs de niche)
   - Trop "difficiles" (régulation, complexité)
   - Trop nouveaux (usages émergents)
8. **Règle** : si un leader dit *"on ne fait pas ça"*, c'est souvent une opportunité.

#### Source 3 — Workflows en-dehors du produit
9. Que font les clients **avant** et **après** utiliser les solutions actuelles ?
10. Quels **workarounds manuels** existent ?
11. Quels **outils en parallèle** sont bricolés (tableurs, Notion, Zapier) pour compenser ?

#### Source 4 — Signaux de timing
12. Qu'est-ce qui a **changé récemment** (6-18 mois) qui rend possible une solution qui ne l'était pas avant ?
    - Technologie (ex: LLM, tokenization, edge computing)
    - Régulation (ex: RGPD, DMA, nouvelles normes sectorielles)
    - Comportement (remote work, mobile-first, AI-native)
    - Économie (récession force des trade-offs différents)

#### Source 5 — Croisements inhabituels
13. Quels **croisements de domaines** sont encore inexplorés ?
    - IA × secteur X
    - Communauté × workflow Y
    - Open-source × marché Z
14. Pas pour la mode — parce que le croisement résout un problème réel.

### Phase 3 — Scoring des opportunités candidates

Pour chaque opportunité candidate, noter de 1 à 5 :

| Critère | Poids | Définition |
|---|---|---|
| **Réalité du problème** | 3x | Y a-t-il une vraie douleur (pas supposée) ? Preuves tangibles ? |
| **Taille du segment** | 2x | Combien de personnes / boîtes ont ce problème ? |
| **Willingness to pay** | 2x | Paieraient-ils pour une solution ? Combien ? |
| **Fit avec nos forces** | 3x | Sommes-nous bien placés pour gagner ici ? |
| **Timing** | 2x | Est-ce maintenant ou encore trop tôt / déjà trop tard ? |
| **Accessibilité** | 1x | Peut-on atteindre ce segment avec nos moyens ? |

**Score = Σ (note × poids)**

Top 3 opportunités → phase suivante.

### Phase 4 — Tester chaque opportunité

Pour les top 3, répondre :

1. **Qui est le client précis** (pas "les PME" — **quel profil exact**) ?
2. **Quel est le problème exact** en une phrase factuelle ?
3. **Comment le résolvent-ils aujourd'hui** ?
4. **Pourquoi c'est mal résolu** ?
5. **Qu'est-ce qui rend viable de mieux résoudre maintenant** ?
6. **Pourquoi NOUS** plutôt qu'un autre pour le faire ?

Si une opportunité ne passe pas 6/6, elle descend dans le ranking.

### Phase 5 — Test d'invalidation rapide

Pour chaque top opportunité :

- **Que faudrait-il observer** dans les 2 semaines qui **invaliderait** cette opportunité ?
- **Que faudrait-il observer** qui la **validerait** fortement ?

Sans ces deux tests, l'opportunité reste spéculative.

### Phase 6 — Synthèse action

**Top 1 opportunité** (pas top 3 — forcer le choix) + 1-3 moves de validation dans les 2 semaines.

## Format de sortie

```markdown
# Opportunity Scanner — <marché / espace>

## 🎯 Question centrale
<ce que l'utilisateur cherche>

## 📋 Contraintes de l'utilisateur
- Compétences disponibles : <...>
- Capital disponible : <...>
- Temps disponible : <...>
- Horizon : <...>

## 🔍 Scanning — 5 sources

### 1. Frustrations clients observables
<pattern principaux repérés + sources>

### 2. Segments mal servis
<qui les leaders ignorent>

### 3. Workflows hors-produit
<workarounds et bricolages repérés>

### 4. Signaux de timing
<ce qui a changé et débloque>

### 5. Croisements inhabituels
<intersections peu explorées>

## 📊 Opportunités candidates + scoring

| # | Opportunité (1 phrase) | Réalité problème (×3) | Taille (×2) | WTP (×2) | Fit (×3) | Timing (×2) | Accès (×1) | Score |
|---|---|---|---|---|---|---|---|---|
| 1 | <...> | N | N | N | N | N | N | TOTAL |
| 2 | <...> | ... | ... | ... | ... | ... | ... | ... |
| 3 | <...> | ... | ... | ... | ... | ... | ... | ... |

## 🏆 Top 1 opportunité retenue

### <Nom court de l'opportunité>

**Client précis** : <profil exact, pas générique>

**Problème exact** : <phrase factuelle, chiffrée si possible>

**Résolution actuelle** : <comment ils se débrouillent aujourd'hui>

**Pourquoi mal résolu** : <gap précis dans les solutions existantes>

**Ce qui rend viable maintenant** : <signal de timing précis>

**Pourquoi nous** : <fit avec les forces de l'utilisateur>

## ⚖️ Test d'invalidation rapide

**Signal qui invaliderait cette opportunité dans 2 semaines** :
- <observation qui ferait abandonner>

**Signal qui la validerait fortement** :
- <observation qui ferait accélérer>

## ✅ Moves actionables (2 semaines)

1. **<action de validation>** — confiance : <...>
   - Ce qu'on apprend : <...>
2. **<action de validation>** — confiance : <...>
3. **<action de validation>** — confiance : <...>

## ⚠️ Angles morts assumés
- <...>
- <...>

## 🔬 À creuser
- [ ] <...>
- [ ] <...>

---

**Confiance globale** : <faible / modéré / élevé>
```

## Règles dures

- **Pas d'opportunité sans client précis.** *"Les PME"* ne compte pas. *"Les DRH d'ETI industrielles de 500-2000 salariés en France"* compte.
- **Pas de "problème" sans preuve.** Si l'utilisateur n'a parlé à personne de son segment cible, l'opportunité reste hypothétique.
- **Pas plus d'UNE opportunité retenue.** Forcer le choix, sinon l'utilisateur ne fait rien.
- **Tests d'invalidation obligatoires.** Sans eux, l'opportunité est non-falsifiable = inutile.
- **Pas de "grande idée" sans fit.** Une opportunité parfaite pour quelqu'un d'autre n'est pas une opportunité pour toi.

## Piège classique

L'utilisateur tombe amoureux d'une opportunité séduisante mais loin de ses forces. La skill doit le confronter : *"Pourquoi TOI plutôt qu'un autre ?"* Si la réponse est *"j'ai une intuition"*, c'est insuffisant.

Autre piège : confondre **tendance** et **opportunité**. "L'IA est en train de tout changer" n'est pas une opportunité. "Les avocats en cabinet individuel passent 6h/semaine à faire de la recherche documentaire et il existe des LLMs spécialisés depuis 18 mois" en est une.
