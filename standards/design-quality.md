# Design Quality Standard

Baseline visual-quality bar, independent of which style/palette a project
chooses (see the `ui-ux-pro-max` skill for style/palette selection itself).

## Consistency

- One spacing scale, used everywhere (e.g. 4/8px base scale) — no
  arbitrary one-off margin/padding values.
- One type scale, a limited set of font sizes/weights, applied
  consistently for the same semantic purpose (all H2s look like H2s).
- A defined, limited color palette used via semantic tokens (`primary`,
  `surface`, `danger`, ...), not raw hex codes scattered through
  components.
- Consistent corner radius, shadow, and border treatment across similar
  components (all cards, all buttons, all inputs).

## Iconography & imagery

- One icon set per project (e.g. Phosphor, Heroicons, Lucide) — never
  mix icon styles.
- No emoji used as functional icons in production UI.
- Real, relevant imagery over generic stock photography where feasible;
  never placeholder/lorem-ipsum imagery in a "done" deliverable.

## States & feedback

- Every interactive element has defined hover, focus, active, and
  disabled states — not just a default state.
- Loading, empty, and error states are designed, not an afterthought —
  every list/table/data view needs all three.
- Feedback for user actions (save, submit, delete) is visible within
  ~100ms, even if it's just an optimistic UI update or a spinner.

## Hierarchy & clarity

- Every screen has one clear primary action; secondary/tertiary actions
  are visually subordinate.
- Whitespace is used deliberately to group related elements and separate
  unrelated ones (proximity = relationship).
- Text contrast and size create clear reading order — don't rely on
  color alone to indicate importance or state.

## Motion

- Motion has a purpose (orient, connect, guide attention) — not
  decoration for its own sake.
- Consistent easing/duration per interaction category (micro-
  interactions fast, page transitions slower).
- Respect `prefers-reduced-motion`.

## Pre-delivery pass

Before calling any page/component "done," do a final quality pass:

1. Does every interactive element have all states designed?
2. Is spacing/type/color consistent with the rest of the site?
3. Would this look intentional to a design-literate reviewer, or does it
   look like defaults?
4. Run it through `standards/accessibility.md` and
   `standards/responsive-design.md` as well — visual quality and
   accessibility/responsiveness are not separate passes.

## Where to go deeper

Use the `ui-ux-pro-max` skill's `style`, `color`, and `typography`
domains to pick and apply a coherent style system, and its `pro-rules`
reference for the canonical pre-delivery checklist.
