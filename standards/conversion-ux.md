# Conversion UX Standard

Applies whenever a page exists to make something happen: a booking, a
lead form, a call, a purchase, a signup, a demo request.

## Above the fold

- State what the business/product is and who it's for within one glance
  — no cleverness before clarity.
- One primary call-to-action (CTA), visually dominant, above the fold.
  Secondary CTAs (e.g. "Learn more") should be visually subordinate.
- If trust is a blocker (healthcare, finance, home services), surface a
  trust signal near the fold: credentials, reviews/rating, years in
  business, certifications, "as seen in," etc.

## CTA design

- CTA copy states the outcome, not the mechanism: "Book your free
  consult" beats "Submit." "Start free trial" beats "Sign up."
- One CTA style = one meaning. Don't reuse the primary button style for
  low-commitment actions.
- Every CTA has a visible hover/focus/active state and, where relevant,
  a loading state so a click always gets feedback within ~100ms.

## Forms

- Ask for the minimum viable information to take the next step. Every
  extra field measurably reduces completion.
- Group related fields, use progressive disclosure for optional/advanced
  fields rather than showing everything at once.
- Inline validation with specific, actionable error copy ("Enter a valid
  phone number" not "Invalid input"), shown near the field.
- Show progress on multi-step forms/checkouts (e.g. "Step 2 of 3").

## Friction and trust

- Never require account creation before showing value (pricing, a demo,
  a guest checkout option) unless the business model requires it.
- Show pricing/cost implications before the final commitment step —
  surprise costs at checkout are a top cause of abandonment.
- Testimonials/case studies/reviews near decision points (pricing,
  checkout, contact form) — not only on a separate "testimonials" page.
- For local/service businesses: make phone number and address
  click-to-call / tap-to-map, and visible without scrolling on mobile.

## Page-type notes

- **Landing pages**: single conversion goal per page. Remove nav links
  that lead away from the goal (or minimize them) for paid-traffic
  landing pages.
- **SaaS pricing**: highlight the recommended/most popular tier, make
  plan differences scannable in a comparison table, and put the CTA in
  the same position on every plan card.
- **E-commerce**: persistent cart visibility, clear shipping/returns
  info before checkout, guest checkout available.
- **Restaurants/local services**: reservation/booking or call CTA
  repeated at natural scroll checkpoints, not just in the header.

## Where to go deeper

Use the `ui-ux-pro-max` skill's `landing` domain for page-structure and
CTA-strategy lookups, and `prompts/landing-page.md` for a full build
workflow.
