# Changed Life Baptist Church — website

An 8-page static website (HTML/CSS/JS, no build step) built for
www.changedlifebaptistchurch.com, sourced from the CLBC Golden Jubilee
brochure and church-supplied photography.

## Pages
- `index.html` — Home, with a full-screen looping hero video
- `about.html` — History timeline (1976–2026) and leadership
- `branches.html` — All 13 branch churches, grouped by region
- `campus.html` — Oasis campus fellowships (UG Legon, UHAS Ho, KNUST)
- `ministries.html` — All ministries (Ladies', Men's, Youth, AWANA, etc.)
- `gallery.html` — Photo gallery with a lightbox viewer
- `sermons.html` — Sermon podcast (Podbean-powered, branded as "Podcast")
  + Facebook/YouTube live stream section
- `contact.html` — Contact form and Give section

Shared styles/scripts live in `assets/styles.css` and `assets/main.js`.

## Logo & favicon
The uploaded crest had a lot of transparent padding around it, so it's
been cropped tightly to `assets/logo.png` (used in every nav and
footer) and rendered into a full favicon set (`assets/favicon-16.png`
through `favicon-512.png`), linked in the `<head>` of every page.

## Hero video
`assets/video/hero.mp4` plays full-bleed, muted, looped and autoplaying
on the homepage, with `assets/video/hero-poster.jpg` as the fallback
poster frame while it loads. If you ever swap the video file, keep the
same filename or update the `<source>` tag in `index.html`.

## Gallery
Seven photos live in `assets/gallery/`, each with a generic caption
(no names) and a click-to-enlarge lightbox. To add more: drop a photo
in that folder and copy one of the `.gallery-item` blocks in
`gallery.html`.

## Podcast
`sermons.html` embeds the live Podbean playlist widget under the
heading "The sermon podcast" — all visitor-facing text says "podcast,"
not "Podbean." To change which episodes appear, update the playlist in
Podbean directly; the embed will reflect it automatically.

## To publish
Upload the whole folder to any static host (Netlify, Vercel, cPanel,
GitHub Pages, etc.) and point changedlifebaptistchurch.com at it. No
server-side code is required for the pages themselves.

## Still needed before launch
1. **Facebook & YouTube Live embeds** — `sermons.html`, `#live`
   section, has ready-to-use iframe snippets in HTML comments; just
   add the church's Facebook video URL and YouTube channel ID.
2. **Addresses, phone numbers, service times** — the brochure text
   didn't include street addresses or clock times for each branch, so
   these are flagged inline with a note for the office to fill in
   (`branches.html`, `contact.html`).
3. **Giving details** — mobile money / bank details on `contact.html`
   under "Give".
4. **Contact form backend** — the form currently just confirms receipt
   in the browser (see `assets/main.js`). Wire it to an email service
   (e.g. Formspree, EmailJS) or a backend endpoint before launch.
5. **Social links** — Facebook and the podcast are linked; add real
   YouTube and Instagram URLs in the footer/social icons across all
   pages.
6. **More gallery photos** — as branch and campus events are
   photographed, drop them into `assets/gallery/` following the
   existing pattern.

