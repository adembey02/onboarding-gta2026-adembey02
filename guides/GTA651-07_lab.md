# GTA651 — Séance 07 / 15 — Prévisions, modélisation des risques et données synthétiques

> Guide de studio (version Markdown). PDF équivalent : `docs/lab-guides/GTA651-07_lab.pdf`.

## En bref

- **Date :** 17 juin 2026
- **Horaire :** 8 h 30 – 11 h 30
- **Lieu :** Sherbrooke
- **Mode :** Studio
- **Temps estimé :** 150 min (~2.5 h)

## Objectif

Comprendre comment l'IA transforme les pratiques de prévision et de modélisation des risques en analysant Citibank (simulation de conditions de marché) et NVIDIA (données synthétiques). Évaluer les opportunités et limites. Produire un rapport d'évaluation.

## Résultats d'apprentissage

- Expliquer comment Citibank utilise l'IA pour simuler des conditions de marché (crashes, hausses de taux) et évaluer l'impact sur les portefeuilles.
- Comparer la modélisation par données synthétiques (NVIDIA) et par données historiques (Citibank) — avantages et limites de chaque approche.
- Évaluer les conditions dans lesquelles l'IA prédictive apporte une réelle valeur d'affaires vs un risque de fausse confiance.
- Produire un rapport d'évaluation d'un modèle prédictif avec ses forces et faiblesses.

## Points clés

- Citibank : simuler des futurs possibles est plus puissant que se fier au passé — mais les simulations ont leurs limites.
- NVIDIA : les données synthétiques permettent d'entraîner l'IA sur l'impossible, mais elles doivent être validées contre le réel.
- Le vrai risque n'est pas que l'agent se trompe — c'est qu'il se trompe systématiquement et que personne ne le détecte.
- Un modèle à 80 % de confiance signifie 20 % d'erreur. La question d'affaires : quel est le coût de ces 20 % ?
- Le gestionnaire qui orchestre un agent prédictif reste responsable de l'interprétation et de la décision finale.
- L'IA prédictive n'est pas magique — elle nécessite des données de qualité et une validation humaine rigoureuse.

## Idées reçues à déjouer

  **Réalité :** 80 % de confiance ne signifie pas 80 % de précision. La confiance est une probabilité estimée par le modèle — elle peut être mal calibrée. Un modèle peut être 'très confiant' et complètement faux. La calibration de la confiance est un sujet en soi. Le gestionnaire doit savoir si le modèle sous-estime ou surestime systématiquement sa propre confiance.
  **Réalité :** Les données synthétiques complètent les données réelles, elles ne les remplacent pas. NVIDIA utilise les deux : synthétique pour la couverture de scénarios rares, réel pour la validation. Le gap sim-to-real est un problème réel : un véhicule qui performe bien en simulation peut échouer dans la vraie vie. La validation sur données réelles reste indispensable.
  **Réalité :** L'IA prédictive bien gouvernée est souvent moins risquée qu'une décision humaine seule — elle traite plus de données, est moins sujette aux biais cognitifs, et offre une traçabilité. Le risque apparaît quand l'humain abdique sa responsabilité d'interprétation et de jugement (automation bias). L'IA + humain bien orchestré bat généralement chacun séparément.

## Déroulé

### Partie 1 — Citibank : l'IA prédictive en finance  *(50 min)*

Wooclap d'ouverture sur la confiance à 75 %. Modélisation des risques : historique vs simulation. Comment Citibank génère des futurs possibles. Limites : le modèle ne peut pas prédire le sans-précédent (cygne noir). Calibration de la confiance : qu'est-ce que '75 %' signifie vraiment ? Le rôle du gestionnaire qui orchestre l'agent : interpréter, contextualiser, décider — pas exécuter aveuglément.

### Partie 2 — NVIDIA : données synthétiques approfondies  *(50 min)*

De la simulation à l'entraînement. Le gap sim-to-real : quand le virtuel ne reflète pas le réel. Stratégies de validation : tester les agents entraînés sur synthétique avec des données réelles. Convergence Citibank + NVIDIA : mêmes principes (générer du futur possible, valider, gouverner), secteurs différents. Le coût d'une fausse alerte vs alerte manquée : asymétrie qui doit guider la décision.

### Partie 3 — Pause  *(10 min)*

Pause. Afficher la structure du rapport d'évaluation à l'écran.

### Partie 4 — Exercice : rapport d'évaluation  *(40 min)*

Individuel : rédiger le rapport d'évaluation pour Citibank ou NVIDIA. Identifier forces, faiblesses, recommandation. Échange en paires : critique sur les faiblesses identifiées (sont-elles crédibles ? complètes ?). 3 présentations finales à la classe.

## Lab

**Objectif du lab :** Évaluer un agent prédictif réel (Citibank ou NVIDIA) avec un œil critique : forces, faiblesses, conditions de succès. Démontrer la capacité à détecter les risques de fausse confiance qu'une analyse naïve manquerait.

**Livrable :** Rapport d'évaluation (2 pages)

**Fichiers à produire (`repo_artifacts`) :**

- `portfolio/M3_rapport_evaluation.pdf` — Rapport d'évaluation complété
- `ai-usage.md` — Divulgation de l'usage IA si applicable

## Remise

- **Échéance :** Avant la séance 8 (8 juillet 2026)
- **Artefacts requis :**
  - `portfolio/M6_rapport_evaluation.pdf`
  - `ai-usage.md`
- **Rubrique de notation :**
  - **description_modele** (20 %) — Le modèle est décrit précisément avec données publiques. Le rôle agentique est nommé.
  - **distinction_donnees** (15 %) — La distinction données réelles vs synthétiques est claire et démontre la compréhension.
  - **forces_documentees** (20 %) — Au moins 2 forces avec exemples concrets. Pas de généralités.
  - **faiblesses_critiques** (25 %) — Au moins 2 faiblesses crédibles. La pensée critique est la compétence clé.
  - **recommandation** (15 %) — Recommandation argumentée (déployer/ajuster/rejeter) avec conditions de succès.
  - **ai_disclosure** (5 %) — ai-usage.md présent.

## Lectures

- [BIS — AI in financial risk management (2023)](https://www.bis.org/publ/work) — Cadre de référence sur l'usage de l'IA dans la gestion des risques bancaires.
- [NVIDIA — Synthetic Data Generation for AV (technical paper)](https://www.nvidia.com/en-us/self-driving-cars/) — Comment NVIDIA génère et valide ses données synthétiques pour l'autonomie.
- [Sim-to-Real Transfer in Deep Reinforcement Learning (survey 2020)](https://arxiv.org/abs/2009.13303) — Vue d'ensemble du défi sim-to-real — lecture optionnelle technique.
- [Taleb — The Black Swan (extraits sur l'imprévisibilité)](https://en.wikipedia.org/wiki/The_Black_Swan_(Taleb_book)) — Pourquoi les modèles prédictifs échouent face aux événements rares à fort impact.

---

*Généré automatiquement à partir de `content/sessions/GTA651-07.yaml`. Pour corriger une coquille, modifiez le YAML source et poussez sur `master` — la CI régénère PDF + Markdown.*
