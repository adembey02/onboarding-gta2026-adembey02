# GTA651 — Séance 11 / 15 — Métriques d'évaluation de l'IA et performance organisationnelle

> Guide de studio (version Markdown). PDF équivalent : `docs/lab-guides/GTA651-11_lab.pdf`.

## En bref

- **Date :** 29 juillet 2026
- **Horaire :** 8 h 30 – 11 h 30
- **Lieu :** Sherbrooke
- **Temps estimé :** 150 min (~2.5 h)

## Objectif

Maîtriser les métriques clés pour évaluer l'IA en s'appuyant sur des données réelles : le gap labo-production (problème courant chez tous les cas étudiés), les métriques de Morgan Stanley (temps économisé par conseiller) et Pfizer Charlie (taux d'approbation accéléré). Produire un tableau de bord de suivi IA.

## Résultats d'apprentissage

- Distinguer les métriques techniques (précision, rappel) des métriques d'affaires (temps économisé, ROI, adoption) en citant Morgan Stanley et Pfizer.
- Concevoir un tableau de bord de suivi de performance IA adapté au contexte organisationnel.
- Identifier les signaux d'alerte indiquant qu'un modèle IA dérive ou doit être réentraîné.
- Produire un mockup de tableau de bord IA avec 5+ métriques alignées technique-affaires.

## Points clés

- Morgan Stanley : la métrique qui compte est l'impact sur le travail réel, pas la précision technique.
- Pfizer : un modèle précis en labo peut être dangereux en production si les données changent.
- Le data drift est le signal #1 : quand les données de production s'éloignent de l'entraînement.
- Un bon tableau de bord aligne métriques techniques (équipe IA) et métriques d'affaires (C-suite).
- L'adoption est une métrique clé : un agent que personne n'utilise ne crée aucune valeur.
- Chaque alerte doit déclencher une action — sinon c'est de la décoration.

## Idées reçues à déjouer

  **Réalité :** Le 'gap labo-production' est le piège classique. Un agent à 98 % de précision en laboratoire peut tomber à 70 % en production si les données réelles diffèrent. Surtout : un agent précis mais inutilisé crée zéro valeur. La précision technique est nécessaire mais jamais suffisante.
  **Réalité :** Un tableau de bord à 30 métriques ne sera consulté par personne. La discipline est de choisir 5-7 métriques alignées au public visé. Les exécutifs veulent 3-4 métriques d'affaires ; les équipes IA veulent 5-6 techniques. Deux tableaux distincts battent un tableau encyclopédique.
  **Réalité :** Le drift est constant et silencieux. Sans surveillance active, il passe inaperçu jusqu'à ce que les utilisateurs s'en plaignent. Les bons systèmes ont des alertes automatiques sur la distribution des entrées et des sorties — pas seulement sur la précision finale.

## Déroulé

### Partie 1 — Métriques techniques vs métriques d'affaires  *(50 min)*

Wooclap d'ouverture. Cas Morgan Stanley : heures économisées > précision du modèle. Cas Pfizer : le coût d'une erreur de classification réglementaire. Le gap labo- production : pourquoi un bon modèle peut échouer. La pyramide des métriques : techniques (équipe IA), opérationnelles (managers), d'affaires (C-suite).

### Partie 2 — Concevoir un tableau de bord IA  *(50 min)*

5 composants d'un tableau de bord efficace : métriques choisies, seuils chiffrés, codes couleur, fréquence de mise à jour, audience. Signaux de dérive (data drift, concept drift, performance drift) et déclencheurs de réentraînement. Anti-patterns à éviter (tableau encyclopédique, métriques de vanité, absence de seuils).

### Partie 3 — Pause  *(10 min)*

Pause. Affichage du canevas de tableau de bord pour préparer l'exercice.

### Partie 4 — Exercice : votre tableau de bord  *(40 min)*

Individuel : concevoir le mockup pour Morgan Stanley, Pfizer, ou un agent du milestone M3/M4. Partage en paires (5 min chacun) avec critique sur : seuils justifiés ? Public clair ? Action déclenchée par chaque alerte ? 2-3 partages au groupe.

## Lab

**Objectif du lab :** Appliquer les concepts de métriques IA à un agent concret.

**Livrable :** 3 métriques justifiées (texte ou PDF, ½ page max)

**Fichiers à produire (`repo_artifacts`) :**

- `portfolio/L11_metriques_agent.pdf` — Réflexion complétée, format PDF ou texte

## Lectures

- [Google Research — Hidden Technical Debt in Machine Learning Systems](https://research.google/pubs/pub43146/) — Le classique sur les coûts cachés de la production ML.
- [Microsoft Research — ML in Production: Drift Detection](https://www.microsoft.com/en-us/research/) — Cadres pour détecter le drift en production.
- [Morgan Stanley AI Press Releases (2023-2024)](https://www.morganstanley.com/press-releases) — Communications publiques sur les métriques d'adoption de leur agent.
- [Pfizer Digital Engineering Blog](https://www.pfizer.com/news) — Insights sur les métriques de Charlie en production.

---

*Généré automatiquement à partir de `content/sessions/GTA651-11.yaml`. Pour corriger une coquille, modifiez le YAML source et poussez sur `master` — la CI régénère PDF + Markdown.*
