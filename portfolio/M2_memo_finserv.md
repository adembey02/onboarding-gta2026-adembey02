# M2 — Mémo exécutif de recommandation IA

**Étudiant·e** : CatherineM2002  
**Équipe** : Équipe FinServ IA — CatherineM2002  
**Spécialisation d'équipe** : conseil financier  
**Cas retenu (L3)** : Aucun — nos cas personnels étaient trop distincts de ce cas  
**Séance** : S04 — Atelier d'intégration : diagnostic et recommandation IA  
**Date limite** : remis pendant la séance S04, avant la présentation au DG

---

> **Jalon M2 (1,5 % du cours — pass/fail)**  
> **Étape 1 (L3, individuel) :** Chaque membre de l'équipe a identifié et documenté un cas d'usage IA individuellement (fiche d'opportunité + canevas + risques).  
> **Étape 2 (début S04, en équipe) :** L'équipe compare les 3–4 cas apportés, délibère et choisit le cas le plus solide à développer. Le cas retenu et son auteur·e sont déclarés dans l'en-tête ci-dessus.  
> **Étape 3 (S04, en équipe) :** L'équipe rédige ce mémo d'une page maximum au DG de FinServ Québec à partir du cas retenu, en intégrant les 3 outils S01–S03 :  
> la fiche d'opportunité agentique, la grille de sélection et le canevas de cas d'usage.  
> Joignez ces outils en annexe (ne comptent pas dans la limite d'une page).  
> **Livraison :** chaque membre pousse ce fichier (PDF) dans son propre dépôt sous `portfolio/M2_memo_finserv.pdf`.

---

## En-tête du mémo

**À :** Directeur général, FinServ Québec  
**De :** CatherineM2002  
**Objet :** Recommandation de premier déploiement d'agent IA  
**Date :** 2026-06-08  
**Confidentialité** : Usage interne uniquement

---

## 1. Diagnostic — Rôle spécialisé recommandé

Nous recommandons de déployer un agent IA analyste du marché financier et du portefeuille client pour les 45 conseillers financiers de FinServ Québec. Cet assistant intelligent aidera les conseillers à offrir un service plus rapide, personnalisé et proactif sans remplacer la relation humaine avec les clients.

L’agent doit :
- résumer automatiquement les dossiers clients;
- analyser les portefeuilles et mouvements récents;
- suggérer des opportunités de suivi;
- préparer des notes de rencontre;
- générer des rappels et alertes;
- recommander des actions au conseiller;
- accélérer la préparation des rendez-vous.

L’objectif est d’augmenter la capacité et l’efficacité des conseillers pour qu’ils maintiennent une relation personnalisée malgré la pression concurrentielle. Ce choix est cohérent avec la culture de FinServ Québec, qui valorise la relation humaine avant la transaction et dont les conseillers craignent déjà “la machine”.

---

## 2. Solution recommandée

Nous recommandons une solution SaaS avec connecteur Salesforce natif, limitée aux 45 conseillers financiers pour réduire les frais de licence, améliorer la traçabilité et limiter la divulgation de données confidentielles.

Brex est privilégié car c’est une solution déjà conçue pour l’analyse financière, plus abordable et plus rapide à implanter que du sur mesure. Brex offre :
- accès restreints et rôles pour limiter l’usage aux conseillers autorisés;
- traces d’activité auditables pour la conformité;
- rapports structurés pour vérifier la cohérence et le devoir de diligence;
- intégration comptable pour documenter frais, flux et produits;
- contrôles d’accès et rôles adaptés à la Loi 25;
- engagements contractuels sur la sécurité et la confidentialité des données.

Si nécessaire, FinServ peut aussi considérer Microsoft Copilot for Financial Services comme solution alternative, mais l’option la plus réaliste reste Brex dans le contexte d’une équipe TI de seulement 8 personnes déjà à pleine capacité.

Au final, nous privilégions davantage Brex puisqu’il s’agit d’une solution plus abordable, plus rapide à implanter et mieux adaptée aux capacités actuelles de l’équipe TI de FinServ Québec, tout en permettant aux conseillers financiers de conserver un rôle central et humain dans la relation avec les clients.

---

## 3. Budget et ROI estimé

### Option 1 — Brex
- Coût de déploiement : 80 000 $ (configuration Salesforce, intégration CRM, sécurité, formation et pilote)
- Coût opérationnel annuel : 20 000 $ à 30 000 $

### Option 2 — Microsoft Copilot for Financial Services
- Coût de déploiement : 120 000 $ (configuration Salesforce/Microsoft, intégration CRM, sécurité, formation et pilote)
- Coût opérationnel annuel : 45 000 $ à 60 000 $

Ces deux solutions respectent l’enveloppe de 300 K$ prévue pour le premier projet IA.

ROI estimé à 12 mois :
- Hypothèse 1 : l’agent IA réduit la perte de clients de 50 %.
- Hypothèse 2 : chaque client conservé représente environ 4 000 $ de revenus annuels.

FinServ Québec perd actuellement entre 3 et 4 clients par semaine depuis avril 2026, soit environ 182 clients par année. En réduisant ces pertes de 50 %, l’entreprise pourrait conserver environ 80 clients sur 12 mois. À 4 000 $ de revenus annuels par client, cela représente environ 320 000 $ de revenus conservés.

Le projet pourrait donc permettre de conserver environ 320 000 $ de revenus annuels, tout en modernisant l’expérience des conseillers et en améliorant la rapidité des suivis clients.

---

## 4. Contraintes réglementaires adressées

La recommandation respecte les contraintes AMF et Loi 25 par les décisions de design suivantes :
- accès restreint aux 45 conseillers autorisés;
- authentification forte et revue des droits;
- supervision humaine obligatoire pour toute recommandation client;
- journalisation complète des actions et des accès;
- traitement des données sensibles dans des flux séparés;
- pseudonymisation/anonymisation des données envoyées au LLM.

Ne pas transmettre au LLM : nom du client, numéro de compte, IBAN, numéro de carte, adresse, téléphone, email, revenus précis, soldes exacts, historique de transactions détaillé et toute information nominative.

Le LLM doit recevoir des données anonymisées ou agrégées : synthèses de portefeuille, scores de risque, catégories d’actifs, tendances de marché et conclusions d’analyse sans éléments nominaux.

En pratique, on prépare des fiches clients non-personnifiées pour le LLM, on conserve les données sensibles séparément et le suivi humain vérifie que rien d’identifiable n’est injecté dans le modèle.

---

## 5. Plan de déploiement en 3 phases

| Phase | Contenu | Durée | Jalon de succès |
|-------|---------|-------|-----------------|
| Phase 1 — POC | Valider la faisabilité sur un échantillon de données financières et un petit groupe de conseillers | 2-4 semaines | Fiabilité des réponses ≥ 80 % lors des tests |
| Phase 2 — Pilote | Tests réels avec une dizaine de conseillers financiers pour vérifier la valeur ajoutée | 3 mois | Gain de temps de 3x sur la préparation de rendez-vous |
| Phase 3 — Déploiement | Déploiement à grande échelle pour les 45 conseillers, avec surveillance et plan de maintenance | 6 mois | Fiabilité des analyses financières ≥ 95 % |

---

## 6. Métriques de succès à 6 mois

| Type | Métrique | Valeur cible |
|------|----------|--------------|
| Technique | Précision des synthèses et analyses de portefeuille | ≥ 90 % |
| Affaires | Réduction du temps de préparation de rendez-vous | -30 % |
| Affaires | Nombre d’actions recommandées validées par un conseiller | ≥ 75 % |
| Conformité | Taux d’usage conforme aux règles AMF/Loi 25 | 100 % |
| Adoption | Pourcentage des conseillers utilisant l’outil au moins 3 fois/semaine | ≥ 70 % |

---

## 7. Clause go/no-go

Indicateur : pertinence des recommandations de l’agent par rapport à la situation client et capacité à proposer des actions utiles validées par le conseiller.  
Seuil d'arrêt : après 2 mois, si l’agent ne fournit pas des recommandations pertinentes dans au moins 80 % des cas testés.  
Date de décision : 2 mois après le démarrage du pilote.  
Action si seuil non atteint : pivoter vers un agent d’aide au conseiller qui consolide et anonymise les données client et fournit les informations de marché pertinentes pour accélérer l’analyse humaine, tout en conservant un support client humain.

---

## Annexes (hors limite d'une page)

- **Annexe A** : Fiche d'opportunité agentique (`portfolio/L1_reflexion_role_specialise.md`)  
- **Annexe B** : Grille de sélection d'agents (`portfolio/M1_grille_selection_agents.md` ou `.pdf`)  
- **Annexe C** : Canevas de cas d'usage (`portfolio/L3_canevas_cas_usage.md`)

---

*Divulgation IA : si des outils d'IA ont aidé à la rédaction de ce mémo, déclarez-les dans `ai-usage.md`.*
