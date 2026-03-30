---
name: public-icarusshell-bootstrap
description: Initialize a new public-safe project with a portable repository layout, a canonical IcarusShell++ scaffold.MD, and privacy-scrubbed examples and references. Use this when creating a shareable skill or starter project that must avoid personal names, home paths, machine identifiers, connector IDs, and other local-only context.
---

# Public IcarusShell Bootstrap

Use this skill to start a portable project that is safe to publish.

## Raw Templates

If you do not want to install or use the skill, copy one of these root-level files directly:

- [`TEMPLATE-scaffold.DaedalusShell.MD`](TEMPLATE-scaffold.DaedalusShell.MD) for the full Daedalus-plus-Icarus contract path
- [`TEMPLATE-scaffold.IcarusShell.MD`](TEMPLATE-scaffold.IcarusShell.MD) for the lighter pure-Icarus contract path

Typical triggers:
- create a new standalone skill repository
- initialize a privacy-safe `scaffold.MD`
- prepare a project for later `git init`
- replace local-only examples with neutral placeholders

## Quick Start

1. Create the project root and keep it standalone.
2. Add one canonical `scaffold.MD` at the repo root.
3. Add only the minimum skill files needed for reuse:
   - `SKILL.md`
   - `agents/openai.yaml`
   - `references/`
   - `examples/`
   - minimal repo metadata
4. Apply the privacy scrub checklist before delivery.

## Default Workflow

1. Inspect the target directory and confirm there is no competing source-of-truth document.
2. Create or update the repo root as the skill root.
3. Choose the raw template path first when the user only wants a copyable contract file:
   - [`TEMPLATE-scaffold.DaedalusShell.MD`](TEMPLATE-scaffold.DaedalusShell.MD)
   - [`TEMPLATE-scaffold.IcarusShell.MD`](TEMPLATE-scaffold.IcarusShell.MD)
4. Build or adapt the project scaffold using the required section order and literal immutable Core from [`references/scaffold-shape.md`](references/scaffold-shape.md).
5. Keep the skill body concise and move detailed guardrails into references.
6. Use neutral placeholders in every example and avoid absolute paths.
7. Run the privacy scrub checks from [`references/privacy-scrub-checklist.md`](references/privacy-scrub-checklist.md).

## Output Contract

- Produce a standalone, shareable repo-shaped skill.
- Keep exactly one canonical `scaffold.MD` at the project root.
- Expose raw root-level template files for users who only want copyable scaffold contracts.
- Avoid personal names, usernames, absolute home paths, machine names, connector IDs, and workspace-specific examples.
- Prefer repo-relative paths in documentation and examples.
- Do not add scripts, dependencies, or licenses unless explicitly requested.

## References

- [`TEMPLATE-scaffold.DaedalusShell.MD`](TEMPLATE-scaffold.DaedalusShell.MD)
- [`TEMPLATE-scaffold.IcarusShell.MD`](TEMPLATE-scaffold.IcarusShell.MD)
- [`references/scaffold-shape.md`](references/scaffold-shape.md)
- [`references/privacy-scrub-checklist.md`](references/privacy-scrub-checklist.md)

## Examples

- [`examples/project-brief.md`](examples/project-brief.md)
