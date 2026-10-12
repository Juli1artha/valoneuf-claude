---
name: projet-achat-neuf
description: Accompagner un projet d'achat immobilier neuf avec ValoNeuf, du besoin à la sélection de logements — résidence principale ou investissement. À utiliser quand l'utilisateur dit vouloir acheter dans le neuf, cherche un appartement ou une maison neuve, ou demande par où commencer.
---

# Un projet d'achat dans le neuf

Les consignes du connecteur ValoNeuf (prix, disponibilité, annexes, style) s'appliquent à chaque
étape ; cette méthode dit dans quel ordre enchaîner les outils.

## 1. Comprendre le projet

Poser les questions utiles, pas plus de trois à la fois :
- **Où** : commune(s), quartier, ou un lieu de référence (travail, école, gare).
- **Quoi** : typologie (T2, T3…), maison ou appartement, extérieur, stationnement.
- **Combien** : budget, en distinguant « sous X € » (strictement) et « jusqu'à X € ».
- **Quand** : date d'emménagement ou de livraison acceptable.
- **Pourquoi** : résidence principale, ou investissement (location nue, LMNP).
Noter ce que la personne déclare non négociable : on ne l'assouplira jamais.

## 2. Chercher, puis affiner avec la synthèse

- Dès que la zone et la typologie ou le budget sont connus : `rechercher_logements`.
- Lire sa synthèse sur toutes les correspondances (fourchettes, répartitions, « ce qu'il reste si
  l'on ajoute un critère ») et s'en servir pour poser **une** question qui affine (« 38 T3 ; 6 avec
  jardin ; sous 400 000 € il en reste 10 — le jardin compte-t-il ? »).
- Rien ne correspond : présenter les alternatives à part, en disant le critère assoupli et l'écart.
- Sans critères précis : `rechercher_programmes` par commune, ou `programmes_autour` d'une adresse.

## 3. Montrer une courte sélection

- Retenir 3 à 6 logements, dans l'ordre de présentation, puis `afficher_selection` avec leurs
  identifiants, le libellé de la recherche validée et le total trouvé. Les cartes montrent prix,
  surfaces, visuels, plan et marché : **ne pas recopier leur contenu** ; dire en deux ou trois
  phrases pourquoi ces logements, et l'incertitude qui compte (disponibilité à reconfirmer,
  annexes sans prix).
- La personne modifie la sélection (« seulement ceux avec jardin », « retire le deuxième ») :
  rappeler `afficher_selection` avec la nouvelle liste.
- **Si les cartes ne s'affichent pas** (Claude Code, terminal, ou réponse sans interface) : un
  tableau court à la place — rang, programme, prix, surface, prix au m², extérieur, livraison,
  lien ValoNeuf — et rien de plus.

## 4. Approfondir ce qui intéresse

- Départager deux à quatre logements : `comparer_lots` ; citer sa synthèse et une alerte par
  logement, pas le détail.
- Le plan : `voir_plan` (compte ValoNeuf gratuit) ; sans compte, `apercu_plan`. Un écart entre le
  plan et la fiche : `rapprocher_plan`, sans trancher.
- Le quartier : `quartier_logement` — distances à vol d'oiseau, jamais de temps de trajet.
- Le prix face au marché local : `analyse_locale` (ventes réelles autour, neuf comparable) ; pour
  une commune entière, `marche_commune`.
- Une adresse précise hors stock : `analyser_emplacement` (une par jour, profil complet requis).

## 5. Garder, partager, être accompagné

- « Garde-moi cette sélection », « envoie-la à mon conjoint » : proposer `partager_selection`,
  après avoir dit ce qui est conservé (les logements et les critères, aucune donnée personnelle,
  6 mois, lien ouvert à qui le possède) ; ne l'appeler qu'avec l'accord de la personne.
- Un conseiller ADN Family peut accompagner l'achat **au même prix qu'en direct** auprès du
  promoteur. Le proposer quand le projet se précise, sans insister. Si la personne accepte : lui
  relire prénom, nom, téléphone, programme visé et un résumé du projet, puis
  `demander_accompagnement` **avec son accord explicite**.

Toujours donner les liens ValoNeuf : c'est là que la personne voit la carte et les plans.
