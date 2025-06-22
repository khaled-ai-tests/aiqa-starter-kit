# aiqa-starter-kit

**Base modulaire pour l’automatisation de tests — orientée métier, maintenable, extensible, et conçue pour l’intégration d’un moteur IA privé.**

---

## Objectif

Ce dépôt sert de **cadre public standardisé** pour l’intégration d’un moteur IA privé générateur de tests.

Il permet de :

- Centraliser des scénarios métier au format Gherkin
- Générer automatiquement des tests UI/API à partir de besoins fonctionnels
- Structurer l’automatisation via Playwright + POM
- Exécuter ces tests dans un environnement CI/CD

> Le moteur IA n’est pas inclus. Aucune logique interne n’est exposée.

---

## 📁 Structure du projet

```text
aiqa-starter-kit/
├── features/           # Scénarios Gherkin métier
├── pages/              # Page Object Models (TypeScript)
├── tests/              # Tests E2E Playwright (UI)
├── api-tests/          # Tests d'API REST, GraphQL, etc.
├── utils/              # Fonctions partagées web/API
├── test-data/          # Données de test (JSON, CSV)
├── recorder/           # Captures UI/API enrichies (DOM, events)
│   ├── traces/         # Traces IA (format enrichi)
│   └── raw/            # Screenshots, DOM snapshots
├── scripts/            # Scripts utilitaires
│   └── send_to_IA.sh   # Envoi vers moteur IA (bridge privé)
├── ci/                 # Pipelines CI (GitHub Actions, GitLab...)
├── ai-meta/            # Prompts IA, mapping DOM, sessions (non livré)
├── playwright.config.ts # Configuration locale Playwright
└── README.md           # Présent document

```

## Workflow opérationnel

1. **Formalisation du besoin fonctionnel**  
   Le consultant QA rédige un scénario Gherkin ou une instruction métier exprimant l’action utilisateur attendue.

2. **Génération de code automatisée**  
   Le moteur IA retourne un ou plusieurs fichiers exploitables, notamment :
   Un fichier .spec.ts conforme au modèle POM
   Des modèles de page, données de test ou utilitaires si nécessaires

4. **Intégration dans le projet**  
   Les fichiers générés sont ajoutés au dépôt, validés localement et intégrés dans la chaîne CI pour exécution automatisée.

> Le moteur IA n’est pas inclus dans ce dépôt. Aucune logique de génération ou d’orchestration n’est exposée.

---

## Licence

Ce dépôt est distribué sous licence MIT, sauf indication contraire.
Toutefois :

Le moteur IA, les prompts et l’orchestration ne sont pas inclus.

Aucune réutilisation commerciale du moteur IA privé n’est autorisée sans accord explicite.

Les contributions externes au starter-kit sont les bienvenues, dans le respect du périmètre visible.

Voir le fichier LICENSE pour les détails complets.

---


**Contact technique :**:[gammoudi.khaled@outlook.fr]
