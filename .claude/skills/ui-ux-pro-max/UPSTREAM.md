# Upstream tracking

This directory is a vendored, unmodified copy of the `ui-ux-pro-max` Claude
Code skill from its upstream repository. It is pulled from the self-contained
`.claude/skills/ui-ux-pro-max/` folder of that repo (the same folder upstream
documents as the hand-maintained Claude Code skill, independent of their
`cli/` and `src/` build tooling).

- Upstream repository: https://github.com/nextlevelbuilder/ui-ux-pro-max-skill
- Vendored commit: `15de38fb70bc80ae9276fa7703b48ae861a672e6`
- Vendored version: `2.13.0` (per upstream `skill.json`)
- Vendored date: 2026-09-15
- License: MIT (see `LICENSE.md` in this directory, copied unmodified from upstream)

## Updating

See `standards/../README.md` at the repo root ("Updating UI UX Pro Max") for
the update procedure. In short:

```bash
git clone --depth 1 https://github.com/nextlevelbuilder/ui-ux-pro-max-skill.git /tmp/uupm-src
rm -rf .claude/skills/ui-ux-pro-max
cp -r /tmp/uupm-src/.claude/skills/ui-ux-pro-max .claude/skills/ui-ux-pro-max
cp /tmp/uupm-src/LICENSE .claude/skills/ui-ux-pro-max/LICENSE.md
```

Then update the commit hash, version, and date in this file, and commit.

Do not hand-edit files inside this directory (other than this `UPSTREAM.md`
file) — any local changes will be silently lost on the next sync. If the
skill genuinely needs a local customization for this toolkit, put it in
`standards/` or `prompts/` instead and reference the skill from there.
