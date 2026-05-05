# GTA651 — Séance 04 / 15 — Atelier d'intégration : diagnostic et recommandation IA

> Guide de studio (version Markdown). PDF équivalent : `docs/lab-guides/GTA651-04_lab.pdf`.

## En bref

- **Date :** 27 mai 2026
- **Horaire :** 8 h 30 – 11 h 30
- **Lieu :** Sherbrooke
- **Mode :** Studio
- **Temps estimé :** 160 min (~2.7 h)

## Objectif

Synthétiser les sessions 1-3 en réalisant un diagnostic complet pour une organisation fictive inspirée des cas réels (structure Goldman Sachs + enjeux Pfizer + accessibilité Brex). Produire un mémo exécutif de recommandation IA d'une page.

## Résultats d'apprentissage

- Réaliser un diagnostic des opportunités IA dans une organisation en s'appuyant sur les cadres et cas réels étudiés.
- Concevoir une recommandation IA structurée intégrant justification d'affaires, plan et gestion des risques.
- Rédiger un mémo exécutif d'une page convaincant pour un auditoire non technique.
- Critiquer constructivement les recommandations des autres équipes.

## Points clés

- Un diagnostic IA commence par identifier quel rôle spécialisé l'agent orchestrera — pas par choisir la technologie.
- Agent SaaS (Brex, Copilot) pour PME avec budget limité. Agent sur mesure pour grandes organisations avec infrastructure.
- Les contraintes réglementaires (AMF, Loi 25) définissent le périmètre DANS lequel la valeur peut être créée, pas un obstacle.
- Un mémo exécutif répond aux questions du DG : quel problème, quel agent, quel coût, quel ROI, quel risque.
- La contrainte budgétaire de 300 K$ révèle les vraies priorités stratégiques — c'est une compétence, pas un frein.
- Les 3 outils S1-S3 (fiche + grille + canevas) sont les composants d'une recommandation IA défendable.

## Idées reçues à déjouer

  **Réalité :** Un diagnostic IA commence par les processus d'affaires à fort impact, pas par la technologie. La question n'est pas 'quelle IA est la meilleure ?' mais 'quel processus coûte le plus cher à l'organisation et peut être orchestré par un agent ?' La technologie est choisie APRÈS avoir défini le problème et les contraintes.
  **Réalité :** Le mémo exécutif traduit la technique en impact d'affaires. Le DG veut savoir : quel problème est résolu, combien ça coûte, quel est le ROI, et que se passe-t-il si ça échoue. Un mémo qui décrit l'algorithme est inutile. Un mémo qui quantifie 'réduire le délai de traitement de 5 jours à 4 heures' est convaincant.
  **Réalité :** 300 K$ représente un budget de POC + pilote pour une solution SaaS, ou à peine le début pour une solution sur mesure (Goldman Sachs dépense des dizaines de millions). La contrainte budgétaire est un cadre de sélection, pas un obstacle — elle force la priorisation et révèle les vraies priorités stratégiques.

## Déroulé

### Partie 1 — Présentation de FinServ Québec  *(30 min)*

Introduction de FinServ Québec : 200 employés, 45 conseillers financiers, 12 en conformité, 8 en IT. Budget de 300 K$ pour un premier déploiement agentique. Contraintes : réglementaires AMF, Loi 25, systèmes IT vieillissants. Le DG veut : identifier l'agent le plus impactant, choisir entre SaaS et sur mesure, respecter le cadre réglementaire. Distribution des équipes de 3-4 avec spécialisation : service client, analyse conseiller, ou conformité.

### Partie 2 — Diagnostic et proposition en équipe  *(70 min)*

Chaque équipe applique les 3 outils S1-S3 : (1) Fiche d'opportunité agentique — identifier le rôle spécialisé à orchestrer, (2) Grille de sélection d'agents — comparer au moins 2 options dans le contexte FinServ, (3) Canevas de cas d'usage — structurer le projet en 7 sections. Rédiger le mémo exécutif d'une page au DG. L'IA est permise comme outil de rédaction avec divulgation — mais pas comme outil de réflexion stratégique (les décisions doivent être justifiées par l'équipe).

### Partie 3 — Pause  *(10 min)*

Pause. Les équipes finalisent leur mémo. Rappel : 3 minutes de présentation, le DG est non-technique.

### Partie 4 — Présentation au DG et critique croisée  *(50 min)*

Chaque équipe présente son mémo au 'DG de FinServ' en 3 minutes. Le DG pose 2 questions difficiles. Les autres équipes notent ce qui les a convaincus et ce qui manquait. Vote de la classe sur la meilleure proposition. Débrief : quelles décisions révèlent une vraie pensée stratégique vs une réponse générique ?

## Lab

**Objectif du lab :** Synthétiser les outils des S01-S03 pour produire un mémo exécutif recommandant un premier déploiement d'agent IA pour FinServ Québec dans les contraintes réglementaires et budgétaires données.

**Livrable :** Mémo exécutif d'une page + fiche d'opportunité + grille de sélection

**Fichiers à produire (`repo_artifacts`) :**

- `portfolio/M2_memo_finserv.pdf` — Mémo d'une page + annexes de travail
- `ai-usage.md` — Divulgation de l'usage IA si des outils ont aidé à la rédaction

## Remise

- **Échéance :** Rendu pendant la séance 4 — à remettre avant la présentation
- **Artefacts requis :**
  - `portfolio/M2_memo_finserv.pdf`
  - `ai-usage.md`
- **Rubrique de notation :**
  - **outils_appliques** (30 %) — Les 3 outils S1-S3 ont été utilisés. Fiche d'opportunité, grille de sélection et canevas de cas d'usage sont visibles dans le mémo ou les annexes.
  - **memo_executif_qualite** (30 %) — Le mémo est d'une page maximum, lisible par un non-technicien en 2 minutes. Il répond aux questions du DG : problème, agent recommandé, coût, ROI, risques.
  - **contraintes_respectees** (20 %) — Budget dans les 300 K$. Contraintes AMF et Loi 25 adressées. Recommandation réaliste pour une PME de 200 employés.
  - **defense_objections** (15 %) — L'équipe répond clairement aux 2 questions du DG (ROI et plan B). La réponse aux risques est spécifique, pas générique.
  - **ai_disclosure** (5 %) — ai-usage.md présent et honnête.

## Lectures

- [Loi 25 Québec — Résumé pour gestionnaires (CAI)](https://www.cai.gouv.qc.ca/entreprises/loi-25/) — Obligations des organisations québécoises pour les projets IA utilisant des données personnelles.
- [AMF — Utilisation de l'IA dans les services financiers](https://lautorite.qc.ca/) — Cadre réglementaire de l'AMF pour les institutions financières québécoises utilisant l'IA.
- [HBR — Building the AI-Powered Organization (2019)](https://hbr.org/2019/07/building-the-ai-powered-organization) — Comment structurer une organisation pour tirer parti de l'IA de façon durable.
- [Révision S01-S03 : fiches Klarna, GitHub Copilot, Morgan Stanley, Pfizer](https://notion.so) — Réviser les 4 cas étudiés depuis le début du cours avant cet atelier.

---

*Généré automatiquement à partir de `content/sessions/GTA651-04.yaml`. Pour corriger une coquille, modifiez le YAML source et poussez sur `master` — la CI régénère PDF + Markdown.*
