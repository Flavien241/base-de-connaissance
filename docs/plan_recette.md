# Plan de recette initial

Plan du 6 novembre 2026 ; ces tests ne sont pas encore exécutés. Abderrahim préparera les valeurs manuelles attendues ; Rayen produira les données fictives, automatisera et exécutera les tests, puis consignera les écarts. La cliente approuvera les règles et les références métier.

## Exemple du pilote

Jeu fictif de six lignes, même promotion à 6 mois, sans doublon :

| Ligne fictive | Situation | Type d’études | Réponse |
|---|---|---|---|
| P01 | Activité professionnelle | Sans objet | Oui |
| P02 | Poursuite d’études | Thèse académique | Oui |
| P03 | Volontariat correspondant à un VIE | Sans objet | Oui |
| P04 | Recherche d’emploi | Sans objet | Oui |
| P05 | Poursuite d’études | Autres études | Oui |
| P06 | Non renseignée | Non renseigné | Non |

Après approbation des correspondances CTI : **5 répondants, FI001 = 3, FI005 = 1, FI012 = 1**. FI014 vaudrait **1** si la règle hors thèses est retenue, **2** sinon ; cette règle doit être arbitrée avant recette. Aucun taux n’est déduit sans dénominateur défini.

## Scénarios

| Test | Situation | Attendu |
|---|---|---|
| T01 | Colonne attendue absente, valeur hors liste ou feuille vide | Message nommant feuille et champ ; aucun calcul dépendant présenté comme valide |
| T02 | En-tête déplacé sans changement de sens | Correspondance métier conservée sans dépendre de la lettre Excel |
| T03 | En-tête ambigu | Confirmation ou correction de correspondance demandée |
| T04 | Même code et même échéance répétés | Doublon signalé, aucune suppression implicite |
| T05 | Même code à 6 et 18 mois | Deux observations distinctes, pas de double comptage dans une même population |
| T06 | FI001 avec activité, thèse, volontariat | Effectif égal au calcul manuel selon les catégories validées |
| T07 | FI005 avec recherche d’emploi et autre situation | Seules les situations validées comme recherche sont incluses |
| T08 | FI012 avec thèse et autres études | Inclusion des seules thèses retenues par la règle validée |
| T09 | Délai vide, zéro, 1, 2 et 3 mois | Vide distinct de zéro ; borne « moins de 2 » testée explicitement |
| T10 — extension | Mobilité à 0, 3, 4,5, 6, 9 et 18 mois | Résultats selon les bornes validées, sans chevauchement ni oubli ; hors recette du premier lot |
| T11 | Filtre sans observation | Population vide visible ; taux indisponible si dénominateur nul |
| T12 | Export après filtres | Effectifs et métadonnées identiques à l’écran |
| T13 | Nouvelle version de règle | Nouveau résultat traçable, ancien résultat conservé |
| T14 | Action d’administration par un lecteur | Action refusée ; aucune modification effectuée |
| T15 | Ajouter FI014 dans l’administration guidée | Seule la configuration change, vérifiable dans Git ; calcul égal au résultat manuel selon l’arbitrage thèses ; désactivation possible sans supprimer l’historique |
| T16 | Génération du premier formulaire | Chaque champ est associé au bon indicateur, à la bonne population et à la bonne version |
| T17 | Indicateur obligatoire indisponible | Champ signalé ; zéro non inventé ; validation du formulaire bloquée ou réservée selon règle convenue |
| T18 | Un administrateur et deux lecteurs de services fictifs | Chaque lecteur ne voit que son périmètre et ses agrégats ; import, paramétrage, données individuelles et export d’un autre périmètre refusés |
| T19 — extension | Rapprochement insertion–mobilité | À définir après validation d’une clé ; hors premier lot |
| T20 | Modification du modèle documentaire | Version antérieure conservée ; génération reliée à la nouvelle version et aux résultats utilisés |
| T21 | Seuil fictif de masquage = 3 ; groupes d’effectifs 1, 2 et 3 | 1 et 2 masqués, 3 visible à l’écran et à l’export ; seuil de production à convenir avec la cliente |
| T22 | Une ou deux personnes d’un service filtrent un résultat puis exportent le formulaire sans aide | Les deux actions sont réalisées ; difficultés observées consignées et blocages corrigés avant acceptation |
| T23 | Trace d’un résultat consulté | Source, enquête, population, filtres, version de règle, lignes retenues/exclues et réponses utiles visibles ; aucune ligne individuelle pour le lecteur |
| T24 | Extrait CTI de référence, si même population/campagne/règles | Identité 19 emplois France + 5 étranger = 24 emplois retrouvée ou écart expliqué ; ne pas l’imposer à une base non comparable |

## Fiche d’exécution

Pour chaque test, conserver le jeu fictif, la version testée, le résultat attendu validé, le résultat obtenu, la date, la personne ayant exécuté le test et l’éventuelle anomalie. Les tests non exécutés restent identifiés comme tels.

## Validation

Les effectifs du lot initial doivent correspondre exactement aux résultats manuels validés. Un autre membre relit les cas et les calculs. La cliente valide les écarts résolus ou les réserves consignées. Une absence de message d’erreur ne constitue pas une preuve d’exactitude.

La disponibilité de tous les champs obligatoires sera contrôlée sur le modèle approuvé. Le prototype peut afficher un champ indisponible ; un formulaire annoncé complet doit avoir tous ses champs obligatoires vérifiés. Le pilote de trois calculs n’est pas cette recette complète.
