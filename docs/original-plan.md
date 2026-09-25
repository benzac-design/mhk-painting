# Plan: Website for MHK Painting & Decorating Services

## Context
The user's dad asked them to build a website for a local painter. Details come from the business card photo + web research. A few details in the spoken request were slightly off, so the **card is the source of truth**:

| Field | Value (from card) |
|---|---|
| Business | MHK Painting and Decorating Services |
| Owner | Magdy Moussa ("John") — Licensed Professional Painter |
| Phone | 0406 786 299 |
| Email | mhk.moussa@yahoo.com |
| Location | Liverpool, NSW |
| ABN | 15 990 194 296 (user said "1599042 96" — missing digits) |
| NSW Fair Trading licence | 454415C (no leading "f") |
| Taglines | Top Quality Guaranteed · Free Quotes |

### Research findings (ServiceSeeking profile)
- **5.0 stars from ~87 reviews**, hired 112+ times, on the platform since Aug 2019
- **Top 10 Painter in Sydney — 2021, 2022, 2023**
- Services: interior, exterior, residential, commercial, fence, floor & concrete painting
- Areas: Liverpool + SW/greater Sydney (Moorebank, Edmondson Park, Oran Park, Macquarie Fields, Bankstown, Padstow, Villawood, Riverwood, Caringbah, Bexley North, Kingsford, Alexandria, Silverwater, Schofields, Denham Court)
- Review themes: on-time, tidy cleanup, attention to detail, fair pricing, friendly
- No existing website or social page found → this would be his first site.

### Brand colours (taken from the card)
- **Black / charcoal** `#121212` — main background
- **Neon lime-yellow** `#D9EC1C` (paint-stroke colour) — accents, buttons, headings
- **Warm yellow drip** `#F2C40F` — secondary accent
- **White** `#FFFFFF` — body text on dark
- **Logo blue** `#1F4FA3` — used sparingly (logo badge only)
- Fonts: bold serif-italic display for the name (like the card's "Magdy Moussa") → *Playfair Display*; clean geometric sans for body (like the card's contact text) → *Jost*.

## Site structure (single page, mobile-first)
1. **Sticky header** — "MHK" blue badge logo, nav links, big yellow **Call 0406 786 299** button (tap-to-call on phones).
2. **Hero** — dark background with a CSS/SVG lime paint-roller stroke + drips echoing the card; headline "Top Quality Guaranteed", sub "Licensed painter in Liverpool & Sydney's South-West", buttons: *Get a Free Quote* / *Call Now*. Trust strip: ★ 5.0 (87 reviews) · Top 10 Sydney Painter 2021–23 · NSW Licensed.
3. **Services** — 6 cards with icons: Interior, Exterior, Commercial, Fences, Floors & Concrete, Residential repaints.
4. **Why choose MHK** — Licensed & ABN-registered, free quotes, clean-up included, on-time, 100+ jobs completed.
5. **Reviews** — 3 short paraphrased review cards + link to the ServiceSeeking profile (not copied verbatim).
6. **Areas we service** — suburb chips.
7. **About John** — short bio (Magdy "John" Moussa, licensed professional painter) with placeholder for a photo.
8. **Free quote form** — name, phone, suburb, job type, message → opens the user's email app via `mailto:` to mhk.moussa@yahoo.com (no backend needed). 
9. **Footer** — phone, email, Liverpool NSW, ABN, Licence No. 454415C.
10. Floating mobile "Call" button.

## Implementation
- One self-contained `index.html` in the session folder (inline CSS + a little vanilla JS for mobile nav, scroll reveal, and the mailto form). No framework, easy to host anywhere (Netlify Drop / Vercel / cPanel).
- Placeholder image slots (gradient boxes labelled "Add job photo") — real before/after photos from John will make the biggest difference later.
- Accessible contrast (lime on black is fine; never lime text on white), responsive down to 360px.
- SEO basics: title/meta description "Painter Liverpool NSW | MHK Painting & Decorating", LocalBusiness JSON-LD with phone, ABN-less address (Liverpool NSW 2170).

## Verification
- Open the file in the built-in browser pane; screenshot desktop + mobile (375px) widths.
- Check tap-to-call link, nav anchors, mailto form, dark layout.
- Send the file to the user.

## Notes for the user
- Not publishing it to a public URL myself — it represents a real business, so hosting/domain should be done by you/your dad once John approves. I'll suggest easy free hosting options after.
- Worth asking John for: job photos, a logo file, and whether he wants reviews/awards shown.
