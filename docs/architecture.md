# Conception technique

L’outil comporte un import de fichiers, une base de données, un module de calcul et un générateur de formulaires. Les technologies seront choisies après un essai sur les fichiers fournis.

## Composants

1. Importer un fichier dans l’espace de traitement autorisé.
2. Vérifier sa structure et produire un rapport d’anomalies.
3. Transformer les champs reconnus vers un modèle métier stable.
4. Exécuter les règles versionnées sur une population explicite.
5. Restituer les agrégats et leurs métadonnées selon les habilitations du service.
6. Associer les résultats aux champs d’un modèle documentaire et générer le formulaire du demandeur avec son export.

Un serveur applicatif léger réalisera les traitements ; l’interface de lecture recevra les agrégats autorisés. Le stockage séparera sources, données normalisées, configurations, résultats et formulaires générés. La stack devra être libre, avec choix motivés et conditions de reprise documentées.

## Modèle logique

| Entité | Attributs principaux |
|---|---|
| Import | identifiant, format, source, date, rapport de contrôles |
| Population et promotion | identité du périmètre, promotion, critères d’appartenance |
| Enquête | campagne, date d’observation, horizon réel, population ciblée |
| Observation | identifiant source, import, population, enquête, variables utiles |
| Correspondance de populations | clés autorisées, version, source, statut d’appariement, conflits |
| Demandeur | identité, référentiel, format demandé |
| Définition d’indicateur | identifiant métier, intitulé, donneur d’ordres |
| Version de règle | version, population, critères, champs requis, paramètres, date |
| Résultat | import, version, filtres, effectif, dénominateur éventuel, date |
| Formulaire et modèle | demandeur, version du document, champs et correspondances de résultats |
| Génération | modèle, résultats associés, date, format d’export et contrôles |
| Compte et habilitation | identifiant, rôle, services autorisés, statut actif |

Modifier une définition crée une nouvelle version et conserve les résultats antérieurs. Un indicateur est une configuration interprétée : population, filtres, opération d’agrégation, gestion des absences et paramètres de taux. Les opérations autorisées sont bornées ; aucun code arbitraire n’est exécuté. La recette vérifie l’ajout d’un indicateur utilisant les champs et opérations existants sans modifier le moteur.

Le rapprochement des populations utilise une clé validée ou une correspondance autorisée par l’école. Les identifiants insertion et mobilité ne sont pas réputés équivalents. Doublons, absences d’appariement et conflits sont signalés ; aucune jointure approximative sur l’identité n’est présumée autorisée.

La génération d’un formulaire relie chaque champ à un résultat et conserve versions du modèle, des règles et des imports. Un champ manquant est signalé et ne devient pas automatiquement zéro. Le modèle du premier demandeur réel doit être fourni ou approuvé avant l’implémentation.

## Choix à instruire

Comparer une application Python avec interface intégrée à une interface web séparée. Retenir la solution que l’équipe sait lancer et maintenir. Évaluer le serveur de l’école : accès, environnement, stockage, sauvegarde et modalités de déploiement. Docker est une option de reprise, pas un prérequis acquis.

## Démonstration

À défaut de serveur confirmé, prévoir un lancement local avec données fictives et consignes reproductibles. Aucune donnée cliente ni aucun secret ne doit être ajouté au dépôt public. La procédure de lancement sera écrite lorsque le choix technique et le prototype existent.
