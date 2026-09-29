# Skill Authoring Standard

A reusable guide and two templates for writing skills with clear triggers, a useful workflow, and progressive disclosure.

- `skills/skill-authoring-standard/SKILL.md` is the authoring skill. Install it in your agent, then invoke it when you create or revise a skill.
- `templates/skill-template.md` is the lean starting point for a personal skill.
- `templates/skill-template-shareable.md` is for a skill intended for distribution. It uses CC BY 4.0; replace the author placeholder before publishing.
- `references/authoring-standard.md` contains the detailed rules and final checklist.

## Install in Hermes

For direct install without adding a source:

```bash
hermes skills install MrRebech/skill-authoring-standard/skills/skill-authoring-standard
```

Or add the repository as a tap, then install the skill:

```bash
hermes skills tap add MrRebech/skill-authoring-standard
hermes skills install MrRebech/skill-authoring-standard/skill-authoring-standard
```

Start a fresh Hermes session after installation, then invoke `/skill-authoring-standard`.

## Install in Codex

Copy the entire `skills/skill-authoring-standard` folder into either `~/.agents/skills/` for your user or `.agents/skills/` in a repository. In Codex, select it with `$skill-authoring-standard`.

The skill includes its reference and templates. Keep the whole folder together so its relative links continue to work.

## License

Original content in this repository by Kenneth (MrRebech) is licensed under [Creative Commons Attribution 4.0 International](https://creativecommons.org/licenses/by/4.0/). Reuse is allowed, including commercial reuse, with appropriate attribution, a link to the license, and notice of changes. See `LICENSE`.
