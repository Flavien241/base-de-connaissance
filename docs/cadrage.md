# Cadrage du projet

Version de travail 0.3 du 5 novembre 2026, soumise à validation. Le cahier des charges de référence reste le document collaboratif partagé par l’équipe.

## Besoin

Les services de Polytech Lyon produisent manuellement des résultats pour la CTI, l’université, les conseils de perfectionnement et les supports de formation. Une douzaine de systèmes sources sont identifiés dans la consigne ; leurs extractions doivent pouvoir être contrôlées et croisées lorsque les autorisations et clés le permettent. La cliente définit les indicateurs et leurs méthodes, avec des validations régulières.

## Solution cible

Le lecteur consulte des indicateurs et formulaires simplifiés, selon les habilitations de son service. L’administrateur importe et contrôle les extractions, gère les comptes, ajoute ou retire des indicateurs par configuration et conserve leurs versions. Le modèle distingue population et promotion, enquête, définition d’indicateur, résultat, formulaire et demandeur. Chaque champ de formulaire est traçable jusqu’à la source autorisée.

Les règles du Ministère restent à recueillir. Les paramètres de thèse ou VIE illustrent un mécanisme possible de configuration ; aucune définition du Ministère n’est déduite des documents CTI.

## Prototype proposé

- Ingestion d’extractions insertion reconnues, avec contrôles et rapprochements lorsque les clés sont validées.
- FI001, FI005 et FI012 à 6 mois, après validation des règles et résultats de référence.
- Consultation habilitée par service et export agrégé.
- Moteur générique à opérations bornées, historique des règles et preuve d’ajout d’un nouvel indicateur sans modifier le moteur.
- Génération du formulaire d’un premier demandeur réel, depuis un modèle fourni ou approuvé par la cliente, et export dans le format convenu.
- Documentation par service et guide d’ajout d’un indicateur.

Le déroulement est : cadrage et catalogue validés → système d’information insertion → formulaire d’un premier demandeur → extensions mobilité et réussite. Les trois indicateurs proposés seront ajustés aux champs obligatoires du premier formulaire. L’éditeur de code libre, la collecte automatique et la mise en production institutionnelle restent des lots ultérieurs.

## Validation

La cliente doit approuver le périmètre, le catalogue et les méthodes, le premier demandeur et son modèle, les horizons, les clés de rapprochement, les habilitations et les exports. Son accord sera consigné avec version, date et réserves. La publication ne vaut pas validation cliente. Les accords de partage des systèmes sources peuvent être longs ; chaque indisponibilité doit être documentée et son impact arbitré.
