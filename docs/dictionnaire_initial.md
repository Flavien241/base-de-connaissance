# Dictionnaire initial des données

Ce dictionnaire rapproche les noms utilisés dans l’application des colonnes des fichiers. La correspondance sera vérifiée pour chaque feuille, car les enquêtes présentent des différences.

| Champ métier proposé | En-tête source ou signification | Contrôle prévu |
|---|---|---|
| identifiant_source | Code | Obligatoire pour les contrôles de doublons, non exposé au lecteur |
| date_enquete | Date de l’enquête | Date valide, cohérente avec la feuille |
| promotion | Promotion | Normaliser texte et nombre sans modifier l’année |
| horizon_mois | Échéance de la feuille | Conserver 6 ou 18 ; aucune conversion implicite en 12 |
| formation | Formation, D | Distinguer libellé de formation et statut étudiant/apprenti/continue ; correspondance cliente requise |
| specialite | Spécialité | Harmoniser les variantes après validation |
| genre | Genre | Conserver et documenter les catégories source et inconnues |
| reponse | Réponse | Normaliser la casse ; distinguer réponse et réponse au champ |
| situation | Question de situation au 1er mars | En-tête contenant une date variable selon l’enquête |
| type_etudes | Quel type d’études poursuivez-vous | Définir les catégories de thèse retenues |
| delai_premier_emploi | Délai du premier emploi | Valeur numérique ; vide distinct de zéro |
| contrat_premier_emploi | Contrat du premier emploi, AH dans les fiches | Ne pas confondre avec le contrat actuel ; choix métier à valider |
| statut_premier_emploi | Statut du premier emploi, AL dans les fiches | Ne pas confondre avec le statut actuel ; choix métier à valider |
| delai_emploi_actuel | Délai pour trouver cet emploi | Ne pas substituer au premier délai sans règle validée |
| contrat_actuel | Contrat de l’emploi actuel | Distinguer de l’ancien emploi |
| statut_actuel | Statut de l’emploi actuel | Distinguer de l’ancien emploi |
| pays_emploi | Dans quel pays | Un champ vide n’établit pas automatiquement France |
| mobilite_id | ID_POLYTECH_INTER | Clé propre à la base mobilité |
| mobilite_diplome | diplômé, colonne F | Population diplômée à filtrer |
| mobilite_double_diplome | double-diplôme, colonne K | Qualification de la modalité à confirmer |
| mobilite_stage_mois | nombre de mois stage, colonne O | Numérique, bornes à valider |
| mobilite_etudes_mois | nombre de mois études, colonne P | Numérique ; semestre défini dans la fiche |

## Correspondance des champs

Créer une correspondance versionnée par feuille et par intitulé de question normalisé. Conserver la campagne malgré la normalisation des dates dans les libellés. Si un en-tête est absent, ambigu ou modifié, signaler l’anomalie et suspendre le calcul dépendant. Les positions Excel servent à l’audit, pas de contrat stable pour le moteur. CA/CB et les colonnes à partir de 65 diffèrent notamment pour 2020 à 6 mois ; CB n’est pas une référence fiable au pays.

## À compléter

Vérifier chaque en-tête dans les cinq feuilles, préciser les types et les catégories autorisées, puis lister les champs requis par indicateur. Ne pas supprimer les valeurs non reconnues : les signaler dans le rapport d’import.
