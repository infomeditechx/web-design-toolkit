# Workflow: Pre-Launch Checklist

Run through this before calling any website/page "done" and shipping it.
It's a fast gate, not a full audit (see `design-audit.md` for the deeper
version) — the goal is to catch the most common, most costly mistakes
before launch.

## Accessibility (`standards/accessibility.md`)

- [ ] Tab through the whole page — everything reachable and operable by
      keyboard, visible focus states throughout.
- [ ] Every image has correct `alt` (descriptive or `alt=""` for
      decorative).
- [ ] Every form field has a real, associated `<label>`.
- [ ] Body text contrast checked (≥ 4.5:1).
- [ ] `prefers-reduced-motion` respected on any animation.

## Responsive (`standards/responsive-design.md`)

- [ ] No horizontal scroll at 375px, 768px, 1024px, 1440px.
- [ ] Viewport meta present, zoom not disabled.
- [ ] Nav collapses to a usable mobile pattern.
- [ ] Tap targets ≥ 44×44px on mobile.

## Conversion (`standards/conversion-ux.md`, if the page has a goal)

- [ ] One clear primary CTA, above the fold where relevant.
- [ ] CTA copy states the outcome, not just "Submit."
- [ ] Forms ask only for what's needed; inline validation with clear
      error copy.
- [ ] Trust signals present near the decision point (if applicable to
      the business type).

## Design quality (`standards/design-quality.md`)

- [ ] Spacing, type, and color consistent across the page(s).
- [ ] Hover/focus/active/disabled/loading/empty/error states all
      designed, not just the default state.
- [ ] No lorem-ipsum or placeholder imagery left in — or if some
      remains intentionally (no real data yet), it's clearly flagged as
      placeholder.

## SEO (`standards/seo-basics.md`)

- [ ] Unique `<title>` and meta description per page.
- [ ] One `<h1>` per page, logical heading order.
- [ ] `robots.txt` and `sitemap.xml` present and correct.
- [ ] HTTPS, canonical URLs, no accidental `noindex`.

## Performance (`standards/performance.md`)

- [ ] Images sized/compressed appropriately, modern formats, lazy-loaded
      below the fold (hero image eager-loaded).
- [ ] No obvious layout shift on load (check LCP element has reserved
      space).
- [ ] Third-party scripts (analytics, chat, ads) loaded async/deferred.

## Final pass

- [ ] Real content/copy in place — no placeholder business facts,
      fabricated testimonials, or fake contact details.
- [ ] Links checked (no dead links, correct targets, `mailto:`/`tel:`
      links work).
- [ ] Cross-browser sanity check (at minimum Chrome + Safari, or
      whatever the project's actual audience uses).
- [ ] 404 page exists and is useful.

If anything fails, fix it before launch — this checklist exists because
these are the mistakes that are expensive to fix after users have
already hit them.
