# L3 — Risques du cycle de vie d'un agent IA

**Étudiant·e** : Adembey02
**Séance** : S03 — Déployer et gérer un agent IA  
**Date limite** : avant le début de S04

---

## Contexte

Un agent IA comporte des risques à chaque phase de son cycle de vie : conception,
déploiement et opération. Ce livrable vous demande d'identifier **3 risques distincts**
associés à un agent IA de votre choix et de proposer une mitigation concrète pour chacun.

Précisez l'agent et le contexte organisationnel en tête de document (½ ligne suffit).

**Agent choisi** : Agent analyste de dossier hypothécaire pour une banque de détail québécoise

---

## Risque 1 — Hallucinations de synthèse

**Phase du cycle de vie** : Opération

**Description** : Le moteur LLM peut générer des conclusions erronées ou inventer des données lors de la synthèse des pièces justificatives et des ratios financiers.

**Impact potentiel** : Une décision de prêt biaisée ou incorrecte peut conduire à des pertes financières et une exposition réglementaire accrue.

**Mitigation proposée** : Mettre en place une revue humaine systématique des recommandations, exiger la traçabilité des sources et verrouiller les réponses factuelles du modèle.

---

## Risque 2 — Exposition de données personnelles

**Phase du cycle de vie** : Déploiement

**Description** : Pendant l'intégration, des documents sensibles (revenus, relevés bancaires, informations personnelles) peuvent circuler vers des services externes non conformes.

**Impact potentiel** : Violation de la Loi 25, sanctions AMF, perte de confiance des clients et atteinte à la réputation.

**Mitigation proposée** : Héberger le traitement dans un environnement régional contrôlé, chiffrer les données en transit et au repos, et limiter l'accès aux utilisateurs autorisés.

---

## Risque 3 — Qualité insuffisante des données d'entrée

**Phase du cycle de vie** : Conception

**Description** : Les bases de données clients et documents PDF contiennent des informations manquantes, incohérentes ou mal structurées.

**Impact potentiel** : Le modèle produit des analyses imprécises et augmente le temps de correction manuelle pour les analystes.

**Mitigation proposée** : Lancer un programme de nettoyage de données en amont, standardiser les formats et valider la qualité sur un échantillon avant l'industrialisation.

---

*Longueur cible : ½ page. Remettez ce fichier complété (Markdown ou PDF) sous
`portfolio/L3_risques_cycle_vie.pdf` avant le début de S04.*
