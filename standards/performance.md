# Performance Standard

Target Core Web Vitals thresholds as the baseline for "good" on every
project, regardless of stack:

| Metric | Good | Needs work | Poor |
|---|---|---|---|
| LCP (Largest Contentful Paint) | ≤ 2.5s | ≤ 4.0s | > 4.0s |
| INP (Interaction to Next Paint) | ≤ 200ms | ≤ 500ms | > 500ms |
| CLS (Cumulative Layout Shift) | ≤ 0.1 | ≤ 0.25 | > 0.25 |

## Images

- Serve modern formats (WebP/AVIF) with sensible fallbacks.
- Always set explicit `width`/`height` or `aspect-ratio` to reserve
  space and prevent layout shift.
- Lazy-load below-the-fold images (`loading="lazy"`); do NOT lazy-load
  the hero/LCP image — eager-load it instead.
- Serve responsive sizes via `srcset`/`sizes` rather than one oversized
  image scaled down by CSS.

## Fonts

- Self-host or use `font-display: swap` (or `optional`) to avoid
  invisible-text flashes and layout shift from late-loading web fonts.
- Limit font families/weights to what's actually used — each extra
  weight is a separate network request.
- Preload the critical above-the-fold font file(s) only.

## JavaScript & CSS

- Avoid layout thrashing: batch DOM reads/writes, animate `transform`/
  `opacity` instead of `width`/`height`/`top`/`left`.
- Code-split and lazy-load non-critical JS (below-the-fold widgets,
  modals, heavy third-party embeds).
- Defer or async non-critical third-party scripts (analytics, chat
  widgets, ads) — they should never block first paint.
- Minify/bundle for production; ship only the CSS actually used on the
  page (avoid shipping an entire unused component library's styles).

## Layout stability (CLS)

- Reserve space for ads, embeds, and async-loaded content before it
  loads.
- Never insert content above existing content unless in direct response
  to a user interaction.
- Reserve space for web fonts if a fallback metric-compatible font isn't
  used.

## Third parties

- Audit third-party scripts (chat widgets, tag managers, A/B test
  tools) — each one is a performance and privacy cost. Load them async
  and only where actually needed, not site-wide by default.

## Where to go deeper

The `ui-ux-pro-max` skill's `ux` domain and `--stack` search surface
framework-specific performance patterns (React re-render pitfalls,
Next.js image/font optimization, etc.) via the `react` domain and stack
guidelines.
