---
name: preparer-rdv-acquereur
description: Préparer un rendez-vous avec un acquéreur dans le neuf (pour un conseiller, un courtier, un CGP ou un agent) — contexte de marché, logements adaptés au profil, arguments, objections et questions à poser, sélection à partager au client. À utiliser quand l'utilisateur prépare un rendez-vous client, une découverte ou une proposition de biens neufs.
---

# Préparer un rendez-vous acquéreur

L'utilisateur est un professionnel. Lui fournir un dossier de préparation **en une page**. Les
consignes du connecteur ValoNeuf (prix, disponibilité, annexes) s'appliquent.

## Ce qu'il faut savoir du client

Commune(s) visée(s), budget, typologie, calendrier, objectif (habiter ou investir), financement
(apport, accord bancaire). Demander ce qui manque ; avancer avec des hypothèses déclarées sinon.

## Le dossier

1. **Le marché en trois chiffres** (`marche_commune`) : prix du neuf, prix de l'ancien (DVF),
   tendance — et ce que cela veut dire pour ce budget.
2. **Les logements à présenter** : `rechercher_logements` avec le profil du client (sa synthèse
   dit aussi ce que le budget permet ou non), puis `comparer_lots` sur les 3 à 5 retenus — prix,
   surface, extérieur, livraison, alerte principale. `fiche_programme` pour le contexte de chaque
   programme.
3. **Le positionnement de chacun** : `analyse_locale` (écart observé avec les ventes réelles et
   le neuf comparable) ; `quartier_logement` pour l'argument d'emplacement (à vol d'oiseau).
4. **Les arguments** : ce qui distingue chaque logement (emplacement, calendrier, prix,
   extérieurs, régime LMNP le cas échéant).
5. **Les objections probables** et la réponse factuelle (prix au-dessus de l'ancien, délai de
   livraison, annexes dont le prix n'est pas communiqué, frais de notaire réduits dans le neuf…).
6. **Les points à vérifier avant le rendez-vous** : disponibilité à reconfirmer auprès du
   promoteur, prix des stationnements, écart entre plan et fiche (`voir_plan`, `rapprocher_plan`).
7. **Les questions à poser** pour affiner la découverte.

## La sélection pour le client

- La montrer avec `afficher_selection` dans l'ordre de présentation ; si les cartes ne s'affichent
  pas (Claude Code, terminal), un tableau court avec les liens ValoNeuf.
- Pour l'envoyer au client : proposer `partager_selection` (lien secret, 6 mois, aucune donnée
  personnelle), et ne l'appeler qu'avec l'accord de l'utilisateur.

S'appuyer uniquement sur les chiffres rendus par les outils, et citer leurs sources.
