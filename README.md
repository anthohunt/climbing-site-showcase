> Showcase repository: the code and data of this project are private; this README describes it. / Dépôt vitrine : le code et les données de ce projet sont privés ; ce README le décrit.

# la structure website

The public website and admin area of a climbing instructors' organisation, which the client runs on their own, without touching the code.

## The problem

A small climbing organisation sells guided outings. It needs a website that presents its activities, venues and instructors, shows upcoming dates and takes enquiries. The manager is not a developer: they must be able to change everything themselves, from prices to text, in French as well as in English.

## How it works

- Visitors browse activities, venues on a map, instructor profiles and the calendar, then book a date or send an enquiry.
- The manager logs into the admin and edits the content; each save refreshes the affected pages, which are otherwise cached for 10 minutes.
- After an outing, they send participants a private link to the photo album; participants can leave a star rating there, published after moderation.
- The English version lives under `/en`: each admin section has an FR/EN toggle, and a field left empty in English shows the French text.

## What is built

In service and used by the client, who has created 11 activities (9 published) and 9 venues.

- **Activities**: publish on/off, featuring, several prices per activity, dates, a person in charge picked from a list.
- **Editable content**: every public label, sections that can be hidden and reordered, 15 block types, free pages, menus, media library, text editor, preview of unpublished content.
- **Public calendar**, by month or as a grid, with filters; "Book this date" preselects the date.
- **Stories** (blog), **souvenir albums** shared by private link, moderated **star ratings**.
- **Instructors**: public profiles, spoken languages (8 to choose from), password that an administrator can regenerate.
- **Internal statistics**: visitors, pages, referrers, devices, countries, with no cookie, no third-party service and no stored IP address.
- **English version**: 345 interface labels translated, 9 content types translatable in the admin, hreflang tags and a bilingual sitemap. The block editor does not have its English toggle yet.

## What is public

The site is online. The code and the admin remain private.

## Tech stack

- Next.js 16, React 19, Tailwind CSS
- Supabase (Postgres, authentication, storage, row-level access rules)
- Leaflet and OpenStreetMap for maps
- Vercel hosting

---

## Version française

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
