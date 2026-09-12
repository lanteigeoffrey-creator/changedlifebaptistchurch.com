# Changed Life Baptist Church — website

A 7-page static website (HTML/CSS/JS, no build step) built for
www.changedlifebaptistchurch.com, sourced from the CLBC Golden Jubilee
brochure.

## Pages
- `index.html` — Home
- `about.html` — History timeline (1976–2026) and leadership
- `branches.html` — All 13 branch churches, grouped by region
- `campus.html` — Oasis campus fellowships (UG Legon, UHAS Ho, KNUST)
- `ministries.html` — All ministries (Ladies', Men's, Youth, AWANA, etc.)
- `sermons.html` — Podbean podcast + Facebook/YouTube live stream
- `contact.html` — Contact form and Give section

Shared styles/scripts live in `assets/styles.css` and `assets/main.js`.

## To publish
Upload the whole folder to any static host (Netlify, Vercel, cPanel,
GitHub Pages, etc.) and point changedlifebaptistchurch.com at it. No
server-side code is required for the pages themselves.

## Still needed before launch (placeholders in the code)
1. **Photos** — Real photography from the church's Facebook page
   should replace the blue/red gradient placeholder blocks
   (`.media-block` in the CSS). Facebook could not be scraped
   automatically here since it requires a login; download images
   manually from https://www.facebook.com/profile.php?id=100066663400036
   and drop them into `assets/photos/`, then swap each `.media-block`
   div for an `<img>` tag.
2. **Podbean player** — `sermons.html` has an HTML comment with the
   exact iframe code; just add the church's Podbean site name.
3. **Facebook & YouTube Live embeds** — same page, `#live` section,
   also has ready-to-use iframe snippets in HTML comments.
4. **Addresses, phone numbers, service times** — the brochure text
   didn't include street addresses or clock times for each branch, so
   these are flagged inline with a note for the office to fill in
   (`branches.html`, `contact.html`).
5. **Giving details** — mobile money / bank details on `contact.html`
   under "Give".
6. **Contact form backend** — the form currently just confirms receipt
   in the browser (see `assets/main.js`). Wire it to an email service
   (e.g. Formspree, EmailJS) or a backend endpoint before launch.
7. **Social links** — Facebook is linked; add real YouTube, Podbean and
   Instagram URLs in the footer/social icons across all pages.
