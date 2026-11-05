# Guide d’ajout d’un indicateur

Ce guide décrit le fonctionnement prévu ; l’application reste à développer. L’ajout suivra trois étapes : définir l’indicateur avec la cliente, renseigner sa configuration dans un écran guidé, puis vérifier le résultat avant de l’activer.

## Préparer la définition avec la cliente

Déterminer demandeur, objectif, population, promotion, enquête et horizon. Faire approuver la méthode, les champs, les inclusions et exclusions, les ventilations et le traitement des non-réponses. Définir les habilitations et les résultats manuels de référence.

## Ajouter la configuration

Attribuer un identifiant stable, un demandeur et une version. Choisir les champs métier, sans lettres Excel, puis les opérations du premier lot : comptage, filtres égalité/appartenance/seuil numérique, ET/OU, ventilation et ratio de deux décomptes. Déclarer champs requis, valeurs manquantes et dénominateur. Moyenne et médiane ne sont pas promises. Deux demandeurs peuvent conserver des définitions différentes pour un même intitulé.

L’administrateur vérifie la configuration avant activation. Si le calcul demande un champ ou une opération que le moteur ne gère pas, l’équipe étudie l’évolution nécessaire.

## Vérifier puis publier

Comparer le résultat aux exemples fictifs ou autorisés approuvés. Tester vide, zéro, doublon, population vide, limites de seuil et filtres. Faire relire par un second membre et valider par la cliente. Associer l’indicateur aux champs du modèle documentaire concerné, puis vérifier le formulaire généré.

Conserver configuration, version, date de validation, source, tests et modèle liés. Toute modification ultérieure créera une nouvelle version ; désactiver ne supprimera pas l’historique.

La recette démontrera FI014 (poursuite d’études à 6 mois). Après arbitrage sur les thèses, l’administrateur ajoutera la définition en ne modifiant que la configuration ; le calcul devra correspondre au résultat manuel validé et l’historique Git ne montrera aucun changement du moteur. Si l’exclusion des thèses nécessite le type d’études, O sera requis avec L : ne pas annoncer que L seule suffit avant cet arbitrage.
