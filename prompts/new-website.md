# Prompt: New Website

Use this prompt (paste it into Claude Code, filling in the brackets) when
starting a brand-new website project in its own repository that has this
toolkit's assets installed (see `workflows/new-project.md`).

---

I'm starting a new website project. Use the `ui-ux-pro-max` skill and the
`standards/` in this repo to guide every design and UI decision.

**Project brief:**
- Business/product name: [NAME]
- Website type: [choose one: local service business / clinic or
  healthcare / real estate / professional services / SaaS / startup /
  restaurant / e-commerce / landing page / other — describe]
- Target audience: [who are they, what do they need]
- Primary goal of the site: [e.g. generate booking calls, sell products
  online, collect signups, build credibility]
- Tone/personality: [e.g. warm and reassuring, bold and modern, premium
  and understated]
- Tech stack: [e.g. HTML+Tailwind, React, Next.js, Astro — see the
  `ui-ux-pro-max` skill's supported stacks; default to HTML+Tailwind if
  unsure]
- Pages needed: [e.g. Home, About, Services, Contact, Pricing]
- Must-have content/sections: [e.g. testimonials, service area map,
  pricing table, booking form]
- Brand assets available: [logo, colors, fonts — or "none, please
  suggest"]

**What I want you to do:**

1. Use the `ui-ux-pro-max` skill to recommend a style, color palette, and
   typography pairing appropriate for this website type and audience
   (`product`, `style`, `color`, `typography` domains).
2. Propose a page/section structure and CTA strategy appropriate for the
   primary goal (`landing` domain for structure, `standards/conversion-ux.md`
   for CTA rules).
3. Build the pages using the chosen stack, applying:
   - `standards/accessibility.md`
   - `standards/responsive-design.md`
   - `standards/design-quality.md`
   - `standards/seo-basics.md`
   - `standards/performance.md`
4. Before calling anything "done," run through
   `workflows/pre-launch-checklist.md`.

Ask me anything you need clarified before starting (brand assets, exact
copy, real contact details) rather than inventing placeholder business
facts.
