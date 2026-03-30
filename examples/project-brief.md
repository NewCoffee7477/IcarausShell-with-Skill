# Example Project Brief

Create a standalone skill repository named `<PROJECT_NAME>` for public sharing.

Requirements:
- The repo root is also the skill root.
- Include `SKILL.md`, `agents/openai.yaml`, `references/`, `examples/`, `README.md`, `.gitignore`, and one canonical `scaffold.MD`.
- The scaffold must embed the literal IcarusShell++ Core and track Shells, Shards, contracts, tests, ambiguities, decisions, lessons, tool usage, and execution history.
- All examples must be sanitized and use repo-relative paths only.
- The repo must be ready for a later `git init`, but do not initialize git during setup.

Constraints:
- No personal names
- No absolute home paths
- No machine-specific identifiers
- No connector or plugin instance IDs
- No copied workspace-specific examples

Success criteria:
- Another operator can clone or copy the folder, initialize git, and understand how to extend the skill without seeing any local-only context.
