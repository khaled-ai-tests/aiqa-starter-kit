# aiqa-starter-kit

**Cadre modulaire pour l’implémentation de stratégies de test pilotées par IA — orienté métier, scalable, et interopérable.**

---

## Objectif

Ce dépôt constitue un point d’entrée structurant pour les professionnels du test logiciel souhaitant initier une approche IA-driven, sans exposer la logique algorithmique sous-jacente.

Il est conçu pour répondre aux exigences des rôles suivants :

- Quality Engineers, SDET, Test Architects
- Équipes QA avancées en contexte CI/CD
- Évaluateurs techniques ou pilotes d’intégration IA

Le starter permet de :

- Écrire ou recevoir des scénarios Gherkin exprimant un besoin métier
- Générer automatiquement des scripts de test maintenables à l’aide d’un moteur IA privé (non inclus ici)
- Exécuter ces scripts dans un cadre POM avec Playwright
- Étendre le système vers d’autres contextes (mobile, API, BDD)

---

## Structure du dépôt

```text
aiqa-starter-kit/
├── features/               # ✅ Scénarios Gherkin générés
├── pages/                  # ✅ Page Object Models (Playwright)
├── tests/                  # ✅ Tests UI E2E (.spec.ts)
├── api-tests/              # ✅ Tests d'API générés (.spec.ts)
├── utils/                  # ✅ Fonctions partagées (web + API)
├── test-data/              # ✅ Données de test JSON, CSV
├── recorder/               # 🔄 Nouveau : captures UI/API (DOM, screenshots, events)
│   ├── traces/             # Sessions QA enrichies (JSON)
│   └── raw/                # Screenshots, snapshots DOM (si activé)
├── scripts/                # ⚙️ Utilitaires manuels
│   └── send_to_IA.sh       # Bridge vers moteur IA
├── docs/                   # 💤 (à laisser vide ou minimal, formation plus tard)
├── ci/                     # ✅ GitHub Actions, GitLab, etc.
├── ai-meta/                # 🔒 Orchestration IA (non livré)
│   ├── prompts/            # Prompts structurés
│   ├── mappings/           # Mappings DOM ↔ intentions
│   └── sessions/           # Exemple de dialogues / traitement
├── playwright.config.ts    # ✅ Config locale
└── README.md               # Intro minimale

```

## Workflow opérationnel

1. **Expression du besoin fonctionnel**  
   Le consultant QA décrit un comportement attendu via un scénario Gherkin ou une instruction en langage naturel.

2. **Envoi au moteur IA**  
   Le script `send_to_IA.sh` transmet cette expression métier à une API privée hébergeant le moteur IA.

3. **Génération automatisée**  
   Le moteur IA retourne un ensemble de fichiers prêts à l’emploi :  
   &nbsp;&nbsp;&nbsp;&nbsp;- Un fichier `.spec.ts` structuré selon le modèle POM  
   &nbsp;&nbsp;&nbsp;&nbsp;- Des composants complémentaires si nécessaire (data sets, page models, fixtures)

4. **Intégration et exécution**  
   Les tests générés peuvent être validés, modifiés puis intégrés dans une chaîne CI/CD pour exécution automatisée.

> Le moteur IA n’est pas inclus dans ce dépôt. Aucune logique de génération ou d’orchestration n’est exposée.

---

## Accès restreint

L’ensemble des composants intelligents (LLM orchestration, validation, auto-réécriture...) est **hébergé en privé**.

- L’accès nécessite une souscription validée via notre plateforme : [https://aiqa.dev](https://aiqa.dev)
- Voir [LICENSE](./LICENSE.md) pour les conditions d’utilisation et les restrictions juridiques

---

## Perspectives d’évolution

Ce starter s’inscrit dans une vision long terme orientée produit SaaS. Les axes d’évolution incluent :

- Support multi-runner (UI, API, mobile, BDD)
- Intégration avec des outils TMS (Jira, Xray, Zephyr)
- Interface no-code pour la génération assistée
- Apprentissage progressif basé sur les résultats de tests
- Orchestration IA par domaine fonctionnel ou projet

---

## Support & communauté

Les utilisateurs disposant d’un accès validé bénéficient de :

- Un espace d’échange dédié (serveur Discord sécurisé)
- Mises à jour incrémentales (scripts ou portail)
- Documentation continue pour intégration dans les workflows QA

**Contact technique :** [gammoudi.khaled@outlook.fr]
