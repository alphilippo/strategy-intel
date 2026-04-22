# Exemple 1 — Competitor Teardown

**Prompt utilisateur** :
> *"Y Combinator vient d'annoncer un nouveau programme dédié aux startups africaines. J'anime un programme d'accompagnement de startups (SIMBA). Analyse-les comme concurrent."*

---

## Ce que la skill fait

**Détection** : *"analyse-les comme concurrent"* + nom précis → `competitor-teardown` immédiat.

**Signal** : l'utilisateur fournit peu de données dans le prompt. La skill doit demander la question stratégique précise **avant** toute analyse, puis lister les sources à consulter.

---

## Sortie

⚔️ **Module : Competitor Teardown**

Avant de plonger, j'ai besoin de préciser 2 choses :

**1. Question stratégique** : qu'est-ce que tu dois **décider ou préparer** suite à cette analyse ? Quelques hypothèses possibles :
- *"Dois-je repositionner SIMBA pour éviter la collision ?"*
- *"Puis-je me différencier par la verticalisation (ex: fintech only) ?"*
- *"Comment je protège ma dealflow / mes startups existantes ?"*
- *"Dois-je chercher un partnership avec eux plutôt que de compétir ?"*

**2. Sources** : je vois que tu n'as pas collé leur annonce. J'ai besoin de :
- L'annonce officielle (blog YC ou communiqué)
- Leur page programme si déjà live
- 3-5 posts / interviews récentes de Garry Tan (CEO YC) sur le sujet
- Leurs conditions (equity, durée, montant, format)

*[L'utilisateur colle l'annonce + un post Garry Tan + répond que la question est "comment je protège ma dealflow et où je me différencie"]*

OK, question claire, 2 sources principales. Analyse avec les données disponibles :

---

# Competitor Teardown — YC Africa Program

## 🎯 Question stratégique
Comment SIMBA protège sa dealflow et se différencie vs le programme YC dédié Afrique.

## 📊 Sources analysées

| Source | Ce qu'on y trouve |
|---|---|
| Annonce blog YC | Format (12 semaines, remote+1 semaine SF), equity (7% pour 500K USD), criteria (tech-first, early-stage) |
| Post Garry Tan | Narratif : "combler le vide de capital smart money en Afrique", focus fintech/logistique/climate |

**Sources manquantes à obtenir** :
- Liste des mentors / partners Afrique nommés
- Critères de sélection détaillés
- Les 3-5 premières startups sélectionnées (signal sur leur positionning réel)

## 🔍 Analyse en 6 dimensions

### 1. Proposition de valeur
- **Promesse centrale** : *"Accélération mondiale avec capital + réseau SF, adaptée au contexte africain"*
- **Public cible** : fondateurs tech-first (souvent anglophones, souvent diaspora-connected)
- **Différenciation claimée** : la marque YC + le network alumni + la promesse d'un demo day mondial
- **Inférence** : ils ciblent le haut du panier — fondateurs très ambitieux, prêts à scale-up mondial depuis le jour 1
- **Angle mort** : peu d'évidence qu'ils comprennent les réalités opérationnelles locales (règlementation, distribution, infra)

### 2. Pricing & modèle économique
- **Structure** : 500K USD pour 7% equity — standard YC depuis 2022
- **Signaux** : 7% reste agressif pour des early-stage africains où le capital vaut plus cher (dilution alternative inférieure via VCs locaux)
- **Inférence** : ils misent sur la **marque** et le **network** pour justifier la dilution

### 3. Distribution & acquisition
- **Canaux principaux** : leur propre marque, endorsements Garry Tan sur X, bouche-à-oreille diaspora
- **Signaux CAC** : très faible — ils n'achètent pas de trafic, les candidats viennent à eux
- **Partnerships** : probablement avec des fonds VC africains (Norrsken22, Partech Africa, etc.) — à vérifier

### 4. Produit & expérience
- **Format** : 12 semaines remote + 1 semaine SF
- **Features headline** : office hours founders YC, alumni network, demo day
- **Gaps probables** : dimension locale (réglementation, distribution physique, équipes africaines)

### 5. Équipe & culture
- **Fondateurs / leadership** : Garry Tan (CEO YC), équipe locale à confirmer
- **Recrutements récents** : à vérifier qui ils nomment comme partners Afrique — critique pour comprendre leur vraie profondeur

### 6. Trajectoire & signaux faibles
- YC n'avait jamais eu de programme régional dédié → shift stratégique important
- Le timing (2026) coïncide avec montée en visibilité des startups africaines (Flutterwave, Chipper Cash, Moove, etc.)
- Signal : YC reconnaît qu'ils perdent peut-être du dealflow au profit de l'ecosystème local

## 🏛️ Power mapping

- **Qui a le pouvoir** :
  - Garry Tan (image publique, décisions stratégiques)
  - Les fonds VC africains partenaires (dealflow, due diligence)
  - Les alumni africains déjà passés par YC (influenceurs locaux)
- **Qui pourrait les bloquer** :
  - Régulateurs (visas US pour la semaine SF)
  - VCs locaux qui ne veulent pas céder le terrain
- **Menaces émergentes** :
  - Techstars Africa, Founders Factory Africa, Google for Startups Africa — concurrents directs à positionnement similaire mais sans la marque YC

## 🔀 Analyse différentielle SIMBA vs YC Africa

| Dimension | YC Africa | SIMBA | Qui gagne ? |
|---|---|---|---|
| Marque globale | ⭐⭐⭐⭐⭐ | ⭐ à ⭐⭐ (selon ton audience) | YC |
| Compréhension contexte local | ⭐⭐ (inférence) | ⭐⭐⭐⭐⭐ | SIMBA |
| Network investisseurs Afrique | ⭐⭐⭐ (via partners) | Variable selon ton deal-flow | À préciser |
| Taille du chèque | 500K USD | À préciser | À préciser |
| Durée / intensité | 12 sem concentrées | À préciser | Selon format SIMBA |
| Sélectivité | Très haute (marque pull) | À préciser | YC sur les top-tier |
| Accessibilité | Basse (top 1% fondateurs) | Plus inclusif (selon positionning) | SIMBA sur l'accès |
| Post-programme | Alumni network mondial | Écosystème local / ministériel | Dépend de l'objectif de la startup |

**Angles d'attaque possibles** :
1. Les fondateurs qui **ne rentrent pas dans le moule YC** (moins anglophones, moins tech-first, plus operateur que technical)
2. Les secteurs où la **profondeur locale** compte plus que le network global (agritech, edutech local, retail physique)
3. Les fondateurs qui ne veulent pas **diluer à 7%** (souvent les bootstrappés ou déjà un peu matures)

**Angles de différenciation** :
1. **Pragmatisme opérationnel** vs idéologie scale-first
2. **Ancrage ministériel / public** (ton positionning SIMBA si je comprends bien)
3. **Durée plus longue** si tu le proposes (YC = 12 sem, tu peux faire 6 mois = accompagnement réel)

**Non-croisement** :
- YC prendra le top 2-3% de founders hyper-ambitieux tech-first
- SIMBA peut cibler les 10-15% suivants + les verticales qu'ils ignorent

## ✅ Moves actionables (2 semaines)

1. **Clarifier le ICP de SIMBA en opposition explicite à YC Africa** — *confiance : élevée*
   - Écrire en 3 lignes QUI tu prends et QUI tu ne prends pas
   - Publier ton positioning dans un post long (LinkedIn) qui nomme les différences
2. **Aligner 2-3 VCs africains comme co-investisseurs** — *confiance : modérée*
   - Ces VCs peuvent être menacés par YC — tu deviens un allié naturel
   - Cibler : Partech Africa, Ventures Platform, 4DX Ventures (à vérifier selon ta géographie)
3. **Approfondir la verticale où tu es le plus crédible** — *confiance : élevée*
   - Probablement fintech, agritech, ou un secteur lié au ministère avec lequel tu travailles
   - Devenir **le** programme de référence sur ce segment

## ⚠️ Angles morts assumés

- Je n'ai pas les conditions financières exactes de SIMBA — analyse différentielle partielle
- Je n'ai pas la liste des partners / mentors réels de YC Africa — leur profondeur locale réelle reste une inférence
- Je ne sais pas si SIMBA a un secteur vertical déclaré ou est généraliste

## 🔬 À vérifier

- [ ] Les partners locaux nommés par YC (signal profondeur)
- [ ] Les 3-5 premières startups YC Africa (positioning réel)
- [ ] Les réactions des VCs locaux (alliés potentiels)
- [ ] Le narratif de Garry Tan dans les 3-6 prochains mois (ajustement de message)

---

**Confiance globale** : **modérée** — l'analyse s'appuie sur 2 sources + beaucoup d'inférences. Les 3 moves proposés sont solides sur le principe, mais à affiner après collecte des données manquantes.

---

## Commentaires sur la sortie

Ce qui fait que cet exemple fonctionne :

1. **Refus d'analyser sans question stratégique** — la skill force à préciser ce qui doit être décidé.
2. **Liste explicite des sources manquantes** — pas d'analyse inventée.
3. **Inférences marquées comme telles** — jamais confondues avec observations.
4. **Power mapping explicite** — qui décide, qui bloque, qui peut être allié.
5. **Analyse différentielle honnête** — SIMBA n'est pas présenté comme "meilleur partout", les forces YC sont reconnues.
6. **3 moves actionables avec confiance différentiée** — pas 10 recommandations creuses.
7. **Confiance globale modérée** — pas de faux ton péremptoire.
