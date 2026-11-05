# Codev

Projet académique de 5e année, sur un semestre, pour les services utilisateurs d’indicateurs de Polytech Lyon. L’outil doit transformer les extractions de l’école en indicateurs fiables et en formulaires adaptés aux demandeurs.

Nom de travail de l’outil : IndiQ, soumis à la cliente.

## État au 5 novembre 2026

Ce premier lot documentaire intègre la consigne complète : cadrage des indicateurs, système d’information insertion, formulaire d’un premier demandeur réel, puis extensions mobilité et réussite. Le prototype applicatif n’est pas encore développé et le cahier des charges V0.3 reste à valider.

Le suivi des tâches est organisé dans le [tableau Trello privé](https://trello.com/b/N3q0qeqB). Les membres restent à inviter. GitHub conserve les versions des fichiers ; Trello suit leur préparation, leur relecture et leur validation. Les documents partagés et les sources autorisées restent dans l’espace Drive de l’équipe. Les droits de partage ne sont pas modifiés par ce dépôt.

## Équipe

| Membre | Rôle |
|---|---|
| Flavien BONTEMPS | Chef de projet confirmé |
| Ahdi BENMAOUIA | Développement et intégration, proposé |
| Abderrahim BEN MOHA | Données et règles métier, proposé |
| Louka PESIC | Fonctionnel et ergonomie, proposé |
| Rayen BENAMMAR | Qualité et documentation, proposé |

## Premiers livrables

- [Cadrage](docs/cadrage.md) et [planning](docs/planning.md).
- [Audit des sources](docs/audit_sources.md) et [dictionnaire initial](docs/dictionnaire_initial.md).
- [Parcours utilisateurs](docs/parcours_utilisateurs.md) et [architecture proposée](docs/architecture.md).
- [Plan de recette](docs/plan_recette.md) et [décisions en attente](docs/decisions.md).
- [Organisation Trello](docs/trello.md) et [méthode de contribution](CONTRIBUTING.md).
- [Catalogue initial des indicateurs](docs/catalogue_indicateurs.md).
- [Premier formulaire](docs/formulaires.md), [guide par service](docs/guide_utilisateur.md) et [ajout d’un indicateur](docs/ajouter_indicateur.md).
- [Points à vérifier avant le mail](docs/avant_envoi.md).

## Périmètre proposé

La cible comprend ingestion contrôlée d’extractions hétérogènes, rapprochement autorisé des populations, catalogue et moteur de calcul paramétrables, consultation par service et génération de formulaires depuis les modèles des demandeurs. FI001, FI005 et FI012 servent de premier lot de calcul proposé. Le lot sera ajusté aux champs obligatoires du premier formulaire choisi avec la cliente.

L’ajout d’un indicateur fondé sur les champs et opérations disponibles doit se faire par configuration, sans modifier le moteur. La preuve d’ajout et les tests de calcul font partie de la recette. Mobilité et réussite viennent en extensions après le parcours insertion vers premier formulaire.

## Échéances

Le mail de M. Haddad du 25 septembre fixait un premier jalon au lundi 5 octobre : cahier des charges validé, répartition des rôles et planning. Le point de novembre demande un bilan, les grilles d’autoévaluation et les premières traces Git. Le Gantt de reprise commence au 5 novembre ; il ne remplace pas le jalon initial. Soutenance prévue le 4 février 2027, comme indiqué dans le document partagé.

## Données

Les bases clientes, leurs extraits individuels, les exports bruts et les autoévaluations personnelles restent hors de ce dépôt public. Les tests partagés utiliseront des données fictives. Les documents ci-dessus décrivent la structure des sources et les règles à discuter, sans reproduire de réponses individuelles.

## Contributions

Ces fichiers forment une base de rédaction à relire et compléter. Les propositions ne constituent pas des décisions validées. Chaque membre publie ses propres modifications après relecture, avec les dates réelles et un lien vers la tâche correspondante. Voir CONTRIBUTING.md.
