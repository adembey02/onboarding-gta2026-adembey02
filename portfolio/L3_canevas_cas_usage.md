# L3 — Canevas de cas d'usage IA

**Étudiant·e** : <!-- votre identifiant GitHub -->  
**Séance** : S03 — Du cas d'usage au déploiement : structurer un projet IA  
**Date limite** : avant le début de S04

---

> **Livrable L3 (deux parties requises)**  
> Ce fichier = Partie A — le canevas 7 sections (à remettre ici).  
> `L3_risques_cycle_vie.md` = Partie B — 3 risques avec mitigations (à remettre dans le même dossier).  
> Les deux fichiers complétés sont nécessaires pour obtenir le crédit pass/fail (1 % du cours).

---

## Cas d'usage choisi

**Secteur** : services financiers — prêts hypothécaires  
**Processus ciblé** : analyse et validation de 120 demandes de prêt hypothécaire par semaine.

---

## Section 1 — Problème d'affaires précis

La banque actuelle traite les dossiers hypothécaires manuellement, ce qui crée des délais de décision trop longs et génère des retards de communication aux clients. L'inaction entraîne une baisse de satisfaction, une perte d'affaires et une charge de travail élevée pour les analystes crédit.

---

## Section 2 — Rôle spécialisé que l'agent orchestre ⭐

Agent analyste de dossier hypothécaire pour les conseillers crédit. L'agent synthétise les pièces justificatives, identifie les risques de solvabilité et prépare une recommandation standardisée pour l'expert humain.

---

## Section 3 — Données nécessaires et disponibilité

Données structurées : historiques de crédit, revenus, ratios d'endettement, valeurs de garantie. Données non structurées : pièces justificatives PDF, lettres d'emploi, relevés bancaires. Ces données sont détenues par les services crédit et conformité et sont partiellement disponibles dans le CRM et le GED interne.

---

## Section 4 — Solution IA proposée

Approche : agent basé sur un LLM avec recherche augmentée (RAG) et extraction de documents, connecté aux systèmes internes de prêt. Fournisseur ciblé : plateforme cloud canadienne pour respecter la gouvernance des données. Ce choix permet d'analyser les documents et de fournir des recommandations tout en conservant le contrôle des données.

---

## Section 5 — Métriques de succès

| Type | Métrique | Valeur cible |
|---|---|---|
| Technique | Précision d'extraction des données critiques | ≥ 95 % |
| Affaires | Durée moyenne de traitement des dossiers | de 48 min → 18 min |

---

## Section 6 — Risques et mitigations

**Risque principal** : erreur dans l'interprétation des pièces justificatives, entraînant des recommandations de crédit incorrectes.  
**Mitigation** : supervision humaine obligatoire pour toutes les recommandations en phase pilote, validation croisée par un analyste senior et tests de qualité sur un échantillon représentatif.

---

## Section 7 — Plan de déploiement phasé

| Phase | Périmètre | Durée estimée |
|---|---|---|
| POC | Analyse de 20 dossiers hypothécaires simples dans une seule succursale | 6 semaines |
| Pilote | Extension à 3 succursales et 80 dossiers par semaine | 3 mois |
| Déploiement | Intégration à l'ensemble des équipes crédit et CRM | 6 mois |

**Sponsor exécutif identifié** : Directeur des opérations crédit

---

*Longueur cible : 300-400 mots. Remettez ce fichier complété sous `portfolio/L3_canevas_cas_usage.md` avant le début de S04.*

> **Rappel IA** : les outils IA sont permis. Toute utilisation doit être déclarée dans `ai-usage.md` à la racine de votre dépôt.
