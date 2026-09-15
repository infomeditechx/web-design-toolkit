# Prompt: UI/UX Audit

Use this prompt to get a structured audit of an existing page, flow, or
whole site — without making changes yet. Pairs with
`workflows/design-audit.md`.

---

Audit [the page at URL / the component at PATH / this whole site] for
UI/UX quality. Use the `ui-ux-pro-max` skill and the `standards/` in this
repo as your rubric. Do not make changes — report findings only, unless I
ask you to fix them afterward.

**Scope:**
- What to audit: [specific page(s), flow (e.g. checkout), or full site]
- Known pain points, if any: [optional — e.g. "conversion seems low on
  mobile" or leave blank for a fully open audit]

**Audit against, in priority order:**

1. `standards/accessibility.md` — contrast, keyboard nav, focus states,
   alt text, forms, semantic structure, touch targets, motion.
2. `standards/responsive-design.md` — breakpoints, horizontal scroll,
   touch vs. hover, image responsiveness.
3. `standards/conversion-ux.md` — CTA clarity, form friction, trust
   signals (only if the page has a conversion goal).
4. `standards/design-quality.md` — consistency of spacing/type/color,
   states (hover/focus/loading/empty/error), hierarchy.
5. `standards/seo-basics.md` — titles, meta, headings, structured data,
   canonical/URL hygiene (only if in scope).
6. `standards/performance.md` — Core Web Vitals concerns, image/font/JS
   loading.

Use the `ui-ux-pro-max` skill's `ux` domain search for the full 119-rule
guideline set where you need more depth than the standards summaries give
you, and cite specific rules/anti-patterns you find violated.

**Output format:**

For each finding: severity (critical/high/medium/low), where it is
(page/component/line if known), what's wrong, why it matters (user
impact), and a concrete fix. Group findings by the standards category
above. End with a prioritized top-5 "fix these first" list.
