# Divulgation d'usage de l'IA — ai-usage.md

> Remplissez ce fichier pour chaque milestone avant de soumettre.
> Si aucun outil IA n'a été utilisé, écrivez « Aucun » dans chaque section et signez.
> **Obligatoire même en cas d'absence d'usage.**
>
> Pour mettre à jour : cliquez sur ce fichier dans GitHub, puis sur l'icône crayon ✏️.

---

## 1. Outil utilisé

Outil : Claude (Anthropic)
Version / date d'accès : Claude 3.5 / juin 2026

Outil : ChatGPT (OpenAI)
Version / date d'accès : GPT-4o / juin 2026

---

## 2. Ce qu'il m'a aidé à faire

**Claude :**
- **Section 1 (Diagnostic)** : Reformuler le diagnostic en contexte d'urgence + orchestration (au lieu de solution unique)
- **Sections 2-7** : Enrichir chaque section avec profondeur logique : solution modulaire vs SaaS, budget détaillé (150 K+ ops), ROI 128%, conformité granulaire par agent, plan 4 phases avec KPI go/no-go, métriques par responsable
- **Section 8 (Orchestration)** : Structurer les 5 agents en chaîne, 3 points de contrôle humain, faiblesses équipe corrigées, angle créatif Agent 6

**ChatGPT :**
- Clarifier les 2-3 faiblesses majeures de la solution Brex en équipe et proposer des corrections dans chaque section
- Générer des exemples concrets d'arbitrage et correction à chaque étape du workflow
- Vérifier la cohérence du workflow avec la conformité AMF et Loi 25 (anonymisation, audit trail, supervision humaine)
- Raffiner les formulations de ROI (128 %) et les arguments d'avantages orchestration vs. SaaS (coût, flexibilité, confiance)

---

## 3. Sources et chiffres que j'ai vérifiés moi-même

- **Contexte d'urgence (section 1)** : Les chiffres de perte de clients (3-4/semaine depuis avril 2026 = ~182/an) viennent directement du diagnostic présenté en S03 — j'ai croisé avec le DG et les managers.
- **Conformité AMF & Loi 25** : J'ai consulté le guide AMF 2025 sur l'usage de l'IA en gestion de portefeuille ; confirmé que l'anonymisation des données sensibles est obligatoire avant traitement par LLM (sections 4-5).
- **ROI & Budget (section 3)** : Les hypothèses de revenus par client conservé (4 000 $/an) et gain de productivité (3x) viennent de données internes FinServ (historique acquisition/retention). J'ai validé auprès du contrôleur.
- **Capacité TI (section 2-5)** : Confirmé que l'équipe TI compte 8 personnes à pleine capacité — explique pourquoi orchestration interne est plus viable que SaaS complexe.
- **Processus conseiller** : Les 5 étapes du workflow (sécurité → agrégation → analyse → recommandations → synthèse) reflètent mon expérience directe de 3 mois d'accompagnement des conseillers sur le terrain.

---

## 4. Ce que j'ai modifié ou rejeté

**Rejeté :**
- La première proposition était SaaS Brex monolithique (comme en équipe) — j'ai pivoté vers orchestration interne pour garder le contrôle et la confiance conseiller
- L'IA proposait 8 agents parallèles — simplifié à 5 agents séquentiels pour respecter la capacité TI (8 personnes) et la maintenabilité
- L'IA proposait des validations humaines "optionnelles" — j'ai rendu les 3 points de contrôle *obligatoires* pour adresser directement la crainte des conseillers

**Modifié :**
- Les sections 1–7 : l'IA avait une structure classique (diagnostic générique, ROI théorique). J'ai enrichi chaque section avec contexte urgence, arguments compétitifs, go/no-go décisionnels concrets
- Les exemples d'arbitrage initiaux étaient trop théoriques — j'ai ajouté des dialogues réalistes et des nuances client (ex : « obligation dégradée » → « obligation à surveiller » pour le contexte psychologique)
- Plan de déploiement : passé de 3 phases génériques à 4 phases avec jalons concrets et critères de décision mesurables (taux validation ≥ 90 %, temps <10 min, etc.)
- Métriques (section 6) : ajouté responsabilités par rôle (IT, Conseiller, Compliance, Manager) pour clarté d'exécution

**Ajouté (ma contribution personnelle) :**
- L'angle créatif Agent 6 (apprentissage continu par conseiller) n'a pas été proposé par l'IA d'emblée — insight développée après discussion avec Jean (conseiller senior) sur la frustration de répéter les mêmes ajustements mois après mois
- Architecture de conformité granulaire (section 4) : chaque agent a des responsabilités explicites d'audit (pas délégation globale)
- Clause go/no-go par phase (section 7) : point de décision après chaque palier, avec action de fallback (pivot vers solution simplifiée si orchestration échoue)

---

## 5. Déclaration de responsabilité

Je déclare que le contenu final reflète mon jugement personnel et mon expérience terrain à FinServ Québec.

Les outils IA m'ont aidé à structurer, clarifier, et raffiner — mais les décisions de design majeures reflètent ma connaissance du contexte :
- Passage SaaS → orchestration interne : basé sur capacité TI réelle et peurs conseillers observées
- 3 points de contrôle humain obligatoires : basé sur discussions directes avec conseillers sur confiance/menace
- Agent 6 apprentissage : feedback de conseillers seniors sur adaptation dynamique
- Go/no-go décisionnel : expérience de projets TI chez FinServ et pivot-plans

Je suis responsable de l'exactitude factuelle (chiffres vérifiés), de la pertinence (contexte FinServ adressé), et du raisonnement (orchestration mieux adaptée que SaaS pour ce cas).

Nom : adembey02
Date : 2026-06-10
