# GTA651 — Séance 03 / 15 — Du cas d'usage au déploiement : structurer un projet IA

> Guide de studio (version Markdown). PDF équivalent : `docs/lab-guides/GTA651-03_lab.pdf`.

## En bref

- **Date :** 20 mai 2026
- **Horaire :** 8 h 30 – 11 h 30
- **Lieu :** Sherbrooke
- **Temps estimé :** 150 min (~2.5 h)

## Objectif

Transformer une idée d'automatisation en cas d'usage structuré et priorisé. Utiliser le déploiement de Charlie chez Pfizer comme modèle de cycle de vie IA réussi dans un secteur réglementé. Produire un canevas de cas d'usage complet.

## Résultats d'apprentissage

- Décrire le cycle de vie complet d'un projet IA (cadrage → POC → pilote → déploiement → suivi) en l'illustrant avec Pfizer Charlie.
- Structurer un cas d'usage IA avec le canevas standardisé : problème, données, solution, métriques, risques, sponsor.
- Prioriser un portefeuille de cas d'usage IA selon la matrice impact × faisabilité.
- Produire un canevas de cas d'usage IA complet et défendable.

## Points clés

- Pfizer Charlie : le POC commence là où le risque est le plus faible, pas là où l'impact est le plus grand.
- 87 % des POC IA ne passent jamais en production — pour des raisons organisationnelles, pas techniques.
- Le canevas en 7 sections : problème → rôle de l'agent → données → solution → métriques → risques → plan.
- La matrice impact × faisabilité est l'outil de priorisation le plus actionnable pour un portefeuille IA.
- Un POC sans plan d'intégration restera un POC — le déploiement se prépare dès le cadrage.
- Le sponsor exécutif est le facteur #1 de succès d'un déploiement agentique.

## Idées reçues à déjouer

  **Réalité :** Pfizer Charlie a commencé avec le contenu marketing existant — des données déjà présentes dans l'organisation. La plupart des déploiements agentiques réussis commencent avec des données disponibles, pas une infrastructure parfaite. La question n'est pas 'ai-je assez de données ?' mais 'mes données disponibles suffisent-elles pour le périmètre ciblé ?'
  **Réalité :** 87 % des POC ne passent jamais en production. Un POC teste si l'IA résout le problème technique dans des conditions contrôlées — pas si l'organisation peut déployer, maintenir et gouverner l'agent dans les conditions réelles. Le déploiement exige intégration, gouvernance, formation, gestion du changement. Le POC ne valide aucun de ces points.
  **Réalité :** Le sponsor exécutif est le facteur #1 de succès selon toutes les études sur les déploiements IA. Sans lui, le projet perd son budget lors des premières difficultés, ne peut pas forcer l'adoption organisationnelle, et manque de légitimité pour passer les contrôles réglementaires. Pfizer Charlie a réussi parce que la direction médicale a défendu le projet, pas parce que la technologie était parfaite.

## Déroulé

### Partie 1 — Le cycle de vie d'un agent IA  *(50 min)*

Wooclap d'ouverture : quel pourcentage des projets IA arrivent en production ? Révélation : environ 13-15 % — 87 % s'arrêtent au POC. Les 5 raisons principales d'échec (facteurs organisationnels, pas techniques). Cinq phases avec Pfizer Charlie comme fil rouge : cadrage → POC à faible risque → pilote avec métriques → déploiement avec gouvernance → suivi continu. Pourquoi Charlie a commencé par le marketing avant les revues médicales : gérer le risque d'abord, pas l'impact. Le déploiement se prépare dès le cadrage.

### Partie 2 — Le canevas de cas d'usage IA  *(50 min)*

Le canevas en 7 sections : (1) Problème d'affaires précis, (2) Rôle spécialisé orchestré, (3) Données nécessaires et disponibilité, (4) Solution IA proposée, (5) Métriques de succès (techniques et d'affaires), (6) Risques et mitigations, (7) Plan de déploiement phasé. Application en direct au cas Pfizer Charlie : remplir chaque section ensemble. Matrice de priorisation impact × faisabilité : classer 5 cas d'usage en 15 minutes — exercice dirigé en classe.

### Partie 3 — Pause  *(10 min)*

Pause. Afficher le canevas 7 sections à l'écran pour le retour.

### Partie 4 — Exercice : votre canevas de cas d'usage  *(40 min)*

Par équipes de 3 : choisir un processus d'affaires réel (service client, comptabilité, RH, logistique), remplir le canevas complet en 7 sections, présenter en 3 minutes. Critères d'évaluation croisée : données manquantes ? Sponsor exécutif réaliste ? Métrique quantifiable ? Vote de la classe sur le canevas le plus déployable.

## Lab

**Objectif du lab :** Appliquer les concepts du cycle de vie IA à un cas concret en identifiant les risques à chaque phase.

**Livrable :** 3 risques avec mitigations (texte ou PDF, ½ page max)

**Fichiers à produire (`repo_artifacts`) :**

- `portfolio/L3_risques_cycle_vie.pdf` — Réflexion complétée, format PDF ou texte

## Lectures

- [McKinsey — Why most AI pilots fail to scale (2024)](https://www.mckinsey.com/capabilities/quantumblack/our-insights/why-most-ai-pilots-fail-to-scale) — Analyse des raisons pour lesquelles 87 % des POC IA n'arrivent jamais en production.
- [Pfizer — AI in drug development and content creation (public)](https://www.pfizer.com/science/innovation/artificial-intelligence) — Informations publiques sur l'approche IA de Pfizer incluant le déploiement de Charlie.
- [DocuSign — AI-powered contract intelligence](https://www.docusign.com/products/intelligent-agreement-management) — Comment DocuSign utilise l'IA pour l'analyse de contrats — cas d'usage agentique dans le domaine légal.
- [MIT Sloan — Why AI projects fail (2023)](https://sloanreview.mit.edu/topic/artificial-intelligence/) — Meilleures pratiques pour structurer et déployer des projets IA en entreprise.

---

*Généré automatiquement à partir de `content/sessions/GTA651-03.yaml`. Pour corriger une coquille, modifiez le YAML source et poussez sur `master` — la CI régénère PDF + Markdown.*
