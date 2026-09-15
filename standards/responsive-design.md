# Responsive Design Standard

Mobile-first. Design and build the smallest viewport first, then enhance
upward — never the reverse.

## Breakpoint baseline

Use these as defaults; adjust per project, but keep the mobile-first
mindset regardless of the exact pixel values chosen:

| Range | Typical target |
|---|---|
| < 480px | Small phones |
| 480–767px | Large phones |
| 768–1023px | Tablets / small laptops |
| 1024–1439px | Laptops / desktops |
| ≥ 1440px | Large desktops |

## Rules

- **No horizontal scroll**, ever, at any viewport width — this is the
  single most common regression to check for.
- **Fluid by default**: prefer `%`, `rem`, `clamp()`, `minmax()`, and
  CSS Grid/Flexbox over fixed pixel widths for containers and type.
- **Viewport meta**: `<meta name="viewport" content="width=device-width,
  initial-scale=1">` — never lock scale or disable zoom.
- **Images**: always responsive (`srcset`/`sizes` or CSS `max-width:100%`),
  served in modern formats (WebP/AVIF) with explicit `width`/`height` (or
  `aspect-ratio`) to reserve layout space and avoid CLS.
- **Touch vs. hover**: never gate essential functionality behind
  `:hover` alone — every hover-revealed action needs a touch/click
  equivalent.
- **Navigation**: collapse to a mobile pattern (hamburger, bottom nav,
  tab bar) below the tablet breakpoint; keep primary actions reachable
  within one tap.
- **Typography**: base body text ≥ 16px on mobile (prevents iOS
  auto-zoom on input focus), line-height ≥ 1.5 for body copy.
- **Test on real breakpoints**: 375px (small phone), 768px (tablet),
  1024px (laptop), 1440px (desktop) at minimum, plus the exact width
  where your layout changes columns.

## Layout-type notes

- **Service/clinic/real-estate/restaurant sites**: prioritize the
  above-the-fold mobile experience — most traffic for local businesses is
  mobile search. Click-to-call and tap-to-map must work without zooming.
- **SaaS/dashboard UIs**: dense desktop layouts should degrade to
  stacked cards or a simplified table view on mobile, not a shrunk
  version of the desktop grid.
- **E-commerce**: product grids should reflow (e.g. 4 → 2 → 1 columns),
  and the cart/checkout flow must be fully usable one-handed on mobile.

## Where to go deeper

The `ui-ux-pro-max` skill's `ux` domain covers layout and responsive
anti-patterns in more depth; the `stack` search (`--stack <name>`) gives
framework-specific responsive patterns (Tailwind, React, etc.).
