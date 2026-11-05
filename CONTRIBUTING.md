# Contribuer au projet

## Base documentaire et contributions suivantes

La première publication centralise une base documentaire préparée avec assistance. Elle ne prétend pas être le travail individuel antérieur des cinq membres. Chaque membre peut maintenant cloner le dépôt avec `git clone https://github.com/Flavien241/Codev.git`, relire son lot et proposer ses modifications.

Le premier commit reste attribué au compte connecté qui le publie. Les documents de cadrage sont des propositions, les tests décrits ne sont pas annoncés comme exécutés et la validation cliente reste à obtenir.

## Contribution de chaque membre

Chacun accepte son invitation comme collaborateur, utilise son propre compte GitHub et vérifie son identité Git avec `git config user.name` et `git config user.email`. Ne pas configurer l’identité d’un autre membre.

Avant une nouvelle contribution :

```text
git switch main
git pull --ff-only
git switch -c docs/mon-sujet
```

Relire puis améliorer un livrable : préciser une règle, corriger un mapping, dessiner un parcours, ajouter un scénario de test. Ajouter seulement les fichiers concernés, par exemple :

```text
git add docs/parcours_utilisateurs.md
git commit -m "docs: préciser les parcours de consultation et administration"
git push -u origin docs/mon-sujet
```

Ouvrir ensuite une pull request dans GitHub, demander une relecture et coller son lien dans Trello. Un changement de nom seul ne remplace pas une contribution au contenu.

## Cinq lots proposés

| Membre | Lot à relire et compléter | Exemple de contribution réelle |
|---|---|---|
| Flavien | cadrage.md, planning.md, decisions.md | Confirmer rôles, jalons et liste d’arbitrages ; intégrer les réponses client |
| Ahdi | architecture.md | Choisir et justifier la solution après un essai local ; décrire le lancement |
| Abderrahim BEN MOHA | audit_sources.md, dictionnaire_initial.md, catalogue_indicateurs.md | Vérifier les champs et règles sur les fichiers conservés hors Git |
| Louka PESIC | parcours_utilisateurs.md, formulaires.md | Produire les écrans, détailler les interactions et le modèle du premier demandeur |
| Rayen BENAMMAR | plan_recette.md, guide_utilisateur.md, ajouter_indicateur.md | Construire les cas fictifs, résultats attendus et procédures de reprise |

Chef de projet confirmé : Flavien. Les quatre autres lots restent proposés. Les dates de publication sont celles du travail réellement publié. Si un document existait auparavant hors Git, préciser sa provenance et sa date réelle lorsqu’elles sont connues ; ne pas antidater les commits.

## Terminer une tâche

Une tâche passe dans Terminé lorsqu’un livrable identifiable est publié, relu et satisfait ses critères. Une proposition attendant l’accord de la cliente reste dans En attente cliente. Les grilles individuelles sont partagées dans l’espace privé choisi par l’équipe ou l’école.
