# Conception technique

L’outil comporte un import de fichiers, une base de données, un moteur configurable et un générateur de formulaires. Ahdi choisira les technologies libres au plus tard le 20 novembre après un essai des cinq feuilles. Il prendra en charge import et accès ; Abderrahim, modèle et moteur ; Louka, interface et formulaires ; Rayen, tests ; Flavien, hébergement et lancement avec Ahdi.

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
| Demandeur | identité, référentiel, format demandé |
| Définition d’indicateur | identifiant métier, intitulé, demandeur, actif/inactif |
| Version de règle | version, population, critères, champs requis, paramètres, date |
| Résultat | import, version, filtres, effectif, dénominateur éventuel, date |
| Formulaire et modèle | demandeur, version du document, champs et correspondances de résultats |
| Génération | modèle, résultats associés, date, format d’export et contrôles |
| Compte et habilitation | identifiant, rôle, services autorisés, statut actif |

Modifier une définition crée une nouvelle version et conserve les résultats antérieurs. Une définition appartient à un demandeur : le même intitulé peut recouvrir une autre formule ailleurs. Un écran guidé permet de créer, modifier ou désactiver un indicateur. Opérations du premier lot : comptage, filtres égalité/appartenance/seuil numérique, combinaison ET/OU, ventilation et ratio de deux décomptes. Champs requis, gestion des absences et dénominateur sont explicites. Pas de code arbitraire ni de moyenne/médiane promise. La recette vérifie FI014 ajouté par configuration seule, sans changement du moteur dans Git.

L’import associe les champs par intitulé normalisé avec une table de correspondance versionnée par feuille. Les dates variables des questions sont normalisées, sans confondre premier emploi et emploi actuel. Colonne absente, valeur hors liste, doublon de clé ou feuille vide produisent un rapport indiquant feuille et champ ; les seuls calculs dépendants sont bloqués.

Chaque promotion × échéance est une enquête distincte. Le rapprochement insertion–mobilité est hors premier lot : les clés diffèrent. Une extension demanderait une clé validée ou une correspondance autorisée, avec détection des conflits ; aucune jointure approximative n’est prévue.

Les lecteurs sont rattachés à un service et à un périmètre autorisé. Un administrateur peut gérer sources et définitions selon son autorisation ; un lecteur n’accède qu’aux agrégats et à leur traçabilité, jamais aux réponses individuelles. La démonstration utilisera un administrateur et deux lecteurs de services fictifs. Le seuil de masquage convenu s’appliquera aux résultats et à leurs traces, à l’écran comme à l’export. Le choix de ce seuil et les risques de reconstitution par filtres seront examinés avec l’école.

La génération relie chaque champ à un résultat et conserve versions du modèle, des règles et des imports. Un champ manquant est signalé et ne devient pas zéro. La trace comprend enquête, population, filtres, règle, nombre de lignes retenues/exclues et réponses utiles. Le modèle sera demandé pour le 18 novembre ; sans réception au 20, l’extrait CTI 2023 sera le gabarit provisoire à faire approuver.

## Choix à instruire

Comparer une application Python avec interface intégrée à une interface web séparée. Retenir la solution que l’équipe sait lancer et maintenir. Évaluer le serveur de l’école : accès, environnement, stockage, sauvegarde et modalités de déploiement. Docker est une option de reprise, pas un prérequis acquis.

## Démonstration

À défaut de serveur confirmé, prévoir un lancement local avec données fictives et consignes reproductibles. Les copies locales des bases reçues ne valent pas accord pour un stockage partagé : emplacement, habilitations et conservation restent à confirmer avec l’école. Minimiser les champs traités. Aucune base brute ne sera ajoutée au Drive ou au serveur sans cet accord, ni au dépôt public. Flavien et Ahdi écriront et vérifieront la procédure de lancement quand le prototype existera.
