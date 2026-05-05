# GTA651 — Séance 09 / 15 — Atelier d'intégration : construire un business case IA

> Guide de studio (version Markdown). PDF équivalent : `docs/lab-guides/GTA651-09_lab.pdf`.

## En bref

- **Date :** 15 juillet 2026
- **Horaire :** 8 h 30 – 11 h 30
- **Lieu :** Sherbrooke
- **Mode :** Studio
- **Temps estimé :** 150 min (~2.5 h)

## Objectif

Synthétiser les sessions 6-8 pour construire un business case complet justifiant un investissement IA. Utiliser les données réelles des cas étudiés pour quantifier la valeur. Produire un business case d'une page.

## Résultats d'apprentissage

- Construire un business case IA complet en une page : problème, stratégie, solution, ROI, risques, plan.
- Quantifier la valeur d'un investissement IA en s'appuyant sur les données des cas réels étudiés (Goldman, NVIDIA, Citibank, Brex).
- Anticiper et répondre aux objections du C-suite avec des données publiques réelles.
- Défendre un business case lors d'une simulation de comité de direction.

## Points clés

- Un business case agentique sans chiffres réels n'est qu'une présentation PowerPoint.
- NVIDIA, Citibank, Brex : utiliser les données publiques comme benchmarks crédibilise votre proposition.
- Le CFO veut : ROI, payback period, hypothèses. Le CEO veut : risques, plan de mitigation, métriques de go/no-go.
- L'approche par phases (pilote → extension → généralisation) réduit le risque et construit la confiance.
- Le pire business case est celui qui promet tout sans adresser les risques.
- L'architecture agentique (HITL/HOTL/HOOTL) doit apparaître explicitement — c'est un signal de maturité.

## Idées reçues à déjouer

  **Réalité :** Au contraire : un ROI démesuré déclenche le scepticisme du CFO. Un business case crédible présente des hypothèses conservatrices, ancrées dans des benchmarks réels, avec une fourchette plutôt qu'un chiffre unique. Le 'sous-promettre / sur-livrer' bat 'sur-promettre / sous-livrer'.
  **Réalité :** Un bon usage d'un benchmark ajuste pour le contexte. Les témoignages clients Brex documentent des économies de temps significatives (ex. : 70 h/mois dans certains cas) pour des PME à équipe finance réduite. Pour IndustrIA (500 employés, finance de ~8 personnes), il faut transposer en justifiant l'ajustement (linéaire ? sublinéaire ?). Sans cette transposition, le benchmark perd sa crédibilité.
  **Réalité :** L'approbation vient de la simulation des objections. Un business case qui n'anticipe pas les questions difficiles du C-suite (et n'y répond pas en avance) sera renvoyé pour révisions. La préparation aux objections est 50 % du travail.

## Déroulé

### Partie 1 — Briefing IndustrIA et benchmarks  *(30 min)*

Wooclap d'ouverture sur 'la question du CFO'. Présentation du contexte IndustrIA : 500 employés, 1.5 M$ disponibles, deux projets agentiques compétitifs (maintenance prédictive vs CFO virtuel). Présentation des 3 benchmarks publics (NVIDIA, Brex, Citibank). Format du business case 1 page. Critères d'évaluation explicites.

### Partie 2 — Construction du business case en équipe  *(70 min)*

Travail en équipes de 3-4. Chaque équipe choisit son angle (maintenance prédictive, CFO virtuel, ou les deux). Construction itérative du business case avec coaching du professeur (rotation entre les équipes). 15 dernières minutes : préparation des réponses aux objections (CFO et CEO).

### Partie 3 — Pause  *(10 min)*

Pause. Préparer la salle pour la simulation comité de direction.

### Partie 4 — Simulation de comité de direction  *(40 min)*

Chaque équipe (5-7 min) présente son business case devant un comité fictif. Le professeur joue le CFO ; deux étudiants jouent le CEO et le VP RH. Questions tranchantes obligatoires. Vote final du CA : approuvé / révisions / rejeté. Débrief commun sur les patterns observés (ce qui passe, ce qui bloque).

## Lab

**Objectif du lab :** Synthétiser les compétences des sessions 6-8 dans un livrable d'équipe : business case 1 page complet, défendable devant un C-suite réel, ancré dans les benchmarks publics des cas étudiés.

**Livrable :** Business case 1 page (équipe)

**Fichiers à produire (`repo_artifacts`) :**

- `portfolio/M4_business_case.pdf` — Business case 1 page
- `ai-usage.md` — Divulgation de l'usage IA si applicable

## Remise

- **Échéance :** Avant la séance 10 (22 juillet 2026)
- **Artefacts requis :**
  - `portfolio/M4_business_case.pdf`
  - `ai-usage.md`
- **Rubrique de notation :**
  - **probleme_quantifie** (15 %) — Le problème est chiffré, pas vague.
  - **benchmark_credible** (20 %) — Au moins un benchmark public est cité avec source et transposé au contexte.
  - **roi_avec_hypotheses** (20 %) — ROI avec hypothèses explicites, conservatrices, et fourchette.
  - **reponse_objections** (15 %) — Réponse anticipée aux objections CFO (chiffres) et CEO (risques).
  - **plan_par_phases** (15 %) — Plan en 3 phases avec métriques de go/no-go.
  - **architecture_agentique** (10 %) — Architecture agentique (HITL/HOTL/HOOTL) nommée et justifiée.
  - **ai_disclosure** (5 %) — ai-usage.md présent.

## Lectures

- [HBR — How to Build a Business Case for AI (2024)](https://hbr.org/topic/subject/artificial-intelligence) — Cadre de référence pour structurer un business case IA.
- [NVIDIA Omniverse Replicator — Synthetic data benchmarks](https://www.nvidia.com/en-us/omniverse/) — Données publiques sur le ROI des données synthétiques.
- [Brex Engineering Blog — CFO virtual benchmarks](https://www.brex.com/journal) — Benchmarks publics sur les économies de temps des agents finance.
- [McKinsey — The state of AI in 2024](https://www.mckinsey.com/capabilities/quantumblack/our-insights) — Statistiques sectorielles pour ancrer vos business cases.

---

*Généré automatiquement à partir de `content/sessions/GTA651-09.yaml`. Pour corriger une coquille, modifiez le YAML source et poussez sur `master` — la CI régénère PDF + Markdown.*
