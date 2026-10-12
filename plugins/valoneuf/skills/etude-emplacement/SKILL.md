---
name: etude-emplacement
description: Étude de prix d'un emplacement en France avec ValoNeuf — prix du neuf et de l'ancien, ventes réelles autour, programmes concurrents, quartier, marché de la commune. À utiliser quand l'utilisateur donne une adresse, un terrain, une rue ou un bien et veut savoir ce que vaut le neuf à cet endroit, si un prix est cohérent, ou ce qui se construit autour.
---

# Étude d'un emplacement

Produire une note courte et sourcée sur la valeur du neuf à un endroit précis. Les consignes du
connecteur ValoNeuf (millésimes, distances à vol d'oiseau, écarts observés) s'appliquent.

## Démarche

1. **Situer** : si l'adresse est floue, la faire préciser (commune ou code postal).
2. **Le marché autour** : `analyse_locale` sur l'adresse — ventes anciennes comparables (DVF),
   neuf disponible comparable, lots marqués vendus, permis à venir, avec l'échantillon, la période
   et les limites. S'il s'agit d'un programme ou d'un logement du stock, l'appeler avec son
   identifiant plutôt qu'avec l'adresse.
3. **L'estimation d'emplacement** : `analyser_emplacement` sur l'adresse, si la personne veut un
   prix au m² estimé à cet endroit précis.
   - Profil incomplet → expliquer que l'analyse demande prénom, nom et mobile (règle de ValoNeuf),
     les demander, puis `completer_profil` **avec l'accord** de la personne.
   - Quota du jour atteint → le dire, et s'appuyer sur les étapes 2, 4 et 5.
4. **La concurrence** : `programmes_autour` (1 500 m par défaut), du plus proche au plus lointain.
5. **Le quartier** : `quartier_logement` sur le point — proximités, quartier INSEE, risques,
   quartier prioritaire. La délinquance seulement si la personne la demande.
6. **La commune** : `marche_commune` pour la tendance (prix DVF par année, permis, baisses de
   prix, promoteurs actifs).

## La note

- **En une phrase** : ce que vaut le neuf ici, et l'écart observé avec l'ancien.
- **Les chiffres** : neuf (prix, fourchette, nombre de programmes), ancien (prix, fourchette,
  nombre de ventes, période), appartements et maisons séparés quand l'analyse les distingue.
- **La concurrence** : 3 à 5 programmes proches — nom, promoteur, distance à vol d'oiseau, prix
  au m², livraison, lots disponibles — avec leur lien ValoNeuf.
- **Le quartier** : deux proximités utiles et le nom du quartier ; les risques s'il y en a.
- **Le contexte communal** : tendance des prix, projets à venir (permis), mouvement des prix.
- **Vigilance** : échantillon mince (`donnees_minces`, peu de ventes) ou chiffre ancien (plus de
  cinq ans) : le dire clairement ; ne jamais présenter une estimation fragile comme un prix.
- **Sources et dates** : DVF (DGFiP, Etalab), offre des promoteurs, Sitadel, INSEE, telles que
  rendues par ValoNeuf, et le lien vers la carte.

Ne jamais inventer un chiffre absent des réponses des outils.
