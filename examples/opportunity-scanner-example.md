# Exemple 2 — Opportunity Scanner

**Prompt utilisateur** :
> *"Je connais bien le secteur fintech en Afrique de l'Ouest. Je me dis qu'il doit y avoir des opportunités, mais je vois pas où frapper. Aide-moi à identifier."*

---

## Sortie (résumée)

🔍 **Module : Opportunity Scanner**

Avant de scanner, j'ai besoin de cadrer 3 choses :

**1. Contraintes** : tes compétences / capital / temps / horizon.
**2. Ce que tu appelles "bien connaître"** : tu as été opérateur ? investisseur ? utilisateur ? → ça change ce qu'on peut exploiter.
**3. Question** : tu cherches un move entrepreneurial ? investissement ? partnership ?

*[L'utilisateur répond : "Ex-opérateur fintech, 5 ans d'expérience paiements B2B. Capital dispo modeste (~50-100K€). 12 mois horizon. Je cherche où entreprendre."]*

OK, on sait où on cherche. Application du scanning 5 sources.

---

# Opportunity Scanner — Fintech Afrique de l'Ouest

## 🎯 Question centrale
Où frapper dans la fintech AOF pour un opérateur paiements B2B avec 50-100K€ et 12 mois ?

## 🔍 Scanning — 5 sources

### 1. Frustrations clients observables
**Sources à consulter** : groupes FB commerçants, threads LinkedIn de PME, AppStore reviews de Flutterwave/Wave/OPay.

**Patterns récurrents probablement présents** :
- **Réconciliation comptable** : les commerçants passent des heures à rapprocher les paiements mobile money avec leurs comptes
- **Multi-wallet fragmentation** : les PME doivent jongler entre Wave, Orange Money, MTN MoMo, Airtel Money selon les clients
- **Cash-out coûteux** : frais cachés sur les retraits de grosses sommes
- **Factures B2B** : aucun standard d'émission / acceptation

### 2. Segments mal servis
- **PME 10-50 salariés** : trop grosses pour du pur mobile money, trop petites pour des intégrations bancaires custom
- **Secteurs spécifiques** : transport informel, restaurants, distribution FMCG — besoins verticaux non servis par les fintechs généralistes
- **Commerçants transfrontaliers** (CEDEAO) : galère devises + règlementaire

### 3. Workflows hors-produit
- **Tableurs partout** : beaucoup de petites boîtes gèrent les paiements dans Excel/Google Sheets
- **WhatsApp comme interface client** : commerçants envoient reçus manuels
- **Paperasse règlementaire** : compliance BCEAO faite à la main

### 4. Signaux de timing
- **Instant payment BCEAO** (PI-SRWA) en déploiement → nouvelle infrastructure à exploiter
- **Régulation "paiements instantanés"** qui force une standardisation
- **Croissance des marketplaces B2B** (Sokowatch, Copia, Jumia B2B) — besoin de back-office paiements
- **LLMs disponibles** pour automatiser du traitement de documents non structurés (factures, relevés)

### 5. Croisements inhabituels
- Fintech × **accounting pur local** (pas QuickBooks qui ne parle pas aux mobile money)
- Fintech × **logistique** (COD + mobile money + cash-to-cash)
- Fintech × **LLM** (automatisation facture, compliance)

## 📊 Opportunités candidates

| # | Opportunité | Problème ×3 | Taille ×2 | WTP ×2 | Fit ×3 | Timing ×2 | Accès ×1 | Score |
|---|---|---|---|---|---|---|---|---|
| 1 | Réconciliation auto multi-wallet pour PME | 5 | 4 | 4 | 5 | 5 | 4 | **58** |
| 2 | Factures B2B standardisées | 4 | 3 | 3 | 4 | 4 | 3 | 43 |
| 3 | Compliance BCEAO automatisée | 4 | 2 | 4 | 3 | 4 | 2 | 37 |
| 4 | Paiements CEDEAO transfrontaliers | 4 | 3 | 4 | 3 | 3 | 2 | 37 |

## 🏆 Top 1 retenue : Réconciliation multi-wallet pour PME

**Client précis** : PME AOF de 10-50 salariés qui reçoivent des paiements sur 3+ wallets différents et ont au moins 1 comptable (interne ou externe).

**Problème exact** : le comptable passe 1-2 jours par mois à rapprocher les paiements mobile money avec les factures clients. Erreurs fréquentes, stress mensuel, zéro scalabilité.

**Résolution actuelle** : Excel + copier-coller des relevés mobile money + recherche manuelle de correspondance.

**Pourquoi mal résolu** : les fintechs leaders ciblent soit le B2C (Wave) soit les grosses entreprises (intégrations SAP). Entre les deux, rien.

**Ce qui rend viable maintenant** :
- APIs mobile money plus ouvertes (Flutterwave, Wave disposent d'APIs)
- LLMs pour traiter les formats hétérogènes
- Instant payment BCEAO qui standardise

**Pourquoi toi** : 5 ans ops fintech = tu connais les APIs, les biais opérationnels, les clients PME.

## ⚖️ Test d'invalidation (2 semaines)

**INVALIDERAIT** : en parlant à 10 PME cible, aucune ne nommerait la réconciliation comme top 3 douleur.

**VALIDERAIT** : 6+ PME sur 10 disent *"oh oui, mon comptable me casse les pieds avec ça chaque mois"* ET 3+ disent qu'elles paieraient 50-150€/mois pour automatiser.

## ✅ Moves (2 semaines)

1. **Parler à 10 PME cible en face-à-face** — confiance : élevée
   - Objectif : valider que le problème est top 3 dans leur vie
   - Pas de pitch produit — juste écouter
2. **Parler à 3 comptables / experts-comptables** — confiance : élevée
   - Ils sont le vrai décideur sur ce genre d'outil
3. **Auditer les APIs disponibles** (Wave, Orange Money, MTN MoMo, Flutterwave) — confiance : modérée
   - Vérifier ce qui est techniquement faisable avec 50-100K€ de dev

## ⚠️ Angles morts
- Je n'ai pas fait les 10 interviews — toute l'analyse repose sur des patterns inférés
- Les APIs mobile money peuvent être moins ouvertes qu'il n'y paraît
- La compliance BCEAO pour un acteur agrégateur peut être un enjeu majeur

## 🔬 À creuser
- [ ] Status license BCEAO pour agrégateur de paiement
- [ ] Pricing de solutions existantes (Paystack B2B, SASware, etc.)
- [ ] Interviews réelles (remplace 80% des inférences)

---

**Confiance globale** : modérée avant interviews — l'opportunité est plausible, mais non validée par du terrain.

---

## Commentaires

Ce qui fait fonctionner cet exemple :
1. **Refuse de scanner sans contraintes claires** — compétences, capital, horizon
2. **Applique les 5 sources systématiquement**
3. **Scoring quantitatif** — pas de feeling
4. **Top 1 forcé** — pas top 3 dilué
5. **Tests d'invalidation précis** — observables en 2 semaines
6. **Moves de validation** — pas "construire le produit"
7. **Confiance modérée assumée** — pas de ton péremptoire
