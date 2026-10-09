---
name: comparer-programmes
description: Comparer deux à quatre programmes immobiliers neufs avec ValoNeuf — prix, typologies, livraison, lots disponibles, position par rapport au marché local. À utiliser quand l'utilisateur hésite entre plusieurs programmes, demande lequel est le plus intéressant, ou veut un tableau comparatif.
---

# Comparer des programmes neufs

## Démarche

1. **Identifier** chaque programme : s'il n'y a qu'un nom ou une commune, le retrouver avec
   `rechercher_programmes` (par nom, commune ou promoteur) et confirmer le bon.
2. **Détailler** : `fiche_programme` pour chacun (synthèse des lots disponibles par typologie,
   prix, livraison).
3. **Situer** : `marche_commune` pour chaque commune concernée (une fois par commune), afin de
   comparer chaque prix au neuf et à l'ancien locaux.

## Le comparatif

Un tableau, une colonne par programme :

| | Programme A | Programme B |
|---|---|---|
| Promoteur, commune | | |
| Livraison | | |
| Lots disponibles | | |
| Prix médian au m² | | |
| Fourchette pour la typologie recherchée | | |
| Écart au neuf de la commune | | |
| Écart à l'ancien (DVF) | | |
| Lien ValoNeuf | | |

Puis :
- **Ce qui les distingue** (prix, calendrier, extérieurs, régime LMNP s'il y en a un).
- **Selon les critères de l'utilisateur** (budget, typologie, délai, investissement ou résidence
  principale) : lequel répond le mieux, et pourquoi — sans trancher à sa place s'il manque une
  information ; poser la question.

Prix en TTC sauf mention LMNP (HT). Ne jamais inventer un lot ou un prix absent des fiches.
