**English** · [Français](README.fr.md)

# Climbing instructors' site

**A climbing instructors' website that its manager runs alone, without touching the code.**

![On the live site in English: activities, an outing's page, the calendar in month then list view, the enquiry form (a visitor types an e-mail, nothing sent), then the map](docs/demo.webp)

<details><summary>French version</summary>

![Sur le site en ligne, le calendrier en vue mois puis liste ; « Réserver cette date » ouvre le formulaire de demande sur cette date et un visiteur tape son nom](docs/demo.fr.webp)

</details>

*Activities, an outing, the calendar, the enquiry form (never sent), the map; the instructor's own texts stay in French.*

## Using it

- **Activities and calendar.** Filters by type, region or month; list or month view.
- **Map.** Venues on an OpenStreetMap map; each marker lists the outings held there.
- **Admin.** The manager edits activities (several prices each), dates, venues, every public label, page sections and menus, and previews before publishing. Each save refreshes the affected pages.
- **Souvenir albums.** After an outing, participants get a private link to the photos and can leave a star rating, published after moderation.
- **English version.** Under `/en`; admin sections have a FR/EN toggle (not yet the block editor), and an empty English field shows the French text.
- **Statistics.** Visitors, pages, referrers, devices and countries, with no cookie and no stored IP address.

## Architecture

![Architecture: visitors and the manager use the Next.js site on Vercel; public pages and the admin read and write a Supabase database; each admin save refreshes the public pages; photos are in Supabase storage; maps use OpenStreetMap](docs/architecture.svg)

<details><summary>French version</summary>

![Architecture : visiteurs et gérant passent par le site Next.js sur Vercel ; pages publiques et administration lisent et écrivent dans une base Supabase ; chaque enregistrement de l'administration rafraîchit les pages publiques ; les photos sont dans le stockage Supabase ; les cartes viennent d'OpenStreetMap](docs/architecture.fr.svg)

</details>

## Deployment

- **Hosting.** Vercel for the site, Supabase (Paris region) for the database and photos.
- **Status.** Online since September 2026; the client edits its content.
- **Stack.** Next.js 16, React 19, Tailwind CSS, Leaflet.

---

**Anthony Hunt** · [ingevision.cloud](https://ingevision.cloud/?lang=en&p=collectif-vertical) · [LinkedIn](https://www.linkedin.com/in/anthony-hunt-3948a9196) · [GitHub](https://github.com/anthohunt)

The code and the client's data are private.
