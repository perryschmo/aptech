# Anchor Partners

Marketing site for **Anchor Partners** — fractional CTO and 90-day systems engagements for small business owners in Orange County, CA.

Live site: [anchorpartners.tech](https://anchorpartners.tech)

## Stack

Static site. Plain HTML + CSS + JS over a Bootstrap 5 template. No build step.

- `index.html` — home page (hero, about, 4 milestones, services, pricing, industries, email capture)
- `contact.html` — contact page with Formspree-wired form
- `tech-audit-checklist.pdf` — branded lead magnet (10-question tech audit). Served at `https://anchorpartners.tech/tech-audit-checklist.pdf` — attach to Formspree signup notifications to send to new subscribers.
- `css/`, `js/`, `lib/`, `scss/` — template assets
- `CNAME` — custom domain for GitHub Pages (`anchorpartners.tech`)
- `.nojekyll` — tells GitHub Pages to serve files as-is (skip Jekyll processing)

## Local preview

Open `index.html` directly in a browser, or serve the folder:

```
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploy (GitHub Pages)

1. Push this repo to GitHub.
2. In the repo settings → **Pages**, set source to `main` branch, root folder (`/`).
3. The `CNAME` file points the site at `anchorpartners.tech`. Make sure your DNS has:
   - An `A` / `ALIAS` record (or four `A` records) pointing the apex domain at GitHub Pages, **or**
   - A `CNAME` record on a subdomain pointing at `<username>.github.io`.
4. In Pages settings, enable **Enforce HTTPS** once the cert is issued.

## Integrations (already wired)

- **Zoho Bookings** — every "Schedule Now" / "Book a Free Call" button points to `https://anchorpartners.zohobookings.com/#/4936866000000034050`. If the booking service ID ever changes, search for `zohobookings.com` and update both `index.html` and `contact.html`.
- **Formspree** (ID `mzdyjvvb`) — the Tech Audit Checklist email capture on `index.html` and the contact form on `contact.html` post to `https://formspree.io/f/mzdyjvvb`. Submissions email the account owner.

## License

Template base: MIT (from HTML Codex / ThemeWagon). Content and brand are © Anchor Partners.
