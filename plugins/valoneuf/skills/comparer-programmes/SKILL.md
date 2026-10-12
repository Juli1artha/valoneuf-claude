---
name: comparer-programmes
description: Comparer deux à quatre programmes immobiliers neufs, ou des logements précis, avec ValoNeuf — prix, typologies, livraison, lots disponibles, quartier, position par rapport au marché local. À utiliser quand l'utilisateur hésite entre plusieurs programmes ou logements, demande lequel est le plus intéressant, ou veut un tableau comparatif.
---

# Comparer des programmes ou des logements neufs

Les consignes du connecteur ValoNeuf (prix, disponibilité, annexes, style) s'appliquent ; cette
méthode dit quoi rassembler et comment le présenter.

## Démarche

1. **Identifier** chaque programme : s'il n'y a qu'un nom ou une commune, le retrouver avec
   `rechercher_programmes` (nom, commune ou promoteur) et confirmer le bon.
2. **Détailler** : `fiche_programme` pour chacun (lots disponibles par typologie, prix, livraison).
3. **Descendre au logement** quand la typologie ou le budget sont connus : retenir dans chaque
   programme le ou les lots qui correspondent, puis `comparer_lots` sur l'ensemble (20 au plus) —
   il rend une synthèse des écarts et une alerte par logement.
4. **Situer** : `analyse_locale` pour le programme ou le lot (ventes réelles autour, neuf
   comparable) ; `marche_commune` une fois par commune pour la tendance.
5. **L'emplacement**, si la personne s'en soucie : `quartier_logement` pour chaque programme
   (distances à vol d'oiseau, quartier, risques).

## Le comparatif

Quand des logements précis sont comparés, les montrer d'abord avec `afficher_selection` (la
fiche des cartes permet de les comparer côte à côte) et ne pas recopier ce qu'elle affiche.
Sinon — ou si les cartes ne s'affichent pas (Claude Code, terminal) — un tableau, une colonne
par programme :

| | Programme A | Programme B |
|---|---|---|
| Promoteur, commune | | |
| Livraison prévue | | |
| Lots disponibles (typologie recherchée) | | |
| Prix et prix au m² | | |
| Extérieur, stationnement | | |
| Écart observé au marché local | | |
| Alerte principale | | |
| Lien ValoNeuf | | |

Puis, en quelques phrases :
- **Ce qui les distingue vraiment** : deux ou trois différences utiles, pas une relecture du tableau.
- **Selon les priorités de la personne** (budget, typologie, délai, habiter ou investir) : lequel
  y répond le mieux, et pourquoi. Sans ces priorités, ne désigner aucun « meilleur » : poser la
  question.

Un écart à la médiane du marché est un écart observé, jamais la preuve d'une surévaluation.
Ne jamais inventer un lot ou un prix absent des réponses.
