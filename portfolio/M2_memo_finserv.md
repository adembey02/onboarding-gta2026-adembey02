# M2 — Mémo exécutif de recommandation IA

**Étudiant·e** : adembey02 
**Équipe** : Équipe FinServ IA —   Equipe 4  
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
**De :** adembey02 
**Objet :** Recommandation de premier déploiement d'agent IA  
**Date :** 2026-06-03 
**Confidentialité** : Usage interne uniquement

---

## 1. Diagnostic — Orchestration d'agents hybride humain-IA

**Contexte d'urgence :** FinServ Québec perd 3–4 clients par semaine depuis avril 2026 (~182/an), menaçant 320 K$ de revenus annuels. Les 45 conseillers sont débordés par la charge opérationnelle (synthèse manuelle, alertes manuelles, analyses lentes) et manquent de temps pour la relation proactive. Les conseillers craignent une automatisation aveugle (« black box IA ») qui risquerait de perturber la relation client.

**Diagnostic :** Le vrai besoin n'est pas un agent unique, mais une **orchestration de 5 agents modulaires avec 3 points de supervision humaine obligatoires** :
1. Agent Sécurité (anonymisation Loi 25)
2. Agent Agrégation (consolidation données) + *Validation humaine #1*
3. Agent Analyse (ratios, risques)
4. Agent Recommandations (actions) + *Validation humaine #2*
5. Agent Synthèse (messages clients) + *Validation humaine #3*

Cette orchestration adresse directement :
- **Confiance conseiller** : 3 points où l'humain reprend le contrôle explicitement
- **Conformité** : chaque agent a un rôle de sécurité/audit clair
- **Apprentissage** : l'agent s'adapte aux préférences du conseiller au fil du temps (Agent 6)

**Objectif :** Augmenter de 3x la productivité des rendez-vous préparés, tout en renforçant la relation humaine — le conseiller devient « pilote assisté » plutôt que « remplacé ».

---

## 2. Solution recommandée — Orchestration modulaire avec supervision humaine intégrée

**Architecture :** Infrastructure personnalisée légère (orchestration interne) plutôt que SaaS monolithique. Pourquoi ? Les solutions clés en main (Brex, Copilot) offrent peu de contrôle sur les étapes intermédiaires — le conseiller ne peut pas intervenir entre analyse et recommandation.

**Composantes principales :**

1. **Socle technique** : API Salesforce (CRM existant) + orchestration agents (workflow engine léger) + LLM sécurisé (Claude, GPT via API sécurisée)

2. **Les 5 agents orchestrés :**
   - Agent 1 (Sécurité) : scrubber de données → anonymisation Loi 25/AMF automatique
   - Agent 2 (Agrégation) : consolidation données multiples sources + tendances marché → **Validation humaine #1**
   - Agent 3 (Analyse) : calculs financiers, ratios, stress-tests
   - Agent 4 (Recommandations) : propose 2–4 actions → **Validation humaine #2**
   - Agent 5 (Synthèse) : génère note client, alerte → **Validation humaine #3**

3. **Points de supervision humaine :** Intégrés dans le workflow — pas d'étapes optionnelles. Le conseiller arbitre explicitement à chaque carrefour critique.

4. **Infrastructure de sécurité :**
   - Journalisation complète par agent (qui valide quoi, quand, pourquoi)
   - Pseudonymisation + historique séparé des données sensibles
   - Authentification forte (SSO Salesforce existant)
   - Audit trail automatique pour AMF/Loi 25

**Avantages sur Brex/Copilot :**
- Contrôle granulaire du workflow → confiance conseiller +50%
- Coût opérationnel réduit (pas de licence par user, API tiering)
- Adaptabilité pour apprentissage continu (Agent 6) sans reconfiguration SaaS
- Équipe TI 8 personnes peut maintenir (architecture modulaire, pas d'intégration massive)

---

## 3. Budget et ROI estimé

### Option recommandée — Orchestration modulaire interne

**Coûts de déploiement (12 mois):**
- Infrastructure & orchestration : 60 000 $ (workflow engine, API sécurisation, infrastructure cloud léger)
- Développement agents (5 agents) : 70 000 $ (intégration Salesforce, LLM API, tests conformité)
- Formation & change management : 20 000 $ (ateliers conseillers, documentation, support pilote)
- **Total déploiement : 150 000 $**

**Coûts opérationnel annuel (steady state):**
- Infrastructure cloud & API LLM : 12 000 $ à 18 000 $
- Maintenance agents & monitoring : 8 000 $ à 12 000 $
- Support utilisateurs & évolutions : 5 000 $ à 8 000 $
- **Total annuel : 25 000 $ à 38 000 $ (vs 45–90 K$ pour SaaS)**

**Budget total pour 300 K$ : ✓ RESPECTE l'enveloppe** (150 K+ 2 ans ops = 213 K$ = 71 % de 300 K$)

---

### ROI estimé à 12 mois

**Scénario conservateur :**
- Hypothèse 1 : orchestration réduit la perte de clients de 50 % → conserve ~80 clients/an
- Hypothèse 2 : chaque client conservé = 4 000 $ revenus/an → **320 000 $ revenus conservés**
- Hypothèse 3 : gain de productivité conseiller = 3x plus de rendez-vous préparés → +2–3 clients supplémentaires par conseiller par an → **+90 K$ revenus additionnels** (hypothèse conservative : 45 conseillers × 2 clients × 1 000 $ avg)

**Bénéfices additionnels (non monétisés mais critiques) :**
- Réduction du turn-over conseiller (80 % des départs cités : peur « machine », charge opérationnelle)
- Amélioration satisfaction conseiller : orchestration = partenaire, pas menace
- Capacité TI : infrastructure modulaire = évolutive sans refonte coûteuse

**ROI calculé :**
- Revenus conservés + additionnels : 410 000 $ (année 1)
- Coûts déploiement + ops : 150 K + 30 K = 180 K$ (année 1)
- **ROI brut : 230 K$ (128 % rendement année 1)**
- **Payback period : 5–6 mois** (après ramp-up pilote)

---

## 4. Conformité AMF & Loi 25 — Intégrée par agent

**Architecture de conformité :** Chaque agent a des responsabilités explicites d'audit et de conformité (pas de « délégation globale »).

**Agent 1 — Sécurité & Anonymisation (point 0 de contrôle)**
- Obligation : scrubber automatique de toutes les données nominatives avant transmission aux agents suivants
- Sortie certifiée : données anonymisées + hash de vérification
- Audit trail : journalisation de ce qui a été retiré (metadata sans données sensibles)
- Conformité : satisfait Loi 25 art. 3–5 (données sensibles isolées)

**Agent 2 — Agrégation + Validation humaine #1**
- Obligation du conseiller : vérifier que les données ne contiennent aucun PII (personally identifiable information)
- Trail : signature du conseiller attestant que synthèse est conforme
- Conformité : satisfait AMF 2025 sur « supervision humaine obligatoire avant transmission LLM »

**Agent 4 — Recommandations + Validation humaine #2**
- Obligation du conseiller : approuver avant transmission client (= « recommandation personnalisée supervisée »)
- Trail : signature + motif acceptation/rejet + timestamp
- Conformité : satisfait devoir de diligence AMF art. 328–2

**Agent 5 — Synthèse + Validation humaine #3**
- Obligation du conseiller : approuver ton/contenu avant envoi client
- Trail : version finale signée = preuve de diligence raisonnable
- Conformité : satisfait AMF sur traçabilité des communications client

**Données interdites au LLM :** nom, IBAN, numéro compte, carte bancaire, adresse, téléphone, email, revenus exacts, soldes exacts, historique transactions détaillé, identité du client.

**Données autorisées (anonymisées/agrégées) :** portefeuille par catégorie (% actions/obligations/liquidités), solde total de période (sans détail), scores de risque (1–5), tendances (pct %/an), alertes de marché (indices publics), conclusions d'analyse (sans nominatif).

**Contrôles techniques :**
- Chiffrement des données client en transit et au repos (TLS 1.3, AES-256)
- Logs d'accès signés par agent avec timestamps
- Alertes anomalies : si données sensibles détectées en input LLM → blocage + escalade IT
- Audit annuel (externe) obligatoire sur 100 % des transactions orchestration

---

## 5. Plan de déploiement en 4 phases

| Phase | Contenu | Durée | Jalon de succès | KPI de go/no-go |
|---|---|---|---|---|
| **Phase 1 — POC** | Agent 1 (Sécurité) + Agent 2 (Agrégation) sur 50 clients de test en sandbox. Valider anonymisation, validation humaine #1 workflow. | 3 semaines | Agent 1 scrubber = 100 % données sensibles supprimées. Conseiller valide en <2 min moyenne. | Zéro fuite data. Validation humaine 100 % compliance. |
| **Phase 2A — Pilote Agents** | Agents 1–5 (chaîne complète) testés avec 5 conseillers (20 clients réels/conseiller = 100 clients live). Mesurer validations #1, #2, #3. | 4 semaines | Taux validation humaine ≥ 90 %. Temps orchestration end-to-end <10 min. Recommandations pertinentes ≥ 75 %. | Si <70 % pertinence → fix Agent 3/4 logique. Si >10 min → optimiser infrastructure. |
| **Phase 2B — Pilote Échelle** | Expansion à 10 conseillers (200 clients live). Mesurer adoption, gain de temps, taux d'action conseiller. | 8 semaines | Gain de temps ≥ 2x sur rendez-vous préparés. Taux usage conseiller ≥ 60 % (min 2 rendez-vous/sem avec orch). | Si <60 % usage → revoir UX/formation. Si <2x gain temps → reprioriser agents. |
| **Phase 3 — Déploiement complet** | 45 conseillers, tous les agents. Activation Agent 6 (apprentissage continu) pour adaptation progressif par conseiller. | 6–8 semaines | Fiabilité analyses ≥ 95 %. Taux validation #1/#2/#3 ≥ 90 %. Confiance conseiller ≥ 80 % (survey). Adoption ≥ 80 % (3x/sem). | Surveillance 24/7. Plan rollback par agent si incident. |

---

## 6. Métriques de succès à 6 mois

| Catégorie | Métrique | Cible | Responsable |
|---|---|---|---|
| **Technique — Agents** | Fiabilité Agent 1 (anonymisation) : zéro donnée sensible passée aval | 100 % | IT |
| | Fiabilité Agent 2 (agrégation) : synthèse reflète réalité CRM | ≥ 95 % | IT + Conseiller |
| | Fiabilité Agent 3 (analyse) : ratios/risk scores validés vs. calcul manuel | ≥ 90 % | Analyste financier |
| **Affaires — Workflow** | Temps orchestration complet (données → synthèse) | <10 min/client | IT |
| | Temps validation humaine #1 (agrégation) : acceptation/rejet | <2 min avg | Conseiller |
| | Temps validation humaine #2 (recommandations) : arbitrage | <5 min avg | Conseiller |
| | Temps validation humaine #3 (synthèse) : approbation | <2 min avg | Conseiller |
| **Affaires — Productivité** | Gain de temps préparation rendez-vous | ≥ 3x (vs. manuel) | Conseiller |
| | Rendez-vous préparés par conseiller par semaine (avant : 8–10) | +15 à 20 | Manager |
| | Nombre d'opportunités détectées per conseiller per month | +5–10 | Conseiller |
| **Conformité** | Taux d'actions recommandées validées par conseiller avant client | ≥ 90 % | Compliance |
| | Taux d'usage conforme AMF/Loi 25 (audit trail, anonymisation) | 100 % | Compliance |
| | Incidents de sécurité ou fuite data | 0 | IT |
| **Adoption & Confiance** | Taux conseiller utilisant orchestration ≥ 3 fois/sem | ≥ 80 % | Manager |
| | Confiance conseiller envers orchestration (survey 1–5) | ≥ 4.0 | Manager |
| | NPS conseiller (question: « L'orch m'aide vraiment ») | ≥ 7/10 | Manager |
| **Apprentissage (Agent 6)** | Taux acceptation recommandations trending (by conseiller) | +10 % mois 4→6 | IT |
| | Variance taux acceptation entre conseillers (doit baisser) | <15 % | IT |

---

## 7. Clause go/no-go — Points de décision par phase

**Après Phase 1 (POC, semaine 3) :**
- **Critères GO :** Agent 1 = 100 % anonymisation. Validation #1 workflow opérationnel. Zéro incident sécurité.
- **Critères NO-GO :** Si fuite data trouvée OU validation #1 >3 min avg OU agents ne communiquent pas.
- **Action NO-GO :** Réviser architecture agents avant Phase 2A.

**Après Phase 2A (pilote agents, semaine 7) :**
- **Critères GO :** Taux validation #1/#2/#3 ≥ 90 %. Recommandations pertinentes ≥ 75 % (validées par conseiller). Orch end-to-end <10 min.
- **Critères NO-GO :** Si pertinence <70 % OU validation <85 % OU temps >12 min OU confiance conseiller <3/5.
- **Action NO-GO :** Arrêter Phase 2B, reformuler logique Agent 3/4 ou revoir prompt LLM. Ré-évaluer semaine 9.

**Après Phase 2B (pilote échelle, semaine 15) :**
- **Critères GO :** Gain temps ≥ 2x mesurable. Taux usage ≥ 60 % (2+ rendez-vous/sem avec orch). Confiance conseiller ≥ 3.5/5. Adoption >50 %.
- **Critères NO-GO :** Si gain temps <1.5x OU usage <40 % OU incidents conformité detectés OU confiance conseiller <3/5.
- **Action NO-GO :** Pivoter vers « Agent Aide Conseiller simplifié » (Agents 1–2 uniquement : anonymisation + agrégation) sans recommandations automatiques. Validation humaine remplacée par « export pour analyse conseiller ». Réduire coût opérationnel, augmenter sécurité, ré-évaluer ROI.

**Date décision finale :** Fin semaine 15 (avant Phase 3 déploiement complet).

**Escalade en cas NO-GO :** Directeur Général + CTO FinServ + Responsable Conformité. Réviser architecture vs. contraintes TI (8 personnes). Considérer SaaS partenaire (Brex, Copilot) comme fallback si orchestration interne non viable.

---

## 8. Orchestration d'agents — Amélioration de la solution d'équipe

### 8.1 Faiblesses de la version équipe corrigées

**Faiblesse 1 : Solution SaaS monolithique sans chaîne logique adaptée au workflow**
- Problème : Brex proposé en équipe fonctionne « en boîte noire » — le conseiller ne contrôle pas les étapes critiques.
- Correction : Orchestration modulaire où chaque étape (sécurité → agrégation → analyse → recommandations → synthèse) est explicite et supervisée.

**Faiblesse 2 : Absence de supervision humaine granulaire**
- Problème : La confiance des conseillers envers « la machine » est faible — validation unique en fin de chaîne insuffisante.
- Correction : 3 points de contrôle humain intégrés *dans* la chaîne (validation données, arbitrage recommandations, approbation message) pour maintenir la relation humaine.

**Faiblesse 3 : Pas d'apprentissage des préférences du conseiller**
- Problème : L'agent propose les mêmes analyses pour tous les conseillers et tous les clients — pas d'adaptation.
- Correction : Chaque conseiller gère un historique des décisions acceptées/rejetées pour affiner les futures recommandations.

---

### 8.2 Séquence d'agents — Orchestration recommandée

Le workflow suit 5 agents en chaîne avec 3 points de validation humaine :

```
[Client Data] → [Agent 1: Sécurité] → [Agent 2: Agrégation] 
                                          ↓ (VALIDATION HUMAINE #1)
[Agent 3: Analyse Financière] → [Agent 4: Recommandations]
                                          ↓ (VALIDATION HUMAINE #2)
[Agent 5: Synthèse] → [Note/Alerte pour Conseiller]
                                          ↓ (VALIDATION HUMAINE #3)
[Action Client]
```

**Agent 1 — Sécurité & Conformité (Loi 25 / AMF)**
- Entrée : fichier client brut de Salesforce
- Fonction : Scrubber de données — supprime noms, IBANs, numéros de carte, adresses personnelles
- Sortie : données anonymisées structurées (portefeuille, solde agrégé, tendances, risque)
- Responsabilité : garantir qu'aucune donnée sensible ne passe aux agents suivants

**Agent 2 — Agrégation de Données**
- Entrée : données anonymisées de l'Agent 1
- Fonction : consolide les données de multiples sources CRM, complète avec tendances de marché du jour
- Sortie : synthèse structurée (portefeuille consolidé, % actifs, score volatilité, alertes de marché pertinentes)
- **Validation humaine #1** : Le conseiller vérifie que la synthèse est exacte avant d'aller plus loin
  - *Cas d'arbitrage* : « Vous avez oublié la nouvelle obligation émise hier par la Banque Mondiale » → le conseiller ajoute manuellement
  - *Cas de correction* : « Le portefeuille est mal classifié en risque élevé (c'est moyen) » → conseiller corrige avant d'aller à l'analyse

**Agent 3 — Analyse Financière**
- Entrée : synthèse validée par humain
- Fonction : calcule ratios, risques, opportunités de rééquilibrage, analyse durée/convexité, stress-tests
- Sortie : 3-5 insights clés + alertes de dégradation/amélioration potentielle
- Responsabilité : analyse objective, impartiale

**Agent 4 — Recommandations Proactives**
- Entrée : insights de l'Agent 3
- Fonction : propose 2-4 actions concrètes pour le conseiller (vendre X, acheter Y, rééquilibrer Z)
- Sortie : liste d'actions rangées par impact potentiel et risque
- **Validation humaine #2** : Le conseiller arbitre et priorise
  - *Cas d'arbitrage* : « L'Agent propose de vendre les obligations, mais je sais que ce client est averse au risque — je vais plutôt proposer un fonds défensif » → conseiller choisit action alternative
  - *Cas de correction* : « L'Agent ne connaît pas que j'ai eu une conversation la semaine passée avec le client sur ce sujet » → conseiller invalide cette action pour cette période

**Agent 5 — Synthèse Exécutive**
- Entrée : actions validées par conseiller + contexte client
- Fonction : rédige note de meeting, génère alerte client, structure le brief préparatoire
- Sortie : document prêt pour échange client
- **Validation humaine #3** : Conseiller approuve ou modifie le ton/message
  - *Cas de correction* : « Changez 'obligation dégradée' par 'obligation à surveiller' — c'est moins alarmant » → conseiller édite
  - *Cas d'arbitrage* : « Mettez l'accent sur la croissance plutôt que le risque dans la conclusion » → Agent rédige variante

---

### 8.3 Trois moments clés de l'humain dans la boucle — Avec corrections d'arbitrage

**Moment 1 — Validation des données (avant analyse)**
- *Qui* : Conseiller FinServ
- *Quoi* : Vérifie que la synthèse d'agrégation reflète correctement la réalité client
- *Correction type* : 
  - **Rejet** : « Ce client a reçu un héritage en mars — vous n'avez pas capté le flux de +250k€ » → L'Agent 2 se corrige ; analyse peut reprendre
  - **Arbitrage** : « Vous classifiez en risque moyen, mais lui est très conservateur depuis la crise 2008 » → Conseiller ajuste paramètre de risque avant d'aller à l'analyse

**Moment 2 — Arbitrage des recommandations (avant synthèse)**
- *Qui* : Conseiller FinServ
- *Quoi* : Choisit parmi les actions proposées celles qui conviennent vraiment au client et son contexte
- *Correction type* :
  - **Correction** : « L'Agent propose achat fonds tech, mais le client m'a dit 'jamais tech, ça me stresse'. » → Conseiller élimine, demande alternative (ex : fonds indices monde large)
  - **Arbitrage** : « Je peux proposer 2 actions sur 4 cette semaine — client peut être overwhelmé sinon » → Conseiller priorise et repousse les 2 autres au prochain cycle

**Moment 3 — Approbation du message avant envoi au client**
- *Qui* : Conseiller FinServ
- *Quoi* : Valide que la note/message synthétisé prend le bon ton, contexte correct, n'omet aucune nuance
- *Correction type* :
  - **Correction** : Note trop technique → Conseiller reformule en langage client-friendly
  - **Arbitrage** : « Vous recommandez achat, mais je vais l'annoncer comme 'opportunité à discuter ensemble' plutôt que 'action à faire' » → Conseiller ajuste niveau d'engagement

---

### 8.4 Angle créatif — Boucle d'apprentissage et feedback humain

**L'IA seule n'aurait pas pensé à :**

Intégrer un **Agent 6 — Apprentissage Continu** qui capte après chaque interaction :
- Quelles recommandations l'Agent 4 a proposé
- Quelles actions le conseiller a finalement choisies (acceptées/rejetées)
- Quel a été le résultat (client satisfait, action réussie, etc.)

Cet Agent 6 crée un historique par profil de conseiller et par type de client, permettant aux Agents 3–4 d'adapter leurs analyses futures :
- Le conseiller Jean préfère toujours les obligations court terme + fonds défensifs → Agent 3 remonte ces catégories en priorité pour les clients de Jean
- Les clients de la Banque X font 80% portefeuille actions → Agent 4 propose rééquilibrages moins radicaux pour les clients du secteur X

**Valeur humaine ajoutée :**
- Le conseiller ne doit pas « casser » l'Agent à chaque fois — l'Agent apprend ses préférences et contexte avec le temps
- L'Agent devient partenaire personnalisé, pas consultant générique
- Cela crée une **relation de confiance progressive** — « l'IA me connaît et m'aide vraiment » vs. « l'IA me ralentit »

---

## Annexes (hors limite d'une page)

- **Annexe A** : Fiche d'opportunité agentique (`portfolio/L1_reflexion_role_specialise.md`)  
- **Annexe B** : Grille de sélection d'agents (`portfolio/M1_grille_selection_agents.md` ou `.pdf`)  
- **Annexe C** : Canevas de cas d'usage (`portfolio/L3_canevas_cas_usage.md`)

---

*Divulgation IA : si des outils d'IA ont aidé à la rédaction de ce mémo, déclarez-les dans `ai-usage.md`.*
