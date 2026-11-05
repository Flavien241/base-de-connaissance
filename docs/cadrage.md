# Cadrage

Version du **6 novembre 2026**, proposée pour validation par Leila Belaribi. Encadrant : M. Haddad. Soutenance : 4 février 2027.

## Objectif

Le projet « Base de connaissance » doit aider les services de Polytech Lyon à calculer leurs indicateurs et à remplir les formulaires demandés par la CTI, l’université et les autres demandeurs.

## Premier périmètre

L’outil doit importer les cinq feuilles d’insertion, contrôler leur qualité, calculer les indicateurs et générer le formulaire d’un premier demandeur. La CTI est l’hypothèse de départ, à confirmer. Un même nom d’indicateur peut avoir une définition différente par demandeur.

Le pilote FI001/FI005/FI012 utilise seulement situation et type d’études (L et O). Ces trois décomptes permettent de vérifier l’import et le calcul sans dépendre des colonnes ambiguës d’emploi. Cible : 4 décembre, après validation des règles. Ils ne suffisent pas au formulaire complet : son catalogue de champs obligatoires, ventilations et nombres de réponses devra être couvert au 18 décembre, selon le modèle convenu.

La consultation filtrera promotion, formation, spécialité, genre et échéance. La correspondance étudiant/apprenti/formation continue est à obtenir ; elle ne se déduit pas automatiquement du champ « Formation ». Deux rôles sont prévus, administrateur et lecteur, avec un périmètre autorisé par service pour chaque lecteur.

L’administration guidée permettra de créer, modifier ou désactiver une définition versionnée. Opérations prévues : comptage, égalité/appartenance/seuil numérique, ET/OU, ventilation et ratio de deux décomptes. La recette démontrera l’ajout de FI014 par configuration seule ; une opération supplémentaire exigera une évolution convenue. Moyenne et médiane ne sont pas promises.

## Livrables

- Cahier des charges, rôles et planning.
- Catalogue des indicateurs et méthodes de calcul.
- Application, code source et tests.
- Guide utilisateur par service et guide d’ajout d’un indicateur.
- Démonstration sur le formulaire d’un demandeur réel.

Mobilité, réussite et rapprochement insertion–mobilité sont des extensions. Un graphique simple est facultatif. Le nom retenu reprend le diaporama : « Base de connaissance — Indicateurs sur les populations étudiantes et diplômées ».

Les règles, les habilitations, le seuil des petits effectifs et le stockage autorisé sont à convenir avec Mme Belaribi. Les lecteurs ne verront que des agrégats autorisés ; les mêmes masquages s’appliqueront aux exports. Les engagements et dépendances figurent au [planning](planning.md).
