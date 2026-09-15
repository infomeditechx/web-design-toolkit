# Prompt: Website Redesign

Use this prompt when redesigning/refreshing an existing website's UI,
rather than starting from scratch.

---

I want to redesign an existing website's UI/UX. Use the `ui-ux-pro-max`
skill and the `standards/` in this repo to guide the redesign.

**Context:**
- Website type: [local service business / clinic or healthcare / real
  estate / professional services / SaaS / startup / restaurant /
  e-commerce / landing page / other]
- What's not working today: [e.g. looks dated, low conversion, not
  mobile-friendly, inconsistent branding, hard to navigate]
- What must NOT change: [e.g. brand colors are fixed, existing URL
  structure for SEO, specific content/copy]
- Tech stack: [current stack, and whether it's changing]
- Any analytics/data on current problem areas: [e.g. high bounce on
  pricing page, low mobile conversion — paste numbers if you have them]

**What I want you to do:**

1. First, audit the current site against `standards/accessibility.md`,
   `standards/responsive-design.md`, `standards/conversion-ux.md`,
   `standards/design-quality.md`, `standards/seo-basics.md`, and
   `standards/performance.md` — use `prompts/ui-ux-audit.md` /
   `workflows/design-audit.md` as the audit method. Report findings
   before changing anything.
2. Use the `ui-ux-pro-max` skill to propose a refreshed style/palette/
   typography direction that respects any constraints above.
3. Propose specific changes tied to the audit findings — prioritize
   fixes by impact (accessibility and conversion blockers first, polish
   last).
4. Implement changes incrementally so I can review each meaningful step,
   rather than a single large rewrite, unless I ask for a full rebuild.
5. Before calling the redesign "done," run through
   `workflows/pre-launch-checklist.md`.

Ask before making changes to anything listed under "what must NOT
change," and flag anywhere the redesign meaningfully affects existing
SEO (URL structure, heading structure, page titles).
