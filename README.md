# aiqa-starter-kit

**Cadre modulaire pour l’implémentation de stratégies de test intelligentes pilotées par IA — orienté métier, scalable, et interopérable.**

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

```markdown
aiqa-starter-kit/
├── features/              # Scénarios Gherkin métier
├── tests/                 # Tests générés en TypeScript (.spec.ts)
├── pages/                 # Page Object Models
├── utils/                 # Fonctions utilitaires (waits, assertions)
├── test-data/             # Données de test externes (JSON, CSV)
├── scripts/
│   └── send_to_IA.sh      # Envoi d'un besoin métier vers le moteur IA
├── docs/                  # Documentation et guides d'intégration
├── ci/                    # Pipelines CI (GitHub Actions, GitLab...)
├── playwright.config.ts   # Configuration d'exécution locale
└── README.md              # Présent document


## Workflow opérationnel

1. **Rédaction d’un besoin fonctionnel**  
   Le QA exprime le besoin sous forme de scénario Gherkin ou en langage naturel.

2. **Transmission vers le moteur IA**  
   Le script `send_to_IA.sh` envoie ce besoin à une API privée sécurisée.

3. **Réception des fichiers générés** :
   - Fichier `.spec.ts` prêt à être exécuté, structuré selon le modèle POM
   - Composants complémentaires éventuels : données, page models, fixtures

4. **Exécution dans la chaîne CI/CD**  
   Intégration dans le pipeline existant, avec vérification du résultat.

> ⚠️ La logique IA de génération est totalement déportée. Ce dépôt ne contient aucun code IA ni modèle intégré.

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

**Contact technique :** [gammoudi.khaled@outlook.fr](mailto:gammoudi.khaled@outlook.fr)
