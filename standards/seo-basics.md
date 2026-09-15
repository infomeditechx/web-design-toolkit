# SEO Basics Standard

Baseline technical/on-page SEO to apply to any new site or page, regardless
of vertical. This is not a marketing/content-strategy doc — it's the
structural minimum every page should ship with.

## Per-page checklist

- **Title tag**: unique per page, ~50–60 characters, primary keyword near
  the front, brand name at the end (`Page Topic | Brand`).
- **Meta description**: unique per page, ~150–160 characters, written as
  a compelling summary (it affects click-through, not ranking directly).
- **One `<h1>`** per page that matches the page's actual topic; heading
  hierarchy below it is logical (no skipped levels, no headings chosen
  for size instead of structure).
- **Canonical tag** (`<link rel="canonical">`) on every page, especially
  where URL parameters or duplicate paths could exist.
- **Semantic HTML**: real `<nav>`, `<main>`, `<article>`, `<footer>` —
  search engines and screen readers both benefit from this, it's not
  redundant with accessibility work.
- **Descriptive URLs**: `/services/roof-repair` beats `/page?id=4821`.
- **Image alt text**: doubles as SEO and accessibility — don't treat
  them as separate tasks.
- **Structured data (schema.org / JSON-LD)** where it matches the content:
  `LocalBusiness` for service/clinic sites, `Product`/`Offer` for
  e-commerce, `Article` for blog content, `FAQPage` for FAQ sections,
  `Review`/`AggregateRating` where genuine reviews exist.

## Site-level checklist

- `robots.txt` present and not accidentally blocking the whole site.
- `sitemap.xml` present and linked from `robots.txt`, kept in sync with
  real pages.
- HTTPS everywhere, no mixed content.
- One canonical domain (redirect `www` ↔ non-`www`, trailing slash
  consistency) — pick one and 301-redirect the rest.
- 404 page that helps the user get back on track (nav + search), not a
  dead end.
- Mobile-friendly (see `responsive-design.md`) — mobile-first indexing
  means this is an SEO requirement, not just a UX one.

## Performance ties into SEO

Core Web Vitals (LCP, CLS, INP) are ranking factors. See
`performance.md` — don't treat SEO and performance as separate
workstreams.

## Local business specifics

- Consistent NAP (Name, Address, Phone) across the site and matching the
  Google Business Profile listing.
- `LocalBusiness` structured data with correct `address`, `geo`,
  `openingHours`, and `telephone`.
- A dedicated, crawlable page per location if the business has more than
  one.

## What this doc does not cover

Keyword research, content strategy, link building, and analytics/tag
setup are project-specific and out of scope for a reusable structural
checklist — handle those per engagement.
