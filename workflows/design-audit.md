# Workflow: Design Audit

Structured process for auditing an existing site/page/flow. Use
`prompts/ui-ux-audit.md` as the prompt that drives this workflow inside a
Claude Code session on the target project (not in this toolkit repo).

## When to use this

- Before a redesign, to know what's actually broken (pairs with
  `prompts/website-redesign.md`).
- Periodically on a live site as a health check.
- Before launch, as a final gate (see `pre-launch-checklist.md` for the
  narrower pre-launch version of this).

## Steps

1. **Define scope.** Pick specific page(s) or flows rather than "audit
   the whole site" when possible — a checkout flow, the homepage, the
   pricing page. Note any known pain points to focus on.

2. **Run the audit prompt.** In the target project's Claude Code session
   (with `standards/` and the `ui-ux-pro-max` skill available there —
   see `new-project.md`), use `prompts/ui-ux-audit.md`, filled in for the
   scope above.

3. **Review findings by category**, in this priority order (matches
   `standards/` priority):
   - Accessibility (`standards/accessibility.md`) — critical, fix first.
   - Responsive/layout (`standards/responsive-design.md`).
   - Conversion (`standards/conversion-ux.md`) — if the page has a
     conversion goal.
   - Design quality/consistency (`standards/design-quality.md`).
   - SEO (`standards/seo-basics.md`).
   - Performance (`standards/performance.md`).

4. **Triage.** Sort findings into: fix now (critical/high severity, low
   effort), plan (high impact, higher effort), backlog (low severity/low
   impact). Don't try to fix everything in one pass.

5. **Fix and re-audit.** After implementing fixes, re-run the relevant
   part of the audit (not the whole thing) to confirm the fix landed and
   didn't regress something else.

6. **Record what changed.** Keep a short note in the project (commit
   messages are usually enough) of what the audit found and what was
   fixed, so the next audit isn't starting blind.

## Output

An audit should always produce a prioritized, actionable list — not just
a list of observations. Every finding needs: severity, location, why it
matters, and a concrete fix (this is enforced by the format in
`prompts/ui-ux-audit.md`).
