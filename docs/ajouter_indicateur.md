# Guide d’ajout d’un indicateur

L’ajout suit trois étapes : définir l’indicateur avec la cliente, renseigner sa configuration, puis vérifier le résultat avant de l’activer.

## Préparer la définition avec la cliente

Déterminer demandeur, objectif, population, promotion, enquête et horizon. Faire approuver la méthode, les champs, les inclusions et exclusions, les ventilations et le traitement des non-réponses. Définir les habilitations et les résultats manuels de référence.

## Ajouter la configuration

Attribuer un identifiant stable et une version. Renseigner les filtres et une opération prise en charge par le moteur, par exemple un décompte, une agrégation ou un ratio avec numérateur et dénominateur séparés. Utiliser les identifiants métier du dictionnaire, pas les lettres Excel. Déclarer les champs requis et la gestion des valeurs manquantes.

L’administrateur vérifie la configuration avant activation. Si le calcul demande un champ ou une opération que le moteur ne gère pas, l’équipe étudie l’évolution nécessaire.

## Vérifier puis publier

Comparer le résultat aux exemples fictifs ou autorisés approuvés. Tester vide, zéro, doublon, population vide, limites de seuil et filtres. Faire relire par un second membre et valider par la cliente. Associer l’indicateur aux champs du modèle documentaire concerné, puis vérifier le formulaire généré.

Conserver configuration, version, date de validation, source, tests et modèle liés. Toute modification ultérieure crée une nouvelle version. La recette doit démontrer qu’un nouvel indicateur utilisant les opérations disponibles est ajouté sans modifier le code du moteur.
