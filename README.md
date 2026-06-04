# JMA Carpentry & Construction

Marketing homepage for JMA Carpentry & Construction, Perth WA.
Roofing, decking, patios, gazebos and outdoor construction. Single-page site, deployed via GitHub Pages.

Built by The Service Edit.

## Stack
- Static HTML, single file (`index.html`)
- Tailwind via CDN (no build step)
- Google Fonts: Anton / Oswald / Inter
- Web3Forms for the quote form
- JSON-LD GeneralContractor schema

## Structure
```
jma-construction/
├── index.html        # homepage (the whole site)
├── 404.html          # branded not-found page
├── robots.txt
├── sitemap.xml
├── CNAME             # custom domain for GitHub Pages
├── README.md
└── images/
    ├── README.txt           # maps every photo slot to a filename
    ├── why-jma-frame.png    # wired in: Why JMA background (real)
    ├── logo.png             # JMA logo (replace header + footer monogram)
    ├── services/            # the six service-card photos
    └── projects/            # real before/after project photography
```
og-image.jpg (1200x630 social share) sits at the repo root, referenced by the OG tag.

## Go-live checklist
Search `index.html` for the word REPLACE and these placeholders:
- [x] JMA logo wired into header + footer (images/logo.png)
- [ ] `REPLACE_WITH_JMA_WEB3FORMS_KEY` -> JMA's own Web3Forms access key (NOT the TSE key)
- [ ] Phone number `04XX XXX XXX` (header schema, footer, tel link)
- [ ] `ABN 00 000 000 000` -> real ABN
- [ ] Stat numbers (250+, 15+) -> confirmed figures
- [ ] Three testimonials -> real client reviews
- [ ] All `picsum.photos` images -> real JMA project photos
- [ ] Confirm domain `www.jmacarpentry.com.au` across CNAME, canonical, OG, sitemap, robots
- [ ] Add a GA4 tag if JMA wants analytics

## Deploy (GitHub Pages)
1. Create repo `jma-construction` under mellyanncox-ctrl, push these files to `main`.
2. Repo Settings -> Pages -> Source: Deploy from branch -> `main` / root.
3. Custom domain: enter `www.jmacarpentry.com.au`, tick Enforce HTTPS.
4. Point DNS: CNAME record `www` -> `mellyanncox-ctrl.github.io`.

## Update workflow
```
cd /Users/melly_1/APPS/jma-construction && git add . && git commit -m "[message]" && git push origin main
```
