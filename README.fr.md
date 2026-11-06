[English](README.md) · **Français**

**Anthony Hunt** · [Fiche du projet sur ingevision.cloud](https://ingevision.cloud/?p=collectif-vertical) · [LinkedIn](https://www.linkedin.com/in/anthony-hunt-3948a9196) · [Profil GitHub](https://github.com/anthohunt)

> Dépôt vitrine : le code et les données de ce projet sont privés ; ce README le décrit.

# Site d’une structure d’escalade

Le site public et l'espace d'administration d'une structure de moniteurs d'escalade, que le client fait vivre seul, sans toucher au code.

## Le problème

Une petite structure d'escalade vend des sorties encadrées. Elle a besoin d'un site qui présente ses activités, ses lieux et ses moniteurs, affiche les prochaines dates et reçoit les demandes. Le gérant n'est pas développeur : il doit pouvoir tout modifier lui-même, des tarifs aux textes, en français comme en anglais.

## Comment ça marche

- Le visiteur parcourt les activités, les lieux sur carte, les fiches des moniteurs et le calendrier, puis réserve une date ou envoie une demande.
- Le gérant se connecte à l'admin et modifie le contenu ; chaque enregistrement rafraîchit les pages concernées, mises en cache 10 minutes sinon.
- Après une sortie, il envoie aux participants un lien privé vers l'album photo ; ceux-ci peuvent y laisser un avis étoilé, publié après modération.
- La version anglaise vit sous `/en` : chaque section de l'admin a une bascule FR/EN, et un champ laissé vide en anglais affiche le texte français.

## Ce qui est construit

En service et utilisé par le client, qui y a créé 11 activités (9 publiées) et 9 lieux.

- **Activités** : mise en ligne, mise en avant, plusieurs tarifs par activité, dates, responsable choisi dans une liste.
- **Contenu éditable** : chaque libellé public, sections masquables et réordonnables, 15 types de blocs, pages libres, menus, médiathèque, éditeur de texte, aperçu du non-publié.
- **Calendrier** public, par mois ou en grille, avec filtres ; « Réserver cette date » présélectionne la date.
- **Récits** (blog), **albums souvenirs** par lien privé, **avis étoilés** modérés.
- **Moniteurs** : fiches publiques, langues parlées (8 au choix), mot de passe régénérable par un administrateur.
- **Statistiques internes** : visiteurs, pages, provenance, appareils, pays, sans cookie ni service tiers, sans stocker d'adresse IP.
- **Version anglaise** : 345 libellés d'interface traduits, 9 types de contenu traduisibles dans l'admin, balises hreflang et plan du site bilingue. L'éditeur de blocs n'a pas encore sa bascule anglaise.

## Ce qui est public

Le site est en ligne. Le code et l'administration restent privés.

## Pile technique

- Next.js 16, React 19, Tailwind CSS
- Supabase (Postgres, authentification, stockage, règles d'accès par ligne)
- Leaflet et OpenStreetMap pour les cartes
- Hébergement Vercel
