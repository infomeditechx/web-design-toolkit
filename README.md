# Web Design Toolkit

A reusable, project-independent design toolkit for building websites with
Claude Code. It bundles the **UI UX Pro Max** Claude Code skill with a set
of vertical-agnostic design standards, ready-to-use prompts, and bootstrap
workflows, so every new website project starts from the same design
quality bar instead of reinventing it.

This repository is **not** a website, a framework, or an application. It
contains no app code, no npm packages, no databases, no APIs, and no
deployment configuration — just skills, docs, prompts, and workflows meant
to be copied into other repositories.

## Independence

This toolkit is intentionally kept **completely independent** from
NexaFlow, MrJobs, MediTechX, and every client/project repository:

- No application code, business data, credentials, environment
  variables, content, or project-specific files from any other project
  live here.
- Nothing in this repo should ever import from, depend on, or point its
  CI/build at another project — and no other project should be modified
  by working in this one.
- The only thing meant to flow *out* of this repo into a project is a
  copy of the reusable assets below (skills, standards, prompts,
  workflows). The only thing that should ever flow back *in* is a
  deliberate, reviewed improvement to those reusable assets — never
  client-specific detail.

## What's in here

```
.claude/
  skills/
    ui-ux-pro-max/        # Vendored Claude Code skill (see below)

standards/                # Vertical-agnostic design/UX rules
  accessibility.md
  responsive-design.md
  conversion-ux.md
  seo-basics.md
  performance.md
  design-quality.md

prompts/                  # Ready-to-paste prompts for common tasks
  new-website.md
  website-redesign.md
  ui-ux-audit.md
  landing-page.md

workflows/                # Step-by-step processes
  new-project.md          # Bootstrap a new project from this toolkit
  design-audit.md
  pre-launch-checklist.md
```

## What is UI UX Pro Max?

[UI UX Pro Max](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill)
is an open-source (MIT-licensed) Claude Code skill that gives Claude a
searchable, local database of UI/UX design intelligence: UI styles, color
palettes, font pairings, UX guidelines, icon recommendations, chart types,
and stack-specific implementation guidance across ~20 frameworks
(React, Next.js, Vue, Astro, Svelte, SwiftUI, Flutter, Tailwind, and
more).

It is vendored **unmodified** in this repo at
`.claude/skills/ui-ux-pro-max/`, taken directly from that folder in the
upstream repository (upstream itself documents this exact folder as the
self-contained, hand-maintained Claude Code skill — independent of their
own CLI/build tooling). See
`.claude/skills/ui-ux-pro-max/UPSTREAM.md` for the exact vendored commit,
version, and update procedure.

**Do not hand-edit files inside `.claude/skills/ui-ux-pro-max/`** other
than `UPSTREAM.md` — any local changes will be overwritten the next time
the skill is synced from upstream. If a project needs a local tweak,
layer it on top in that project's own `standards/`, don't fork the skill.

### How it's used

Once installed in a project (see below), Claude Code automatically has
access to the skill when the task is UI/UX-shaped (designing pages,
choosing colors/typography, reviewing accessibility, implementing
components, etc.) — see `SKILL.md` inside the skill folder for the exact
trigger conditions. You can also invoke its search tool directly:

```bash
python3 .claude/skills/ui-ux-pro-max/scripts/search.py "<query>" --domain <domain>
```

Domains include `product`, `style`, `typography`, `color`, `landing`,
`chart`, `ux`, `icons`, `react`, `web`, `google-fonts`, and `gsap`. Add
`--stack <name>` for framework-specific guidance. See the skill's own
`SKILL.md` for full usage.

The `standards/`, `prompts/`, and `workflows/` in this toolkit are
designed to sit on top of the skill: the skill answers "what style/
palette/pattern should I use," while `standards/` sets the non-negotiable
quality bar (accessibility, responsiveness, performance, etc.) and
`prompts/`/`workflows/` give you a repeatable process for applying both.

## Who this toolkit is for

The standards and prompts are written to be vertical-agnostic. They cover
(and are meant to be adapted, not rewritten, for):

- Local service businesses
- Clinics and healthcare
- Real estate
- Professional services
- SaaS / startups
- Restaurants
- E-commerce
- Landing pages

## How to use this toolkit when starting a new repository

Full step-by-step: `workflows/new-project.md`. Short version:

1. Clone/access this toolkit locally.
2. In the new project repo, copy `.claude/skills/ui-ux-pro-max/` in
   as-is.
3. Copy the `standards/` and `prompts/` files relevant to that project
   (or all of them — delete what doesn't apply).
4. Start a Claude Code session in the new project and open with
   `prompts/new-website.md`, filled in with the project's brief.

## How to copy only the required reusable assets into another project

You rarely need the whole toolkit in every project. Typical picks:

- **Always**: `.claude/skills/ui-ux-pro-max/` (the skill itself).
- **Almost always**: `standards/accessibility.md`,
  `standards/responsive-design.md`, `standards/design-quality.md`.
- **If the site has a conversion goal** (most do):
  `standards/conversion-ux.md`.
- **If SEO/performance are in scope for this engagement**:
  `standards/seo-basics.md`, `standards/performance.md`.
- **Prompts**: copy the one matching the task —
  `prompts/new-website.md`, `prompts/website-redesign.md`,
  `prompts/ui-ux-audit.md`, or `prompts/landing-page.md`.
- **Workflows**: `workflows/pre-launch-checklist.md` is worth copying
  into almost every project; `workflows/design-audit.md` only if you'll
  run audits there.

See `workflows/new-project.md` for the exact copy commands.

## Using a prompt

Each file in `prompts/` is a fill-in-the-blanks template for a specific
kind of task (new site, redesign, audit, landing page). Copy the
relevant one into the target project (or just read it from this repo),
fill in the bracketed project details, and paste it into a Claude Code
session in that project. The prompts reference the skill and the
`standards/` files by path, so make sure those are present in the target
project first (step 2–3 above).

## Updating UI UX Pro Max

The skill is vendored, not linked, so updates are a manual, deliberate
sync — this keeps this toolkit (and every project that copied from it)
independent of upstream's release cadence and free of surprise breaking
changes.

**To update this toolkit's copy:**

```bash
git clone --depth 1 https://github.com/nextlevelbuilder/ui-ux-pro-max-skill.git /tmp/uupm-src
rm -rf .claude/skills/ui-ux-pro-max
cp -r /tmp/uupm-src/.claude/skills/ui-ux-pro-max .claude/skills/ui-ux-pro-max
cp /tmp/uupm-src/LICENSE .claude/skills/ui-ux-pro-max/LICENSE.md
```

Then update the commit hash, version, and date recorded in
`.claude/skills/ui-ux-pro-max/UPSTREAM.md`, review the diff, and commit.

**To pull an update into an already-bootstrapped project**, repeat the
"copy the skill in" step from `workflows/new-project.md` in that
project — it's the same clean folder overwrite, just targeting the
project repo instead of this toolkit.

Never edit the vendored skill files by hand; always re-sync from
upstream so the next update doesn't silently discard local edits.

## What this toolkit deliberately does not include

No frameworks, no npm/pip packages, no application code, no databases, no
APIs, no deployment/CI configuration, and no business/client data of any
kind. This is a design-intelligence and process toolkit, meant to be
copied from — not a runnable application.

## License

The `ui-ux-pro-max` skill is MIT-licensed by NextLevelBuilder — see
`.claude/skills/ui-ux-pro-max/LICENSE.md`. The `standards/`, `prompts/`,
and `workflows/` content in this repo is original to this toolkit.
