# icarusshell-skill-kit

`icarusshell-skill-kit` is a standalone, public-safe starter for a reusable Codex skill that bootstraps new projects with a canonical IcarusShell++ `scaffold.MD`.

The repository root is also the skill root. This starter is intentionally documentation-first: it includes the skill definition, interface metadata, scaffold reference, privacy scrub guidance, and a sanitized example brief. It does not include scripts, dependencies, a license choice, or an initialized git repository.

The scaffold structure in this repo is aligned to the `scaffold-icarusshellpp` workflow: one canonical root `scaffold.MD`, the literal immutable Core block, and explicit Shell, Shard, contract, test, ambiguity, decision, lesson, tool-usage, and execution sections.

## Start Here

If you want a raw scaffold template and do not want to install or use the skill, copy one of these files directly:

- `TEMPLATE-scaffold.DaedalusShell.MD` for the full Daedalus-plus-Icarus contract path
- `TEMPLATE-scaffold.IcarusShell.MD` for the lighter pure-Icarus contract path

If you want the guided workflow, use the skill in `SKILL.md`.

## Included Files

- `TEMPLATE-scaffold.DaedalusShell.MD` is the full raw template artifact for direct copy use
- `TEMPLATE-scaffold.IcarusShell.MD` is the pure-Icarus raw template artifact for direct copy use
- `SKILL.md` defines the bootstrap skill trigger and workflow
- `agents/openai.yaml` provides UI-facing metadata
- `references/scaffold-shape.md` defines the full Icarus scaffold reference
- `references/privacy-scrub-checklist.md` defines release-time privacy checks
- `examples/project-brief.md` shows a sanitized bootstrap brief
- `scaffold.MD` is the canonical source of truth for this project
- `.gitignore` ignores standard OS and editor clutter only

## Privacy Posture

This starter is designed for public sharing. Documentation and examples use neutral placeholders and repo-relative paths so the project can be published without exposing local operator details.

## Next Step

Initialize git when you are ready, then extend the skill or references as your workflow requires.
