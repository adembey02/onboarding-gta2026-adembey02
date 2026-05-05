# GTA651 — Séance 08 / 15 — Pipelines de décision assistés par l'IA

> Guide de studio (version Markdown). PDF équivalent : `docs/lab-guides/GTA651-08_lab.pdf`.

## En bref

- **Date :** 8 juillet 2026
- **Horaire :** 8 h 30 – 11 h 30
- **Lieu :** Sherbrooke
- **Temps estimé :** 150 min (~2.5 h)

## Objectif

Concevoir un pipeline de décision assistée par l'IA en s'inspirant des cas réels : Goldman Sachs (IA + analystes), Morgan Stanley (IA + conseillers) et Brex (IA autonome pour PME). Comprendre quand l'IA décide seule et quand l'humain intervient.

## Résultats d'apprentissage

- Concevoir un pipeline de décision IA en s'inspirant des architectures réelles de Goldman Sachs, Morgan Stanley et Brex.
- Distinguer les décisions automatisables (Brex : alertes budgétaires) des décisions nécessitant un jugement humain (Goldman : stratégie d'investissement).
- Définir des seuils de confiance et des critères d'escalade humaine dans un pipeline IA.
- Produire un diagramme de pipeline de décision IA avec points d'escalade.

## Points clés

- Goldman Sachs : HITL strict — l'agent recommande, l'humain décide. Standard en finance à haut enjeu.
- Morgan Stanley : HOTL — l'agent enrichit le conseiller, ne contacte jamais le client directement.
- Brex : HOTL avec escalade conditionnelle — l'agent agit sans approbation préalable sur les décisions à faible enjeu ; escalade vers l'humain pour les décisions à haut enjeu.
- Le niveau d'autonomie dépend de 3 facteurs : enjeu de la décision, coût de l'erreur, disponibilité d'un expert humain.
- Les seuils de confiance doivent être asymétriques selon le coût des faux positifs vs faux négatifs.
- Un bon pipeline a toujours une boucle de feedback — l'agent qui ne s'améliore pas se dégrade.

## Idées reçues à déjouer

  **Réalité :** L'autonomie n'est pas un objectif en soi — c'est un choix d'architecture qui dépend de l'enjeu, du coût d'erreur et de la disponibilité d'un expert humain. Pour les décisions à haut enjeu et faible volume, HITL bat HOOTL. Pour les décisions à faible enjeu et fort volume, HOOTL est plus efficace. Le choix d'architecture est une décision d'affaires, pas technique.
  **Réalité :** Différentes décisions méritent différents seuils. Bloquer un paiement = seuil élevé (faux positifs gênent les clients). Alerter sur une anomalie = seuil moyen. Catégoriser une dépense = seuil bas (faible coût d'erreur). Les seuils doivent être asymétriques selon le coût de chaque type d'erreur.
  **Réalité :** Sans boucle de feedback, l'agent dégrade : les patterns changent, les données évoluent, les nouveaux cas apparaissent. Un agent sans feedback devient progressivement moins pertinent. La boucle de feedback (humain corrige → agent réapprend) est un composant essentiel de l'architecture, pas un bonus.

## Déroulé

### Partie 1 — Anatomie d'un pipeline de décision IA  *(50 min)*

Reconnexion après la pause de 3 semaines (Fête nationale + relâche estivale) : 5 min pour rappeler les cas Citibank et NVIDIA de S07 — simulation de risque, gap sim-to-real, calibration de la confiance. Pont : 'En S07, vous avez évalué des agents prédictifs. Aujourd'hui : quand ces agents produisent un résultat, qui décide d'agir — et comment ?' Wooclap d'ouverture sur l'autonomie. Trois architectures réelles : Goldman (HITL strict), Morgan Stanley (HOTL — humain supervise), Brex (HOTL avec escalade conditionnelle). Quand chaque architecture est appropriée. Les 3 facteurs qui déterminent le niveau d'autonomie : enjeu de la décision, coût de l'erreur, disponibilité d'un expert humain.

### Partie 2 — Seuils, escalade et feedback  *(50 min)*

Comment définir un seuil de confiance : asymétrie des coûts (faux positifs vs faux négatifs). L'exemple Brex 72 % de confiance : que faire ? Stratégies d'escalade : seuil simple, seuil multi-critères, escalade par contexte. Boucle de feedback : comment l'agent apprend de ses erreurs en production. Sans feedback, l'agent dégrade.

### Partie 3 — Pause  *(10 min)*

Pause. Afficher les 3 architectures à l'écran pour préparer l'exercice.

### Partie 4 — Exercice : votre pipeline  *(40 min)*

Par équipes : concevoir un diagramme de pipeline pour Goldman, Morgan Stanley ou Brex (ou un cas du milestone précédent). Le diagramme doit explicitement nommer l'architecture (HITL/HOTL/HOOTL), les seuils de confiance, et la boucle de feedback. 3 présentations avec critique sur les seuils choisis.

## Lab

**Objectif du lab :** Appliquer les concepts de pipeline de décision IA à un processus concret.

**Livrable :** Diagramme annoté (1 page max)

**Fichiers à produire (`repo_artifacts`) :**

- `portfolio/L8_mini_pipeline.pdf` — Diagramme annoté, format PDF ou image

## Lectures

- [Goldman Sachs — Engineering Blog (AI in trading)](https://developer.gs.com/) — Insights publics sur l'architecture des agents de Goldman Sachs.
- [Microsoft Research — Human-AI Decision Making (2023)](https://www.microsoft.com/en-us/research/group/human-understanding-and-empathy/) — Cadre académique pour les architectures HITL/HOTL/HOOTL.
- [Brex — Engineering Blog (autonomous agents)](https://www.brex.com/journal) — Comment Brex décide ce qui est automatisable et ce qui ne l'est pas.
- [HBR — When Should AI Make the Decision? (2023)](https://hbr.org/topic/subject/artificial-intelligence) — Cadre exécutif pour décider du niveau d'autonomie agentique.

---

*Généré automatiquement à partir de `content/sessions/GTA651-08.yaml`. Pour corriger une coquille, modifiez le YAML source et poussez sur `master` — la CI régénère PDF + Markdown.*
