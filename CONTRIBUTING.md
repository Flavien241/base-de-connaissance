# Contribuer au projet

Chaque membre utilise son compte GitHub et fait relire ses modifications par un autre membre.

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

Flavien suit le cadrage et le planning ; Ahdi, la conception technique et le développement ; Abderrahim, les fichiers et les règles ; Louka, les parcours et formulaires ; Rayen, les tests et les guides.

Une tâche passe dans Terminé lorsque son résultat est disponible et relu. Un point nécessitant une décision de la cliente reste dans En attente cliente. Les sources individuelles et les grilles personnelles sont conservées dans l’espace privé de l’équipe.
