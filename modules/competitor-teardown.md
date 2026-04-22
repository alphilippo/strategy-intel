# Competitor Teardown

Audit approfondi d'un concurrent précis, orienté vers les décisions que l'utilisateur doit prendre.

## Quand l'utiliser

- L'utilisateur nomme un concurrent et veut comprendre son positioning
- Un concurrent vient d'annoncer une feature ou un pivot
- Avant de lancer quelque chose, vérifier la concurrence directe
- Pour benchmarker ses propres choix (pricing, positioning)

## Procédure

### Phase 1 — Cadrer la question stratégique (3 min)

1. **Demander** : *"Qu'est-ce que tu dois décider ou préparer suite à cette analyse ?"*
2. Exemples de bonnes questions :
   - *"Dois-je lancer la même feature qu'eux ou me différencier ?"*
   - *"Leur pricing est-il soutenable ? Dois-je m'aligner ?"*
   - *"Est-ce qu'ils pivotent sur mon territoire ?"*
3. Si pas de question → l'analyse sera trop large. Forcer une formulation.

### Phase 2 — Identifier les données nécessaires

4. **Liste minimum à collecter** :
   - Landing page(s) principales
   - Pricing page (ou absence = signal)
   - 3-5 posts récents sur leurs canaux
   - Reviews clients (G2, Capterra, Trustpilot, Amazon selon secteur)
   - Équipe clé (LinkedIn : dirigeants, recrutements récents)
   - Financement (Crunchbase, DealRoom, presse)
5. **Si l'utilisateur a accès à web search** : demander à Claude de chercher.
6. **Si l'utilisateur a collé du contenu** : analyser ce qui est là, nommer ce qui manque.
7. **Si rien n'est disponible** : proposer une liste de choses à collecter et reporter l'analyse.

### Phase 3 — Analyse en 6 dimensions

Pour chaque dimension, noter :
- **Ce qu'on observe** (factuel)
- **Ce qu'on infère** (inférence explicite, marquée comme telle)
- **Ce qu'on ne sait pas** (angle mort assumé)

#### 1. Proposition de valeur
- Promesse centrale en 1 phrase
- Public cible (à qui ils parlent)
- Promesse différenciante vs alternatives

#### 2. Pricing & modèle économique
- Structure de prix (abonnement, usage, one-shot, freemium)
- Tiers et leurs différenciateurs
- Signaux sur la marge (gratuit trop généreux = brûle du cash ?)
- Upsell / expansion implicite

#### 3. Distribution & acquisition
- Canaux principaux (SEO, paid, outbound, partnerships, community)
- Signaux sur le CAC (investissement marketing visible)
- Partenariats / intégrations nommées

#### 4. Produit & expérience
- Features headline
- UX / onboarding (si accessible)
- Gaps repérés dans les reviews clients

#### 5. Équipe & culture
- Fondateurs : profils, parcours, crédibilité domaine
- Recrutements récents (signal sur la direction)
- Rotation : départs clés récents (signal négatif ou renouvellement)

#### 6. Trajectoire & signaux faibles
- Levées de fonds récentes (montant, investisseurs, tour)
- Mentions presse
- Changement de narratif depuis 6-12 mois
- Moves récents (feature, pivot, partnership)

### Phase 4 — Power mapping mini

7. **Qui a le pouvoir** dans leur écosystème ?
   - Fondateurs / CEO
   - Investisseurs principaux
   - Clients clés (si B2B concentré)
   - Partenaires stratégiques
8. **Qui pourrait les bloquer** ?
9. **Qui pourrait leur succéder / les menacer** ?

### Phase 5 — Analyse différentielle

10. **Comparer à l'utilisateur** (si contexte fourni) :
    - Où sont-ils supérieurs ?
    - Où sont-ils vulnérables ?
    - Où ne se croise-t-on pas (créneau différent) ?
11. **Identifier les angles d'attaque ou de différenciation** possibles.

### Phase 6 — Synthèse action

12. **1-3 moves actionables** dans les 2 semaines, pas 10 recommandations.
13. **Niveau de confiance** sur chaque move (faible / modéré / élevé).
14. **Liste de vérifications** pour affiner l'analyse.

## Format de sortie

```markdown
# Competitor Teardown — <nom concurrent>

## 🎯 Question stratégique
<ce que l'utilisateur doit décider>

## 📊 Données analysées

| Source | Ce qu'on y trouve |
|---|---|
| <URL / document> | <synthèse> |
| ... | ... |

**Sources manquantes** : <ce qu'il faudrait idéalement>

## 🔍 Analyse en 6 dimensions

### 1. Proposition de valeur
- **Promesse centrale** : "<...>"
- **Public cible** : <...>
- **Différenciation claimée** : <...>
- **Inférence** : <...>
- **Angle mort** : <...>

### 2. Pricing & modèle économique
<même structure>

### 3. Distribution & acquisition
<...>

### 4. Produit & expérience
<...>

### 5. Équipe & culture
<...>

### 6. Trajectoire & signaux faibles
<...>

## 🏛️ Power mapping

- **Qui a le pouvoir** : <fondateurs / investisseurs / clients clés>
- **Qui pourrait les bloquer** : <...>
- **Menaces émergentes** : <...>

## 🔀 Analyse différentielle vs <utilisateur>

| Dimension | Eux | Nous | Qui gagne ? |
|---|---|---|---|
| ... | ... | ... | ... |

**Angles d'attaque possibles** : <liste>
**Angles de différenciation** : <liste>
**Non-croisement** : <où on ne se bat pas>

## ✅ Moves actionables (2 semaines)

1. **<action précise>** — niveau de confiance : <faible/modéré/élevé>
   - Pourquoi : <...>
2. **<action précise>** — confiance : <...>
3. **<action précise>** — confiance : <...>

## ⚠️ Angles morts assumés

Ce que cette analyse ne couvre pas :
- <...>
- <...>

## 🔬 À vérifier pour affiner

- [ ] <info à collecter>
- [ ] <info à collecter>
- [ ] <info à collecter>

---

**Confiance globale sur l'analyse** : <faible / modéré / élevé>
**Raison** : <data suffisante / data partielle / beaucoup d'inférence>
```

## Règles dures

- **Pas d'analyse sans question stratégique.** Refuser si l'utilisateur veut juste "analyser pour le fun".
- **Inférences marquées explicitement.** Jamais confondre observation et inférence.
- **Pas de SWOT naïf.** Les forces/faiblesses générales sont interdites — remplacées par l'analyse 6 dimensions.
- **Pas plus de 3 moves.** Plus = l'utilisateur n'en fait aucun.
- **Confiance nommée.** Chaque move a son niveau de confiance.
- **Pas de prédiction de faillite / succès**. "Ils vont couler dans 6 mois" n'est pas une analyse — c'est une opinion déguisée.

## Piège classique

L'utilisateur veut une analyse "complète" d'un concurrent Apple ou Google. Refuser : ces concurrents ont des départements entiers qui les étudient. Proposer une analyse **ciblée sur un segment** où la comparaison est pertinente.

Autre piège : l'utilisateur fournit uniquement la landing page et attend une analyse à 360°. Répondre avec ce qui est possible depuis la landing, et lister explicitement les 5-10 autres sources nécessaires pour une analyse sérieuse.
