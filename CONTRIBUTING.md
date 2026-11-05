# Contribuer au projet

Chaque membre utilisera son compte GitHub et fera relire ses modifications par un autre membre. Les commits décrivent les contributions réellement déposées, avec leur date effective.

## Préparer une modification

Cloner le dépôt : `git clone https://github.com/Flavien241/base-de-connaissance.git`.

Avant de travailler, mettre à jour main et créer une branche :

```text
git switch main
git pull --ff-only
git switch -c docs/mon-sujet
```

Ajouter uniquement les fichiers modifiés, créer le commit et publier la branche :

```text
git add docs/parcours_utilisateurs.md
git commit -m "docs: préciser le parcours de consultation"
git push -u origin docs/mon-sujet
```

Ouvrir une pull request, demander une relecture et ajouter son lien à la fiche Trello.

## Répartition

La [répartition du README](README.md#équipe) attribue les modules : import et accès à Ahdi, moteur et modèle à Abderrahim, interface et formulaires à Louka, tests et guides à Rayen, coordination et hébergement à Flavien avec Ahdi.

Abderrahim calculera les valeurs attendues à la main ; Rayen préparera les jeux fictifs et exécutera les tests automatisés. La cliente approuvera les règles et les références métier.

Une tâche passe dans Terminé lorsque son résultat est disponible et relu. Un point nécessitant une décision de la cliente reste dans En attente cliente. Chacun remplira sa grille officielle d’autoévaluation et ajoutera les liens de ses contributions aux tâches. Rayen et Flavien consolideront le bilan ; les grilles resteront privées. Les bases brutes sont exclues du dépôt ; leur stockage autorisé reste à convenir avec l’école.
