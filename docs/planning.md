# Planning et échéances

## Consignes reçues

Selon le mail de M. Haddad du 25 septembre, transmis par l’équipe :

- **Lundi 5 octobre** : cahier des charges validé, rôles attribués et planning incluant la soutenance ; retour par mail avec les membres et la cliente en copie.
- **Novembre** : point d’avancement, grilles d’autoévaluation et dépôt Git avec les premières traces.
- **4 février** : soutenance.

Le 5 octobre 2026 était bien un lundi. Le calendrier de travail utilise 2026–2027, cohérent avec la soutenance du 4 février 2027 figurant dans le document partagé. Au 5 novembre, la validation du premier jalon n’est pas documentée. Ne pas le marquer comme terminé sur la seule base du dépôt créé.

## Gantt de reprise proposé

```mermaid
gantt
    title Planning de reprise Codev
    dateFormat YYYY-MM-DD
    axisFormat %d/%m
    section Cadrage
    Cadrage et premier demandeur       :c1, 2026-11-05, 2026-11-12
    Cadrage soumis                    :milestone, 2026-11-12, 0d
    Catalogue et règles               :c2, 2026-11-09, 2026-11-27
    Modèle de données et maquettes    :c3, 2026-11-16, 2026-11-27
    Point académique proposé          :milestone, 2026-11-27, 0d
    section Prototype
    SI insertion et moteur configurable :p1, 2026-11-30, 2026-12-18
    Calculs de référence               :milestone, 2026-12-18, 0d
    Marge de fin décembre             :2026-12-19, 2027-01-03
    Premier formulaire et habilitations :p2, 2027-01-04, 2027-01-15
    Premier formulaire                :milestone, 2027-01-15, 0d
    section Livraison
    Recette et guides par service     :r1, 2027-01-18, 2027-01-29
    Gel du prototype                  :milestone, 2027-01-29, 0d
    Préparation soutenance            :r2, 2027-01-25, 2027-02-03
    Soutenance                        :milestone, 2027-02-04, 0d
```

Ces jalons sont des propositions. La date exacte du point académique de novembre et les disponibilités ne sont pas encore connues. Le 12 novembre correspond à une remise proposée, pas à une validation cliente présumée.

## Suivi

Après chaque séance, mettre à jour Trello et les décisions. La cliente valide règles et modèle documentaire avant calcul et génération définitifs. Les accords de partage et les clés disponibles conditionnent les rapprochements. Le parcours complet insertion vers premier formulaire reste prioritaire ; les extensions mobilité et réussite seront planifiées après son acceptation. Fin décembre est une marge sans disponibilité présumée.
