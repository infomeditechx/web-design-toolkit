# Workflow: Bootstrap a New Project From This Toolkit

This is the step-by-step bootstrap procedure for starting a brand-new
website repository using this toolkit as the source. It only copies
reusable design assets — never application code, credentials, or content
from any existing project.

## Prerequisites

- This toolkit repo (`web-design-toolkit`) cloned or accessible locally.
- A new, separate git repository already created for the website project
  (this workflow does not create that repository for you).

## Steps

### 1. Locate this toolkit locally

If you don't already have it:

```bash
git clone <this-toolkit-repo-url> ~/web-design-toolkit
```

### 2. In the new project repo, copy in the skill

The `ui-ux-pro-max` skill is self-contained — copy the whole folder
as-is:

```bash
cd /path/to/new-website-project
mkdir -p .claude/skills
cp -r ~/web-design-toolkit/.claude/skills/ui-ux-pro-max .claude/skills/ui-ux-pro-max
```

Do not edit files inside `.claude/skills/ui-ux-pro-max/` in the new
project — treat it as a vendored dependency. If it needs project-specific
tuning, do that in the new project's own `standards/` copy instead (next
step), and reference the skill from there.

### 3. Copy the standards and prompts relevant to this project

You rarely need everything — copy what applies. At minimum:

```bash
mkdir -p standards prompts
cp ~/web-design-toolkit/standards/accessibility.md standards/
cp ~/web-design-toolkit/standards/responsive-design.md standards/
cp ~/web-design-toolkit/standards/design-quality.md standards/
# add conversion-ux.md, seo-basics.md, performance.md as relevant
cp ~/web-design-toolkit/prompts/new-website.md prompts/
```

Or, for a quick start, copy everything and delete what doesn't apply:

```bash
cp -r ~/web-design-toolkit/standards standards
cp -r ~/web-design-toolkit/prompts prompts
```

### 4. Tell Claude Code about the project

In the new repo, start a Claude Code session and use
`prompts/new-website.md` as your starting prompt, filling in the project
brief (business type, audience, goal, stack, pages).

### 5. Keep the toolkit and the project independent

- Never add this toolkit repo as a git submodule/subtree of a client
  project, and never point a client project's CI/build at this repo.
- Never commit client business data, credentials, `.env` files, or
  content back into this toolkit.
- If you improve a standard or prompt while working on a client project
  and want it reusable, port the improvement back into
  `web-design-toolkit` as a separate, deliberate change — don't let
  client-specific detail leak in when you do.

## Updating an existing project later

If `ui-ux-pro-max` has been updated upstream and you want the new
version in an already-bootstrapped project, repeat step 2 (it's a clean
overwrite of that one folder) — see the root `README.md`, "Updating UI
UX Pro Max."
