# Audit préliminaire des sources

Repères sur la structure des fichiers fournis et les points de calcul à clarifier avec la cliente.

Audit de structure actualisé le 6 novembre 2026. Il ne constitue pas une validation des valeurs ni des méthodes métier.

## Structure constatée

| Source | Contenu |
|---|---|
| Insertion, promotion 2020 à 6 mois | 198 lignes de données, 84 colonnes |
| Insertion, promotion 2020 à 18 mois | 198 lignes de données, 84 colonnes |
| Insertion, promotion 2021 à 6 mois | 197 lignes de données, 84 colonnes |
| Insertion, promotion 2021 à 18 mois | 197 lignes de données, 84 colonnes |
| Insertion, promotion 2022 à 6 mois | 217 lignes de données, 84 colonnes |
| Mobilité, promotion 2022 | 245 lignes de données, 18 colonnes |
| Recueil des fiches | 15 fiches insertion, 3 fiches mobilité et un modèle de fiche |

Les lignes d’enquête sont des observations à des échéances différentes. Ne pas additionner les relevés à 6 et 18 mois comme des personnes distinctes. Les identifiants des deux bases ne fournissent pas de clé de rapprochement commune établie.

## Arbitrages

1. Certaines fiches demandent un horizon de 12 mois, les relevés fournis sont à 6 et 18 mois. Conserver l’horizon réel et demander la correspondance souhaitée.
2. FI018 cite F pour les doubles diplômés ; F est le statut diplômé et K le champ double diplôme. La population et la durée à compter doivent être confirmées.
3. FI003 et FI004 citent AB, délai du premier emploi. Ce champ peut être vide lorsque la personne est toujours dans son premier emploi. Définir le champ pertinent et les éventuelles règles de remplacement, sans traiter le vide comme zéro.
4. FI014 et FI015 décrivent la poursuite d’études sans exclure explicitement les thèses, tandis que les tableaux CTI précisent hors thèses.
5. FI016 distingue moins d’un semestre, un semestre et plus d’un semestre ; sa fiche indique 4,5 mois pour un semestre.
6. FI017 : le PDF comporte < 3 mois, ≥ 3 et < 6 mois, > 6 mois. Le cas de 6 mois n’est pas couvert ; les bornes et les durées nulles doivent être arbitrées.
7. FI018 : les intitulés < 2 semestres et < 4 semestres se chevauchent. Faire confirmer des classes exclusives ainsi que la durée retenue.
8. Les lettres ne sont pas stables. Comparée à « Promo 2020 à 18 mois », « Promo 2020 à 6 mois » présente 20 en-têtes différents à partir de la colonne 65, plus la question de situation datée en L. Par exemple CA est le pays dans quatre feuilles, mais la ville dans celle de 2020 à 6 mois. CB est la ville dans quatre feuilles et une autre question dans celle de 2020 à 6 mois : FI011 cite pourtant CB pour l’emploi basé en France. Prévoir une correspondance par feuille et par intitulé normalisé.
9. AB (délai), AH (contrat) et AL (statut cadre), cités par les fiches, appartiennent au bloc du premier emploi (« Quel était… »). Le bloc actuel (« Quel est… ») est distinct : le statut actuel est par exemple en colonne 71 dans quatre feuilles. Faire confirmer le bloc à utiliser, sans substituer l’un à l’autre.
10. Le champ Formation est en D mais ne garantit pas une distinction étudiant/apprenti/formation continue. Obtenir la correspondance nécessaire au formulaire. Les en-têtes de situation contiennent la date du 1er mars de l’année d’enquête : les normaliser sans perdre la campagne.
11. Les titres de mobilité mentionnant « 6 mois après diplomation » sont à clarifier pour l’extension. Les asymétries insertion sont conservées : cadre à 6 mois, emploi en France à 12 mois.

## Contrôles à réaliser

Les contrôles porteront sur les doublons, les types de champs, les valeurs manquantes, les catégories de réponse, les noms de formation et la cohérence des échéances.

L’extrait CTI donne un contrôle interne : 19 emplois en France + 5 à l’étranger = 24 emplois (IX-D6-14, IX-D6-15 et IX-D6-11). Cette identité est à retrouver ou à expliquer uniquement si population, campagne et règles de la base utilisée correspondent. Ce n’est pas un résultat attendu automatiquement sur les cinq feuilles reçues.

Références : bases insertion et mobilité fournies ; recueil des fiches du 14 février 2025 ; extraits CTI campagne 2023. Leur applicabilité à la campagne visée reste à confirmer.
