# Cas de test — strategy-intel

11 prompts pour valider la skill. Pour chaque cas : bon module routé, question stratégique forcée, moves actionables, niveau de confiance explicite.

## Comment tester

1. Le bon module est annoncé ?
2. La question stratégique est forcée avant analyse ?
3. Les inférences sont marquées comme telles ?
4. 1-3 moves actionables + confiance + angles morts ?
5. Sources manquantes listées ?

---

## Cas 1 — Audit concurrent nommé

**Prompt** : *"Peux-tu analyser Notion comme concurrent ?"*

**Module attendu** : `competitor-teardown`
**Doit** : demander la question stratégique, lister les sources nécessaires, marquer les inférences.

**Red flags** :
- Analyse sans demander la question
- Prédiction du futur ("ils vont couler")
- SWOT générique

---

## Cas 2 — Cartographie de marché

**Prompt** : *"J'entre dans le marché du logiciel RH pour PME en France. Aide-moi à le comprendre."*

**Module attendu** : `market-mapping`
**Doit** : définir précisément le marché (JTBD + géo + segment), couvrir les 7 catégories d'acteurs, faire le power mapping explicite, identifier les bloqueurs.

**Red flags** :
- Oublie le power mapping
- Invente des parts de marché
- Oublie les adjacents/substituts

---

## Cas 3 — Recherche d'opportunité

**Prompt** : *"Je connais bien le secteur de la formation continue. Où est-ce que je pourrais lancer quelque chose ?"*

**Module attendu** : `opportunity-scanner`
**Doit** : cadrer les contraintes, passer par les 5 sources, scorer les candidates, forcer une top 1, proposer des tests d'invalidation.

**Red flags** :
- Propose 5+ opportunités sans trancher
- Pas de tests d'invalidation
- Oublie de préciser le client exact

---

## Cas 4 — Préparation de move engageant

**Prompt** : *"Je vais lancer une version entreprise de mon produit dans 6 semaines. Aide-moi à préparer."*

**Module attendu** : `strategic-move-planner`
**Doit** : quantifier l'engagement, questionner l'intention, thèse stratégique + 3 sous-hypothèses, 5 stress tests, verdict structuré, kill criteria.

**Red flags** :
- Planning sans stress tests
- Pas de kill criteria
- Thèse stratégique absente

---

## Cas 5 — Intuition de piège

**Prompt** : *"On me propose un deal exclusif avec un gros acteur. Je suis tenté mais je sens un truc pas net."*

**Module attendu** : `strategic-move-planner`
**Doit** : prendre au sérieux le signal *"pas net"*, nommer les biais possibles, stress test poussé sur l'irréversibilité, proposer contre-propositions.

**Red flags** :
- Minimise l'intuition
- Encourage à signer sans conditions
- Oublie d'explorer les alternatives

---

## Cas 6 — Analyse avec URL/contenu collé

**Prompt** : *"Voici la landing page de [concurrent]: [colle texte]. Qu'en penses-tu ?"*

**Module attendu** : `competitor-teardown`
**Doit** : analyser ce qui est là, **lister explicitement** ce qui manque pour une analyse sérieuse (autres pages, équipe, financement, reviews).

**Red flags** :
- Analyse complète à partir de la seule landing — prétendra en savoir trop
- N'identifie pas les trous

---

## Cas 7 — Pas de question stratégique

**Prompt** : *"Analyse le marché du cloud."*

**Module attendu** : `market-mapping` mais **avec refus initial**
**Doit** : refuser de faire une analyse massive sans segment, demander la question stratégique précise, proposer reformulations ("B2B SaaS hébergé ? IaaS ? edge computing ?").

**Red flags** :
- Produit un rapport de 20 pages sur "le cloud" en général
- Accepte le périmètre flou

---

## Cas 8 — FOMO déguisé en stratégie

**Prompt** : *"Tout le monde lève en Serie A en ce moment sur l'IA, je dois lever moi aussi. Aide-moi à préparer."*

**Module attendu** : `strategic-move-planner`
**Doit** : **nommer le FOMO**, questionner si la levée sert vraiment la thèse business ou juste le bruit externe, proposer de revenir avec une vraie raison.

**Red flags** :
- Fait un plan de pitch deck sans challenger l'intention
- Acquiesce à "tout le monde le fait"

---

## Cas 9 — Move trop gros pour la taille

**Prompt** : *"On a 200K€ en caisse, 18 mois de runway. Je veux ouvrir un bureau à Dubai et recruter 5 personnes sur place."*

**Module attendu** : `strategic-move-planner`
**Doit** : pointer que le move engage 80%+ des ressources, tester la réversibilité, proposer une version réduite (1 scout sur place pendant 6 mois avant décision d'équipe).

**Red flags** :
- Planifie l'expansion sans questionner la taille
- Oublie la ruin check

---

## Cas 10 — Opportunité séduisante mais hors force

**Prompt** : *"Je vois une opportunité énorme dans la blockchain pour des NFTs immobiliers. J'ai jamais touché à ces sujets mais je sens que c'est le bon moment."*

**Module attendu** : `opportunity-scanner` qui **redirige** partiellement vers `thinking-os/circle-of-competence`
**Doit** : reconnaître le fit faible, proposer soit un parcours d'apprentissage, soit un pivot vers une opportunité mieux alignée avec les forces réelles.

**Red flags** :
- Planifie le lancement sans questionner le fit
- Encourage "tu sens que c'est le bon moment"

---

## Cas 11 — Composition avec d'autres skills

**Prompt** : *"Je veux pivoter ma boîte de B2C vers B2B. Comment décider ?"*

**Module attendu** : `strategic-move-planner` (pour la préparation du pivot) MAIS avec recommandation d'utiliser d'abord `thinking-os` pour la décision elle-même.
**Doit** : clarifier que "comment décider" est une question pour `thinking-os/opportunity-cost` ou `first-principles`, puis que `strategic-move-planner` intervient **après** la décision pour préparer l'exécution.

**Red flags** :
- Planifie le pivot sans s'assurer que la décision est prise
- Confond décision et préparation

---

## Critères de validation globaux

La skill est validée si :

- ✅ **9/11** cas routent sur le bon module (ou suggèrent la bonne composition)
- ✅ **100%** des outputs demandent/forcent une question stratégique
- ✅ **100%** des outputs listent des moves actionables (max 3) avec confiance
- ✅ **100%** des outputs incluent une section "à vérifier" pour affiner
- ✅ **0%** de prédictions péremptoires ("ils vont couler", "tu vas exploser")
- ✅ Les cas 5, 8, 9, 10 (biais ou mauvais fit) déclenchent les bons garde-fous

Si plusieurs échecs :
- Routage → revoir la table dans SKILL.md
- Analyses creuses → durcir "Règles dures" du module concerné
- Manque de composition → ajouter exemples de redirection vers thinking-os/execution-os/learning-os
