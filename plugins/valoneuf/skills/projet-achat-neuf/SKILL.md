---
name: projet-achat-neuf
description: Accompagner un projet d'achat immobilier neuf avec ValoNeuf, du besoin à la sélection de logements — résidence principale ou investissement. À utiliser quand l'utilisateur dit vouloir acheter dans le neuf, cherche un appartement ou une maison neuve, ou demande par où commencer.
---

# Un projet d'achat dans le neuf

## 1. Comprendre le projet

Poser les questions utiles, pas plus de trois à la fois :
- **Où** : commune(s), quartier, ou un lieu de référence (travail, école, gare).
- **Quoi** : typologie (T2, T3…), maison ou appartement, extérieur, stationnement.
- **Combien** : budget total, ou mensualité visée.
- **Quand** : date d'emménagement ou de livraison acceptable.
- **Pourquoi** : résidence principale, ou investissement (location nue, LMNP).

## 2. Chercher

- Dès que la typologie ou le budget sont connus : `rechercher_logements` (commune, code postal,
  département, ou rayon autour d'une adresse de référence ; pièces, budget TTC, surface,
  livraison, résidence classique ou gérée). Il rend les logements qui conviennent et leur total
  exact, 50 par page.
- Pour une première découverte sans critères : `rechercher_programmes` par commune, ou
  `programmes_autour` d'une adresse.
Présenter une **courte sélection** (3 à 6 logements ou programmes) avec, pour chacun, la raison de
sa présence. Rappeler que le prix est celui du lot seul : stationnements et annexes à part.

## 3. Approfondir

- `fiche_programme` sur ceux qui intéressent : lots disponibles dans la typologie et le budget.
- `marche_commune` pour dire si le prix est dans le marché.
- `analyser_emplacement` si un emplacement précis mérite une étude (une par jour).

## 4. Proposer d'être accompagné

Un conseiller ADN Family peut accompagner l'achat **au même prix qu'en direct** auprès du
promoteur. Le proposer quand le projet se précise, sans insister. Si la personne accepte :
lui relire prénom, nom, téléphone, programme visé et un résumé de son projet, puis
`demander_accompagnement` **avec son accord explicite**.

Toujours donner les liens ValoNeuf : c'est là que la personne voit les plans et la carte.
