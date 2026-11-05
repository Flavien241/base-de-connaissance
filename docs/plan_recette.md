# Plan de recette initial

Statut : tests à préparer, non exécutés. La cliente doit valider les définitions et les résultats de référence avant la recette.

| Test | Situation | Attendu |
|---|---|---|
| T01 | Champ requis absent à l’import | Erreur explicite et aucun calcul dépendant présenté comme valide |
| T02 | En-tête déplacé sans changement de sens | Correspondance métier conservée sans dépendre de la lettre Excel |
| T03 | En-tête ambigu | Confirmation ou correction de correspondance demandée |
| T04 | Même code et même échéance répétés | Doublon signalé, aucune suppression implicite |
| T05 | Même code à 6 et 18 mois | Deux observations distinctes, pas de double comptage dans une même population |
| T06 | FI001 avec activité, thèse, volontariat | Effectif égal au calcul manuel selon les catégories validées |
| T07 | FI005 avec recherche d’emploi et autre situation | Seules les situations validées comme recherche sont incluses |
| T08 | FI012 avec thèse et autres études | Inclusion des seules thèses retenues par la règle validée |
| T09 | Délai vide, zéro, 1, 2 et 3 mois | Vide distinct de zéro ; borne « moins de 2 » testée explicitement |
| T10 | Mobilité à 0, 3, 4,5, 6, 9 et 18 mois | Résultats selon les bornes validées, sans chevauchement ni oubli |
| T11 | Filtre sans observation | Population vide visible ; taux indisponible si dénominateur nul |
| T12 | Export après filtres | Effectifs et métadonnées identiques à l’écran |
| T13 | Nouvelle version de règle | Nouveau résultat traçable, ancien résultat conservé |
| T14 | Action d’administration par un lecteur | Action refusée ; aucune modification effectuée |
| T15 | Ajout d’un indicateur par configuration | Nouvelle définition calculée sans changement du code du moteur, avec résultats de référence approuvés |
| T16 | Génération du premier formulaire | Chaque champ est associé au bon indicateur, à la bonne population et à la bonne version |
| T17 | Indicateur obligatoire indisponible | Champ signalé ; zéro non inventé ; validation du formulaire bloquée ou réservée selon règle convenue |
| T18 | Accès depuis un autre service | Population ou export non autorisé refusé selon les habilitations |
| T19 | Rapprochement de deux extractions | Correspondances exactes sur la clé approuvée ; doublons et non-appariés exposés |
| T20 | Modification du modèle documentaire | Version antérieure conservée ; génération reliée à la nouvelle version et aux résultats utilisés |

## Fiche d’exécution

Pour chaque test, conserver le jeu fictif, la version testée, le résultat attendu validé, le résultat obtenu, la date, la personne ayant exécuté le test et l’éventuelle anomalie. Les tests non exécutés restent identifiés comme tels.

## Validation

Les effectifs du lot initial doivent correspondre exactement aux résultats manuels validés. Un autre membre relit les cas et les calculs. La cliente valide les écarts résolus ou les réserves consignées. Une absence de message d’erreur ne constitue pas une preuve d’exactitude.
