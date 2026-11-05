# Base de connaissance

**Indicateurs sur les populations étudiantes et diplômées — Polytech Lyon**

Ce projet tutoré vise à faciliter le calcul des indicateurs et la préparation des formulaires demandés aux services de l’école. Le premier périmètre concerne l’insertion des diplômés. La mobilité internationale et la réussite viennent ensuite.

## Équipe

| Membre | Responsabilité |
|---|---|
| Flavien BONTEMPS | Chef de projet : cadrage, comptes rendus, planning, suivi APC ; hébergement et procédure de démonstration avec Ahdi |
| Ahdi BENMAOUIA | Architecture, import et contrôles, comptes et droits par service ; intégration |
| Abderrahim BEN MOHA | Modèle de données, correspondances, développement du moteur configurable ; calcul manuel des valeurs attendues |
| Louka PESIC | Maquettes et développement de la consultation, des filtres, de la génération et de l’export du formulaire |
| Rayen BENAMMAR | Données fictives, tests automatisés, exécution et suivi des écarts, guides |

Rôles confirmés par Flavien, chef de projet ; lots précisés le **6 novembre 2026**. Chaque livrable sera relu par un autre membre. La cliente validera les règles métier.

## Documents

- [Cahier des charges partagé, version du 6 novembre](https://docs.google.com/document/d/1oyuepsKSqtQUYQNIi3GD1bW9C46xIw8h7-YmlZXqtaA/edit).
- [Cadrage](docs/cadrage.md) et [planning](docs/planning.md).
- [Catalogue des indicateurs](docs/catalogue_indicateurs.md), [dictionnaire](docs/dictionnaire_initial.md) et [points sur les fichiers](docs/audit_sources.md).
- [Conception technique](docs/architecture.md), [parcours utilisateurs](docs/parcours_utilisateurs.md) et [formulaires](docs/formulaires.md).
- [Tests prévus](docs/plan_recette.md), [guide utilisateur](docs/guide_utilisateur.md) et [ajout d’un indicateur](docs/ajouter_indicateur.md).
- [Décisions](docs/decisions.md) et [contributions](CONTRIBUTING.md).

## Organisation

[Trello](https://trello.com/b/N3q0qeqB) suit les tâches et leurs responsables. **État au 6 novembre : documents de cadrage publiés ; application et tests exécutables à réaliser.** Le dépôt accueillera le code et les tests au fil du projet. Drive sert aux documents communs ; les bases brutes n’y seront pas ajoutées sans accord de l’école.

Les méthodes de calcul et le premier formulaire restent à valider avec Leila Belaribi. La CTI est le premier demandeur envisagé. La soutenance est prévue le **4 février 2027** ; le 27 novembre est une date proposée de bilan, à confirmer avec M. Haddad.

Les extractions individuelles, les exports bruts, les secrets et les grilles personnelles ne sont pas déposés sur ce dépôt public. Les tests partagés utilisent des données fictives.
