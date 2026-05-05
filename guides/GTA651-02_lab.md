# GTA651 — Séance 02 / 15 — Sélectionner des solutions IA : décision, opérations, productivité

> Guide de studio (version Markdown). PDF équivalent : `docs/lab-guides/GTA651-02_lab.pdf`.

## En bref

- **Date :** 13 mai 2026
- **Horaire :** 8 h 30 – 11 h 30
- **Lieu :** Sherbrooke
- **Mode :** Studio
- **Temps estimé :** 150 min (~2.5 h)

## Objectif

Apprendre à évaluer et sélectionner des solutions IA en comparant des déploiements réels : Brex (CFO virtuel), Salesforce Einstein (aide à la décision commerciale) et Microsoft Copilot 365 (productivité). Développer un cadre de sélection technologique et l'appliquer pour produire une grille d'évaluation comparative.

## Résultats d'apprentissage

- Comparer les catégories de solutions IA (automatisation, aide à la décision, génération de contenu, analyse prédictive) avec des exemples réels.
- Appliquer un cadre de sélection technologique (impact × faisabilité × risque × coût) à Brex, Salesforce Einstein et Microsoft Copilot 365.
- Identifier les prérequis organisationnels (données, compétences, infrastructure) pour chaque solution.
- Produire une grille d'évaluation comparative documentée.

## Points clés

- Trois catégories d'agents : décision (Einstein), opérations (Brex), productivité (Copilot) — chacun orchestre un rôle spécialisé différent.
- La sélection n'est pas une question technique — c'est un alignement entre le problème, le contexte organisationnel et les prérequis.
- Brex pour la PME sans CFO. Salesforce Einstein pour l'équipe commerciale. Copilot pour tous les knowledge workers.
- Agent spécialisé (Einstein, Brex) : précision élevée dans son domaine. Agent généraliste (Copilot) : flexibilité sur de nombreux usages.
- Trois prérequis universels : données accessibles et propres, compétences minimales pour gouverner l'agent, sponsor exécutif.
- La grille de sélection est un outil de structuration, pas une formule — le contexte détermine la pondération.

## Idées reçues à déjouer

  **Réalité :** La puissance technique n'est pas le critère de sélection — c'est la pertinence au problème d'affaires. ChatGPT est très puissant mais pas conçu pour l'intégration CRM de Salesforce. Brex est spécialisé pour les PME financières. Copilot est généraliste. Le bon agent est celui qui résout le bon problème dans le bon contexte organisationnel, pas celui qui a le plus de paramètres.
  **Réalité :** L'intégration est souvent le facteur limitant principal, pas la technologie. Salesforce Einstein nécessite des données CRM propres et structurées. Copilot nécessite Microsoft 365 et des processus de travail adaptés. La sélection doit inclure une évaluation des prérequis organisationnels : données, compétences, systèmes existants, et budget d'intégration — distinct du prix de la licence.
  **Réalité :** La grille est un outil de structuration, pas une formule magique. Les critères sont pondérés différemment selon le contexte — pour une PME, la faisabilité prime ; pour un groupe financier, la conformité réglementaire peut tout dominer. Les scores sont des jugements, pas des vérités. La grille aide à défendre une décision devant un comité, pas à éliminer l'incertitude.

## Déroulé

### Partie 1 — Taxonomie des agents IA : décision, opérations, productivité  *(50 min)*

Wooclap d'ouverture : quelle tâche vous vole le plus de temps ? Lien avec S01 : si la complexité technique monte, quels rôles voulez-vous orchestrer en premier ? Trois catégories d'agents : décision (Salesforce Einstein — prédire, recommander), opérations (Brex — exécuter, catégoriser, alerter), productivité (Copilot 365 — résumer, rédiger, analyser). Matrice généraliste vs spécialisé × faible enjeu vs haut enjeu. Chaque catégorie illustrée avec son rôle spécialisé et ses prérequis.

### Partie 2 — Cadre de sélection appliqué  *(50 min)*

La grille de sélection : 4 critères (impact d'affaires, faisabilité, risque, coût total de possession). Application aux 3 agents dans 2 contextes : PME 50 employés vs grande entreprise 500+. La même solution peut scorer radicalement différemment selon le contexte. Exemple : Brex score 4/5 en faisabilité pour une PME, 2/5 pour un groupe financier qui a déjà un CFO et un ERP complexe. Discussion : pourquoi le contexte organisationnel est le facteur de sélection le plus important.

### Partie 3 — Pause  *(10 min)*

Pause. Afficher la grille vierge (5 critères) à l'écran pour préparer l'exercice.

### Partie 4 — Exercice : votre grille d'évaluation d'agents  *(40 min)*

Par équipes de 3 : choisir un contexte (PME ou grande entreprise), remplir la grille comparative pour les 3 agents, justifier chaque score avec un fait ou une hypothèse vérifiable, conclure avec une recommandation argumentée. 3-4 équipes présentent, discussion sur les désaccords entre équipes. Point pédagogique : classer un agent comme "meilleur" sans spécifier pour qui et dans quel contexte est une erreur.

## Lab

**Objectif du lab :** Appliquer le cadre de sélection (impact × faisabilité × risque × coût) à trois agents IA dans un contexte organisationnel précis. Démontrer que la sélection dépend du contexte, pas de la puissance technique de l'agent.

**Livrable :** Grille comparative complétée avec recommandation argumentée pour deux contextes

**Fichiers à produire (`repo_artifacts`) :**

- `portfolio/M1_grille_selection_agents.pdf` — Grille complétée, format PDF ou document partagé
- `ai-usage.md` — Divulgation de l'usage IA si des outils ont aidé

## Remise

- **Échéance :** Avant le début de la séance 3 (20 mai 2026)
- **Artefacts requis :**
  - `portfolio/M1_grille_selection_agents.pdf`
  - `ai-usage.md`
- **Rubrique de notation :**
  - **contexte_organisationnel** (30 %) — Le contexte est explicité (taille, secteur, budget). La recommandation est différente selon le contexte PME vs grande entreprise. Les scores changent de façon justifiée entre les deux contextes.
  - **justification_criteres** (30 %) — Chaque score est accompagné d'une justification factuelle ou d'une hypothèse vérifiable. Les 4 critères (impact, faisabilité, risque, coût) sont tous adressés.
  - **role_specialise_identifie** (20 %) — Le rôle spécialisé orchestré par chaque agent est nommé précisément. La valeur créée est exprimée en termes d'affaires, pas technique.
  - **recommandation_argumentee** (15 %) — La recommandation est défendable devant un comité de direction. Elle adresse le compromis entre les options, pas seulement l'option retenue.
  - **ai_disclosure** (5 %) — ai-usage.md présent même si aucun outil IA n'a été utilisé.

## Lectures

- [Salesforce — State of Sales Report (2024)](https://www.salesforce.com/resources/research-reports/state-of-sales/) — Données sur l'adoption de Salesforce Einstein et l'impact sur la productivité commerciale.
- [Microsoft — Copilot Work Trend Index (2024)](https://www.microsoft.com/en-us/worklab/work-trend-index) — Étude sur l'impact de Copilot 365 sur la productivité des knowledge workers — données Accenture incluses.
- [McKinsey — The economic potential of generative AI (2023)](https://www.mckinsey.com/capabilities/mckinsey-digital/our-insights/the-economic-potential-of-generative-ai) — Analyse des catégories de valeur créée par l'IA générative selon les fonctions d'affaires.
- [HBR — Don't Just Tell Employees Org Changes Are Coming — Explain Why (2018)](https://hbr.org/topic/subject/technology-and-analytics) — Cadre pour évaluer et sélectionner des solutions technologiques dans un contexte d'affaires.

---

*Généré automatiquement à partir de `content/sessions/GTA651-02.yaml`. Pour corriger une coquille, modifiez le YAML source et poussez sur `master` — la CI régénère PDF + Markdown.*
