[English](README.md) · **Français**

# Site de moniteurs d'escalade

**Le site d'un collectif de moniteurs d'escalade, que son gérant fait vivre seul, sans toucher au code.**

[![Sur le site en ligne, le calendrier en vue mois puis liste ; « Réserver cette date » ouvre le formulaire de demande sur cette date et un visiteur tape son nom (cliquer pour la vidéo complète)](docs/demo.gif)](https://drive.google.com/file/d/1B9oK9wRxfSd5EIXMBbhqnzkp8tGdWlr6/view)

*Calendrier, puis « Réserver cette date » : le formulaire s'ouvre avec la date déjà choisie. [Vidéo complète (1 min 12)](https://drive.google.com/file/d/1B9oK9wRxfSd5EIXMBbhqnzkp8tGdWlr6/view)*

## Utilisation

- **Activités et calendrier.** Filtres par type, région ou mois ; vue liste ou mois.
- **Carte.** Les lieux sur une carte OpenStreetMap ; chaque marqueur liste les sorties qui s'y déroulent.
- **Administration.** Le gérant modifie les activités (plusieurs tarifs chacune), les dates, les lieux, chaque libellé public, les sections des pages et les menus, avec un aperçu avant publication. Chaque enregistrement rafraîchit les pages concernées.
- **Albums souvenirs.** Après une sortie, les participants reçoivent un lien privé vers les photos et peuvent laisser un avis étoilé, publié après modération.
- **Version anglaise.** Sous `/en` ; les sections de l'administration ont une bascule FR/EN (pas encore l'éditeur de blocs), et un champ anglais vide affiche le texte français.
- **Statistiques.** Visiteurs, pages, provenance, appareils et pays, sans cookie ni adresse IP stockée.

## Architecture

![Architecture : visiteurs et gérant passent par le site Next.js sur Vercel ; pages publiques et administration lisent et écrivent dans une base Supabase ; chaque enregistrement de l'administration rafraîchit les pages publiques ; les photos sont dans le stockage Supabase ; les cartes viennent d'OpenStreetMap](docs/architecture.svg)

## Exploitation

- **Hébergement.** Vercel pour le site, Supabase (région Paris) pour la base et les photos.
- **État.** En ligne depuis septembre 2026 ; le client en modifie le contenu.
- **Technologies.** Next.js 16, React 19, Tailwind CSS, Leaflet.

---

**Anthony Hunt** · [ingevision.cloud](https://ingevision.cloud/?p=collectif-vertical) · [LinkedIn](https://www.linkedin.com/in/anthony-hunt-3948a9196) · [GitHub](https://github.com/anthohunt)

Le code et les données du client sont privés.
