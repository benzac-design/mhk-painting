# MHK Painting and Decorating Services: Website

Website for John (Magdy Moussa), a licensed painter in Liverpool NSW. Built 25 Sept 2026 as a favour, at Dad's request.

- **Live site:** https://mhkpainting.com.au (also https://mhk-painting.vercel.app)
- **Domain:** mhkpainting.com.au, registered 25 Sept 2026 at Crazy Domains, renews 25 Sept 2027 (auto renew on). DNS: A records for `@` and `www` point to Vercel `76.76.21.21`
- **Vercel project:** `mhk-painting` (account: benjoezacharia8-tech)
- **GitHub backup:** https://github.com/benzac-design/mhk-painting (private)

## Business details (from his business card)

| | |
|---|---|
| Business | MHK Painting and Decorating Services |
| Owner | Magdy Moussa ("John"), Licensed Professional Painter |
| Phone | 0406 786 299 |
| Email | mhk.moussa@yahoo.com |
| Location | Liverpool, NSW |
| ABN | 15 990 194 296 |
| NSW Fair Trading licence | 454415C |
| Taglines | Top Quality Guaranteed. Free Quotes. |

## Research (ServiceSeeking profile)

Source: https://www.serviceseeking.com.au/profile/205788-mhk-painting-and-decorating-services

- 5.0 stars from 87 reviews, all 5-star
- Hired 112 times, member since Aug 2019
- ServiceSeeking "Top 10 Painter in Sydney" 2021, 2022, 2023
- Services: interior, exterior, commercial, fence, residential, floor and concrete
- Areas: Liverpool plus Moorebank, Edmondson Park, Oran Park, Macquarie Fields, Denham Court, Bankstown, Padstow, Villawood, Riverwood, Bexley North, Caringbah, Kingsford, Alexandria, Silverwater, Schofields
- Recent jobs (from Dad): homes in Panania and Connells Point
- No existing website or social pages found

## Brand (taken from the business card)

- Black `#121212` background
- Lime `#D9EC1C` (the paint stroke), warm yellow `#F2C40F` (the drips)
- White `#FFFFFF`, logo blue `#1F4FA3` (MHK badge only)
- Fonts: Playfair Display italic (headings, like "Magdy Moussa (John)" on the card), Jost (body)

## Folder layout

```
mhk painting/
  README.md            this file
  website/             everything that gets deployed
    index.html         the whole site (one file, inline CSS + JS)
    img/               job photos, compressed to WebP
    .vercelignore      stops .env files ever being uploaded
    .vercel/           links this folder to the Vercel project (not in git)
  docs/
    original-plan.md   the first plan
    website-review.md  the 6.5/10 review and what was fixed
  photos/originals/    unedited job photos (local only, not in git)
```

## How to update the site

1. Edit `website/index.html` (or ask Claude to).
2. Preview: open `website/index.html` in a browser, or run `python3 -m http.server 8765 --directory website` and go to http://localhost:8765.
3. Deploy from the `website` folder:

```bash
cd "website" && npx vercel deploy --prod --yes
```

4. Commit and push the change to GitHub.

## Privacy decisions

- House number on the letterbox is blurred in `driveway-finished.webp`.
- Date stamps cropped off the interior photos.
- Ceiling photo (hanging wires, stain) left off the site on purpose.
- realestate.com.au listing photos not used (they belong to the agents). Client street addresses not published, suburbs only.
- Unedited originals stay in `photos/originals/`, which git ignores.

## To do

- [ ] Show John the site and get his OK
- [ ] Get finished "after" shots and before/after pairs from John
- [ ] Confirm he still has every review at 5 stars (the site says so)
- [ ] Click the licence check link once to make sure it works
- [x] Domain `mhkpainting.com.au` bought and connected to Vercel
- [ ] Re-take a photo of the business card for this folder (the original upload expired)
