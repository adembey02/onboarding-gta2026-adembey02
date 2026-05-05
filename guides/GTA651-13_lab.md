# GTA651 — Séance 13 / 15 — Humain dans la boucle : conformité et confiance

> Guide de studio (version Markdown). PDF équivalent : `docs/lab-guides/GTA651-13_lab.pdf`.

## En bref

- **Date :** 12 août 2026
- **Horaire :** 8 h 30 – 11 h 30
- **Lieu :** Sherbrooke
- **Temps estimé :** 150 min (~2.5 h)

## Objectif

Comprendre les systèmes HITL en comparant Goldman Sachs (humain décide, IA recommande), Pfizer Charlie (revue humaine obligatoire) et Brex (IA semi-autonome). Identifier le risque d'automation bias. Produire un design d'interface HITL.

## Résultats d'apprentissage

- Classer Goldman Sachs (HITL), Brex (HOTL) et un véhicule autonome NVIDIA (HOOTL) selon les trois architectures de supervision.
- Identifier le risque d'automation bias en contexte réel (ex. : que se passe-t-il si les analystes de Goldman cessent de vérifier les recommandations IA ?).
- Concevoir une interface HITL qui force la vérification humaine réelle, inspirée de la gouvernance de Pfizer Charlie.
- Produire un design d'interface HITL avec mécanismes anti-automation-bias.

## Points clés

- Goldman = HITL strict. Brex = HOTL. Pfizer = HITL maximaliste (même pour faible risque).
- L'automation bias est le danger #1 des systèmes HITL : l'humain cesse de vérifier après exposition prolongée.
- Pfizer sacrifie de l'efficacité pour de la sécurité — choix de gouvernance, pas d'UX.
- Le design de l'interface détermine si le HITL est réel ou cosmétique.
- Un HITL mal designé peut être plus dangereux qu'un HOTL bien designé (fausse impression de contrôle).
- L'audit du superviseur humain (taux d'approbation, temps de revue) est un mécanisme anti-bias essentiel.

## Idées reçues à déjouer

  **Réalité :** Un HITL mal conçu est une illusion de sécurité. Si l'interface ne force pas la vérification réelle (juste un bouton 'approuver'), les humains tombent rapidement dans l'automation bias. Un HITL réel inclut : information contextuelle, mécanismes anti-bias, audit du superviseur, rotation. Sans ces composants, le HITL est cosmétique.
  **Réalité :** L'automation bias est prévisible et systémique. Tous les humains y sont sujets après exposition prolongée. C'est une responsabilité de design, pas d'utilisateur. Les bons systèmes intègrent des mécanismes pour le contrer : tests injectés, métriques de vigilance, rotation des reviewers.
  **Réalité :** Trop d'options paralysent. Un HOTL où l'humain peut intervenir 'à tout moment sur n'importe quelle décision' est ingérable. Le bon design définit clairement QUAND l'intervention humaine est attendue, et automatise tout le reste. Le pouvoir d'intervention sans déclencheurs clairs = pas d'intervention.

## Déroulé

### Partie 1 — Trois architectures, trois réalités  *(50 min)*

Rappel explicite de S08 (5 min) : 'En S08, vous avez conçu des pipelines HITL/HOTL/HOOTL — entrées, seuils, escalade, feedback. Aujourd'hui on revient sur le même cadre pour répondre à une question différente : pourquoi ces pipelines s'effondrent-ils humainement avec le temps ?' Le concept d'automation bias : le risque invisible qui fait dégrader le HITL après des semaines d'usage. Goldman (HITL), Brex (HOTL), véhicule autonome NVIDIA (HOOTL). Quand chaque architecture est requise ou recommandée. Pourquoi un HITL mal designé peut être pire qu'un HOTL bien designé — la fausse impression de contrôle.

### Partie 2 — Concevoir un HITL qui fonctionne  *(50 min)*

Cas Pfizer : forcer la revue réelle. Mécanismes anti-automation-bias : tests injectés, rotation des reviewers, métriques de vigilance, ralentissement intentionnel sur cas critiques, justification écrite obligatoire. Audit du superviseur humain (taux d'approbation, temps moyen de revue). Le contre-paradoxe : parfois ralentir l'humain améliore la sécurité globale.

### Partie 3 — Pause  *(10 min)*

Pause. Distribuer le canevas wireframe HITL.

### Partie 4 — Exercice : votre design HITL  *(40 min)*

Individuel : dessiner le wireframe annoté pour Goldman, Pfizer, Brex ou un agent du milestone M3-M5. Partage en paires (5 min chacun) avec critique sur : le mécanisme anti-bias est-il robuste ? Que se passe-t-il après 6 mois d'usage ? 2-3 partages au groupe.

## Lab

**Objectif du lab :** Appliquer les concepts de supervision humaine à un cas sensible.

**Livrable :** 1 paragraphe (texte ou PDF, ½ page max)

**Fichiers à produire (`repo_artifacts`) :**

- `portfolio/L13_choix_hitl.pdf` — Réflexion complétée, format PDF ou texte

## Lectures

- [Parasuraman & Manzey — Complacency and Bias in Human Use of Automation (2010)](https://journals.sagepub.com/doi/10.1177/0018720810376055) — La référence académique sur l'automation bias.
- [Goldman Sachs Engineering Blog (HITL practices)](https://developer.gs.com/) — Insights publics sur les architectures HITL chez Goldman.
- [Pfizer Digital Engineering — Charlie governance](https://www.pfizer.com/news) — Insights sur la revue humaine universelle chez Pfizer.
- [FAA — Automation in Cockpits (lessons for HITL design)](https://www.faa.gov/) — Leçons aviation transposables au HITL en entreprise.

---

*Généré automatiquement à partir de `content/sessions/GTA651-13.yaml`. Pour corriger une coquille, modifiez le YAML source et poussez sur `master` — la CI régénère PDF + Markdown.*
