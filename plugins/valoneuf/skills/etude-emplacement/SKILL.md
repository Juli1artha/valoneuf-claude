---
name: etude-emplacement
description: Étude de prix d'un emplacement en France avec ValoNeuf — prix du neuf et de l'ancien, programmes concurrents, marché de la commune. À utiliser quand l'utilisateur donne une adresse, un terrain, une rue ou un bien et veut savoir ce que vaut le neuf à cet endroit, si un prix est cohérent, ou ce qui se construit autour.
---

# Étude d'un emplacement

Produire une note courte et sourcée sur la valeur du neuf à un endroit précis, à partir des
outils ValoNeuf.

## Démarche

1. **Situer** : si l'adresse est floue, la faire préciser (commune ou code postal).
2. **Analyser** : appeler `analyser_emplacement` sur l'adresse.
   - Profil incomplet → expliquer que l'analyse demande prénom, nom et mobile (c'est la règle
     de ValoNeuf), les demander, puis `completer_profil` **avec l'accord** de la personne.
   - Quota du jour atteint → le dire, et continuer avec les étapes 3 et 4 (elles suffisent
     pour une première lecture).
3. **Le voisinage** : `programmes_autour` (rayon 1 500 m par défaut) pour l'offre neuve en
   cours de commercialisation, du plus proche au plus lointain.
4. **La commune** : `marche_commune` pour les tendances (prix DVF par année, permis de
   construire, baisses de prix récentes, promoteurs actifs).

## La note

- **En une phrase** : le prix au m² du neuf ici, et son écart avec l'ancien.
- **Les chiffres** : neuf (prix, fourchette, nombre de programmes), ancien (prix, fourchette,
  nombre de ventes), appartements et maisons séparés si l'analyse les distingue.
- **La concurrence** : 3 à 5 programmes proches — nom, promoteur, distance, prix au m²,
  livraison, lots disponibles — avec leur lien ValoNeuf.
- **Le contexte communal** : tendance des prix, projets à venir (permis), mouvement des prix.
- **Vigilance** : si `donnees_minces` est vrai ou si les ventes sont peu nombreuses, le dire
  clairement ; ne jamais présenter une estimation fragile comme un prix.
- **Sources** : DVF (DGFiP, Etalab), offre des promoteurs, Sitadel, telles que rendues par
  ValoNeuf, et le lien vers la carte.

Ne jamais inventer un chiffre absent des réponses des outils.
