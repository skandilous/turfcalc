# TurfCalc.au — turf calculator site

A ready-to-upload static site: a turf calculator (the hero) plus supporting guides
and the trust pages Google AdSense needs. No build step, no backend — pure HTML/CSS/JS.

## Files

| File | Purpose | Target keyword(s) |
|------|---------|-------------------|
| `index.html` | The calculator + FAQ (money page) | "turf calculator", "how much turf do i need" |
| `how-much-turf-do-i-need.html` | Worked examples guide | "how much turf do i need", "turf calculator australia" |
| `how-to-measure-your-lawn.html` | Measuring guide | "how to measure lawn for turf" |
| `turf-prices-australia.html` | Cost guide (commercial intent) | "turf prices australia", "cost of turf per m2" |
| `turf-prices-sydney.html` | Sydney-specific cost guide | "turf prices sydney", "cost of turf sydney" |
| `how-to-lay-turf.html` | Laying guide | "how to lay turf", "laying turf australia" |
| `turf-types-australia.html` | Variety comparison | "turf types australia", "buffalo vs kikuyu" |
| `about.html` `contact.html` `privacy-policy.html` | Trust pages (required for AdSense) | — |
| `sitemap.xml` `robots.txt` | Indexing | — |
| `style.css` | Shared styling | — |

## Before you publish (10 minutes)

1. **Buy a domain** and pick something keyword-relevant (e.g. turfcalc.com.au). Domain age
   helps — register now even if you tweak content later.
2. **Find-and-replace `https://turfcalculator.com.au`** with your real domain in every file
   (canonical tags + sitemap + robots).
3. **Replace `hello@turfcalculator.com.au`** on the contact page with your real email.
4. Optional: swap the "TurfCalc.au" brand name if your domain differs.

## Hosting (free options)

Any static host works. Easiest:
- **Cloudflare Pages** or **Netlify** — drag-and-drop the folder, free HTTPS, fast.
- **GitHub Pages** — push the folder to a repo, enable Pages.
Upload the whole folder; `index.html` is the homepage.

## Getting ranked

1. Add the site to **Google Search Console**, submit `sitemap.xml`.
2. Get a few genuine visitors flowing (share it, link from any profile you have).
3. Aim for ~50–100 organic visits/day before applying to AdSense — protects you from
   invalid-click flags and shows Google the site is real.

## Adding AdSense (after the site is live + aged a little)

1. Apply at adsense.google.com with your domain.
2. Once approved, paste your AdSense script into the `<head>` of every page
   (look for the `ADSENSE:` comment already placed in `index.html`).
3. Replace each `<div class="ad-slot">Ad space</div>` placeholder with a real ad unit,
   or turn on Auto Ads and let Google place them.
4. Start conservative — one or two units — so the calculator stays usable. A tool people
   actually complete is worth more long-term than a page buried in ads.

## Expanding (to grow traffic)

The fastest way to more rankings is more calculators + guides on the same theme:
soil/mulch/gravel calculators, a "cost to lay a lawn" estimator, state-specific pages
("turf prices Sydney/Melbourne"). Each new page is another door into the site.
