# M1 — Grille de sélection et évaluation de solutions IA

> Comparez **Brex** (CFO virtuel), **Salesforce Einstein** (aide à la décision commerciale)
> et **Microsoft Copilot 365** (productivité) sur 5 critères, pour **deux contextes** :
> une PME de 50 employés et une grande entreprise de 500+ employés.
> Concluez par une **recommandation argumentée par contexte**.
>
> Exportez en PDF et déposez `M1_grille_selection_agents.pdf` dans ce dossier.
> Mettez à jour `ai-usage.md` à la racine du dépôt (obligatoire, même si « Aucun »).

---

## Contexte 1 — PME de 50 employés

PME québécoise de services financiers spécialisés pour travailleurs autonomes, maturité numérique moyenne, budget IA limité à 120 K$ pour la première année, équipe IT interne réduite.

| Critère | Brex | Salesforce Einstein | Microsoft Copilot 365 |
|---|---|---|---|
| **1. Rôle spécialisé orchestré** _(nommez le spécialiste que l'agent remplace/augmente)_ | Agent trésorier virtuel pour la gestion de trésorerie et les prévisions de flux de trésorerie | Agent commercial pour le suivi des prospects et des opportunités clients | Agent assistant de productivité pour l'équipe administrative et les conseillers client |
| **2. Impact d'affaires** _(1-5 + justification en 1 phrase)_ | 4 : amélioration directe de la gestion de cash et réduction des risques de liquidité | 3 : aide les ventes, mais la PME n'a pas encore de CRM mature | 4 : productivité élevée sur les tâches bureautiques répétitives |
| **3. Faisabilité PME** _(1-5 + données, compétences, intégration)_ | 4 : solution SaaS adaptée aux petites structures, faible intégration requise | 2 : nécessite une adoption CRM et des données commerciales propres | 3 : facile à déployer si l'entreprise utilise Microsoft 365 déjà existant |
| **4. Coût estimé** _(ordre de grandeur annuel + TCO si pertinent)_ | 30-40 K$ / an avec intégration minimale | 40-60 K$ / an plus licence CRM et formation | 25-35 K$ / an si Microsoft 365 est déjà en place |
| **5. Risque principal** _(et mitigation concrète)_ | Mauvais alignement des prévisions de trésorerie sur les données réelles → validation mensuelle par le CFO interne | Données clients insuffisantes dans le CRM → phase de nettoyage obligatoire avant déploiement | Adoption faible par les utilisateurs sans formation ciblée → formation de 2 jours et champions internes |

### Recommandation pour la PME

Brex est la meilleure option pour cette PME car le besoin prioritaire est la gestion de trésorerie et la solution demande peu d'intégration IT. Elle offre le meilleur retour sur investissement immédiat par rapport aux autres agents.

---

## Contexte 2 — Grande entreprise de 500+ employés

Grande entreprise financière québécoise avec ERP et CRM installés, fortes exigences de gouvernance, sponsor exécutif en place (directeur de l'innovation), et besoin de productivité à l'échelle.

| Critère | Brex | Salesforce Einstein | Microsoft Copilot 365 |
|---|---|---|---|
| **1. Rôle spécialisé orchestré** | Agent contrôle de trésorerie pour la direction financière | Agent de décision commerciale pour les équipes de vente et les conseillers | Agent de productivité pour les employés de back-office et les analystes |
| **2. Impact d'affaires** _(1-5 + justification)_ | 3 : utile pour la gestion de trésorerie centrale, mais moins critique que les ventes | 5 : améliore l'efficacité commerciale et la rétention client dans un grand CRM | 4 : accélère le travail de milliers d'employés et réduit les cycles de traitement |
| **3. Faisabilité grande entreprise** _(1-5 + intégration systèmes, gouvernance)_ | 3 : possible mais nécessite alignement avec la trésorerie centrale | 4 : bien adapté à une entreprise avec CRM mature et gouvernance formelle | 5 : s'intègre facilement à un parc Microsoft 365 déjà déployé |
| **4. Coût estimé** _(licences + intégration + formation)_ | 60-80 K$ / an avec intégration des systèmes financiers | 100-130 K$ / an compte tenu de l'intégration CRM et de la formation | 80-100 K$ / an si le parc Microsoft 365 est déjà en place |
| **5. Risque principal** _(et mitigation)_ | Dépendance à des prévisions internes imprécises → gouvernance mensuelle renforcée | Problèmes de qualité des données commerciales → nettoyage et pilote sur segment de clients | Usage dispersé sans standards → charte d'utilisation et référents métiers |

### Recommandation pour la grande entreprise

Salesforce Einstein est recommandé car l'entreprise dispose déjà d'un CRM mature et le besoin commercial est prioritaire. Ce choix tire parti des données existantes et de la gouvernance en place.

---

## Synthèse — ce que la grille révèle

Le critère décisif est l'alignement du rôle spécialisé avec le besoin opérationnel du contexte : trésorerie pour la PME et ventes/CRM pour la grande entreprise. Cela montre qu'une solution IA doit être choisie en fonction du domaine métier le plus critique, pas seulement de la notoriété du fournisseur.

---

## Liste de contrôle de remise

- [x] Les 3 agents sont comparés sur les mêmes 5 critères dans les deux contextes
- [x] Le rôle spécialisé orchestré est nommé précisément pour chaque agent
- [x] Les scores sont justifiés (pas juste des chiffres)
- [x] La recommandation diffère — ou est explicitement justifiée comme identique — entre PME et grande entreprise
- [x] Le contexte d'une organisation québécoise est pris en compte (Loi 25, marché local, talent)
- [x] `ai-usage.md` mis à jour à la racine du dépôt

> **Crédit :** Jalon M1 — pass/fail (1,5 % du cours). Préparation directe à l'**Examen-cas 1** (S05, 25 %).
