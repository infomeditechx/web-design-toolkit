# Accessibility Standard

Applies to every website type in this toolkit (service business, clinic,
real estate, professional services, SaaS, startup, restaurant, e-commerce,
landing page). Target: WCAG 2.1 AA as a floor, not a ceiling.

## Non-negotiable checks

- **Color contrast**: body text ≥ 4.5:1, large text (≥ 24px or ≥ 19px bold)
  ≥ 3:1, and non-text UI elements (icon buttons, form borders, focus rings)
  ≥ 3:1 against their background.
- **Keyboard navigation**: every interactive element (links, buttons, form
  fields, menus, modals, carousels) is reachable and operable with Tab /
  Shift+Tab / Enter / Space / Escape alone. No keyboard traps.
- **Visible focus state**: never remove `outline` without replacing it with
  an equally visible custom focus style. Focus order follows visual/reading
  order.
- **Alt text**: every informative image has descriptive `alt`; purely
  decorative images use `alt=""` (not omitted). Icon-only buttons get an
  `aria-label`, never rely on a tooltip alone.
- **Forms**: every input has a visible, programmatically associated
  `<label>` (placeholder text is not a label). Errors are announced near
  the field, not only in a summary at the top, and are associated via
  `aria-describedby`.
- **Semantic structure**: one `<h1>` per page, headings in order (no
  skipped levels), landmark regions (`header`, `nav`, `main`, `footer`),
  lists marked up as `<ul>/<ol>`, buttons are `<button>` and links are
  `<a>` — never a `<div onclick>`.
- **Touch targets**: minimum 44×44px hit area with ≥ 8px spacing between
  adjacent targets, for every device, not just "mobile breakpoints."
- **Motion**: respect `prefers-reduced-motion`; no auto-playing content
  that moves, flashes more than 3 times/second, or cannot be paused.
- **Zoom/scale**: never disable pinch-zoom or set `maximum-scale=1` /
  `user-scalable=no` in the viewport meta tag.

## Review checklist (use before calling a page "done")

1. Tab through the entire page — can you reach and operate everything?
2. Turn off color — does the page still make sense (icons, states, errors)?
3. Zoom to 200% — does layout still work without horizontal scroll?
4. Run a contrast checker on body text, buttons, and links.
5. Check that every form field announces its label and any error via a
   screen reader (or inspect the accessibility tree in devtools).

## Where to go deeper

Use the `ui-ux-pro-max` skill's `ux` domain search for the full rule set
(119 guidelines) and rationale — see `prompts/ui-ux-audit.md` for the
audit workflow that wires this in.
