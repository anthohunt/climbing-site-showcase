**English** · [Français](README.fr.md)

**Anthony Hunt** · [Project page on ingevision.cloud](https://ingevision.cloud/?lang=en&p=collectif-vertical) · [LinkedIn](https://www.linkedin.com/in/anthony-hunt-3948a9196) · [GitHub profile](https://github.com/anthohunt)

> Showcase repository: the code and data of this project are private; this README describes it.

# Climbing instructors' website

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
