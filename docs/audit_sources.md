# Audit préliminaire des sources

Repères sur la structure des fichiers fournis et les points de calcul à clarifier avec la cliente.

## Structure constatée

| Source | Contenu |
|---|---|
| Insertion, promotion 2020 à 6 mois | 198 lignes de données, 84 colonnes |
| Insertion, promotion 2020 à 18 mois | 198 lignes de données, 84 colonnes |
| Insertion, promotion 2021 à 6 mois | 197 lignes de données, 84 colonnes |
| Insertion, promotion 2021 à 18 mois | 197 lignes de données, 84 colonnes |
| Insertion, promotion 2022 à 6 mois | 217 lignes de données, 84 colonnes |
| Mobilité, promotion 2022 | 245 lignes de données, 18 colonnes |
| Recueil des fiches | 18 fiches FI001 à FI018 et un modèle |

Les lignes d’enquête sont des observations à des échéances différentes. Ne pas additionner les relevés à 6 et 18 mois comme des personnes distinctes. Les identifiants des deux bases ne fournissent pas de clé de rapprochement commune établie.

## Arbitrages

1. Certaines fiches demandent un horizon de 12 mois, les relevés fournis sont à 6 et 18 mois. Conserver l’horizon réel et demander la correspondance souhaitée.
2. FI018 cite F pour les doubles diplômés ; F est le statut diplômé et K le champ double diplôme. La population et la durée à compter doivent être confirmées.
3. FI003 et FI004 citent AB, délai du premier emploi. Ce champ peut être vide lorsque la personne est toujours dans son premier emploi. Définir le champ pertinent et les éventuelles règles de remplacement, sans traiter le vide comme zéro.
4. FI014 et FI015 décrivent la poursuite d’études sans exclure explicitement les thèses, tandis que les tableaux CTI précisent hors thèses.
5. FI016 distingue moins d’un semestre, un semestre et plus d’un semestre ; sa fiche indique 4,5 mois pour un semestre.
6. FI017 : le PDF comporte < 3 mois, ≥ 3 et < 6 mois, > 6 mois. Le cas de 6 mois n’est pas couvert ; les bornes et les durées nulles doivent être arbitrées.
7. FI018 : les intitulés < 2 semestres et < 4 semestres se chevauchent. Faire confirmer des classes exclusives ainsi que la durée retenue.
8. Les lettres de colonnes de certaines fiches doivent être rapprochées des en-têtes effectifs. Des colonnes de même rang peuvent différer selon les enquêtes.

## Contrôles à réaliser

Unicité des clés au sein de chaque observation, types des champs, valeurs manquantes, catégories de genre et de réponse, homogénéité des formations et des situations, cohérence des horizons. Le présent inventaire structurel ne prouve pas que tous ces contrôles ont été exécutés.

Références : bases insertion et mobilité fournies ; recueil des fiches du 14 février 2025 ; extraits CTI campagne 2023. Leur applicabilité à la campagne visée reste à confirmer.
