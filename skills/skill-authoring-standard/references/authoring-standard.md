# Authoring Standard

## Design goal

A skill should make useful work repeatable. Treat `SKILL.md` as the complete common workflow, not a directory index that forces a second read for ordinary use.

## Progressive disclosure

Use the description as the first relevance check so the agent can skip unrelated skills. When it matches, the skill's `SKILL.md` should carry the full common workflow. Link specialized detail only when it is genuinely conditional, shared, or too large to keep clear; read that file only when its condition applies.

## Frontmatter

The Agent Skills format requires `name` and `description`. Other fields are optional. Add metadata only when it serves a real purpose:

- For a personal skill, the lean template is usually enough.
- For a distributed skill, identify the author and state a license that clearly grants the reuse rights intended.
- Add a version when maintaining releases.
- Add platform restrictions only when the instructions truly require them.
- Add catalog tags only when the target catalog uses them.

A free community does not by itself mean other people may copy, modify, or redistribute a skill. The shareable template uses CC BY 4.0: it permits reuse and adaptation, including commercially, with attribution, a license link, and notice of changes. Apply that license only to material you have the right to license; preserve third-party licenses and identify excluded material.

Some tools set stricter limits than the Agent Skills specification. The Atlas Hermes skill-creation tool enforces a 60-character description limit. Keep descriptions concise and check the limits of the target agent before publishing.

OpenAI Codex recommends plugins as the distribution unit when you want people to install reusable skills beyond a single repository or bundle integrations. A plain skill folder in a GitHub repository is suitable for direct download and Hermes skill taps. Pick the format based on where recipients will use it.

## Main file shape

Use only sections that help the specific skill, usually in this order:

1. **Name and description:** keep the required machine-readable fields at the top; add readable labels in the body if useful.
2. **Title and opening:** briefly state the task and result.
3. **When to use:** clear triggers and a counter-trigger when useful.
4. **Workflow:** the smallest complete, ordered procedure for the common case.
5. **Boundaries:** approvals, exclusions, and failure paths that matter.
6. **Supporting files:** link only to real files and state when to load them.
7. **Verification:** show what proves the task is done.

Aim for 40–80 lines only when that is enough. Keep essential workflow and safety rules in the skill even if it is longer. Never split content just to meet a line count.

## What belongs in supporting files

Use `references/` for conditional detail, troubleshooting, frameworks, or long examples; `templates/` for reusable starting artifacts; and `scripts/` for repeatable code. Keep the core procedure in `SKILL.md`. Every link must resolve within the package and explain when to use it.

## Authoring principles

- Define one clear job, a recognizable trigger, and a checkable outcome.
- Put the normal path first; branch only when the task materially differs.
- End important steps with a result that can be checked.
- Name exact tools or data sources when necessary.
- Make approvals and external-action limits explicit.
- Use concrete rules, not generic cautions or filler.
- Preserve exact names, identifiers, commands, and user-provided values.
- Adapt source material instead of copying it wholesale; retain required attribution and licensing.
- Prefer extending a suitable existing skill over creating a duplicate.

## Inspiration

Nate Herk's AIS-OS separates the operating manual from business context, decisions, and shared references. Its skills use clear triggers, boundaries, and workflows, and are mostly self-contained. Use that clear organization as inspiration while keeping each skill focused on one job.

## Verification checklist

Before sharing a skill, confirm:

- [ ] The description clearly identifies when the skill should load.
- [ ] The main file contains the complete common workflow.
- [ ] Boundaries, approvals, and failure paths are explicit where relevant.
- [ ] Supporting files are genuinely useful, present, and linked where needed.
- [ ] The frontmatter meets the target agent's requirements and limits.
- [ ] If distributing, the author and license are explicit and all included material can be shared under that license.
- [ ] The skill contains no secrets or personal/client data that should remain private.
- [ ] A reader can tell what done means and how to verify it.
