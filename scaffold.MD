# scaffold.MD

## IcarusShell++ Core (Immutable)

1. **Recursive Task Decomposition:**  
   All project goals are broken down hierarchically into Shells (modules/tasks) and Shards (sub-tasks/atomic units), recursively, until each unit is minimal, actionable, and verifiable.

2. **Persistent Memory and Scaffold:**  
   All knowledge, plans, decisions, outputs, and lessons learned are recorded in `scaffold.MD`. This document is continuously updated and serves as the external, persistent memory for all agents and processes.

3. **Autonomous Execution and Reflection:**  
   All agents (at every layer) autonomously plan, execute, test, and reflect on their outputs. Reflection and self-correction are built into every loop, with all insights and improvements documented in the Scaffold.

4. **MCP Tool Use (Model Context Protocol):**  
   The system must utilize all available MCP tools and data sources at its disposal to access real-time information, perform actions, and ground its outputs in accurate, up-to-date data.  
   - **Definition:** MCP (Model Context Protocol) is an open standard for connecting AI assistants to external data sources and tools, enabling standardized, modular, and context-aware tool and data integration.
   - **Scope:** In IcarusShell++, MCP is used exclusively for tool and data source integration. MCP is **not** used for orchestrating or cascading between different AI models.
   - **Operation:** Always invoke MCP-enabled tools for data access, tool usage, and action execution. Document all MCP tool usage and results in `scaffold.MD` for transparency and reproducibility.
   - **Architecture:** MCP follows a client-server model, with the AI as the client and MCP servers exposing data and functionalities.

5. **Continuous Learning and Adaptation:**  
   The system continuously incorporates new knowledge, feedback, and lessons learned into the Scaffold. All failures, successes, and process improvements are documented and used to adapt future behavior.

6. **Explicit Contracts and Interfaces:**  
   All modules, tasks, and sub-tasks define explicit, measurable contracts and interfaces. These are recorded in the Scaffold and used to ensure integration and verification across all layers.

7. **Holistic Integrity and Minimalism:**  
   The system maintains holistic project coherence, avoids unnecessary complexity, and ensures all decomposition and orchestration is minimal and justified.

8. **Immutability of Core:**  
   The IcarusShell++ Core section in `scaffold.MD` is immutable and may only be revised with explicit human approval. The system must never autonomously alter or update the Core section except when explicitly instructed by the human user.

## Project Overview

This project packages a standalone, public-safe bootstrap skill for creating shareable repositories with a canonical IcarusShell++ `scaffold.MD`. The repo root is the skill root. The project now serves two audiences in parallel: users who want the skill workflow and users who only want raw copyable scaffold templates. The release remains documentation-first and intentionally excludes scripts, dependencies, git initialization, and license selection.

## Authoritative Inputs

1. The explicit project request to build a standalone, public-safe skill repository named `icarusshell-skill-kit`
2. The requirement that the skill be named `public-icarusshell-bootstrap`
3. The requirement to keep one canonical `scaffold.MD` at the repo root
4. The requirement to exclude personal information, local-only paths, connector identifiers, and copied workspace examples
5. The requirement to prepare the repo for later git initialization without initializing git now
6. The scaffold structure and immutable Core are derived from the `scaffold-icarusshellpp` skill workflow and the full `references/scaffold-shape.md` reference
7. The repo must expose clearly named root-level raw template artifacts for both the full Daedalus-plus-Icarus contract path and the pure-Icarus contract path

## Shells, Shards, Contracts, and Tests

### Shell 1: Public-Safe Skill Definition

- Objective: Define a reusable bootstrap skill that initializes a privacy-safe starter project with a canonical scaffold.
- Dependencies: project brief, scaffold reference, privacy scrub reference
- Interactions: `SKILL.md`, `agents/openai.yaml`, `README.md`
- Status: completed
- Measurable contracts:
  - The skill exposes the public name `public-icarusshell-bootstrap`.
  - The skill description explicitly targets privacy-safe bootstrap work.
  - The interface metadata matches the skill purpose and naming.
  - The skill body links directly to the required reference files.
- Linked tests:
  - Confirm `SKILL.md` frontmatter matches the planned name and description.
  - Confirm `agents/openai.yaml` display name, short description, and default prompt match the skill.
  - Confirm the skill links to both reference files and the example brief.

#### Shard 1.1: Create `SKILL.md`

- Scope: Define the trigger language, workflow, output contract, and reference links.
- Dependencies: Shell 1
- Status: completed
- Contract: `SKILL.md` is concise, procedural, and sufficient to trigger the bootstrap workflow without leaking local context.
- Failure conditions: missing frontmatter, local-only identifiers, or missing links to required references
- Concrete tests: inspect frontmatter; inspect linked references; search for prohibited local identifiers
- Evidence: file added at repo root with repo-relative links only

#### Shard 1.2: Create `agents/openai.yaml`

- Scope: Add UI-facing metadata aligned to the skill.
- Dependencies: Shard 1.1
- Status: completed
- Contract: metadata is human-readable, consistent with `SKILL.md`, and uses the public-safe naming.
- Failure conditions: mismatched skill name, stale prompt, or missing metadata fields
- Concrete tests: compare interface fields against `SKILL.md`
- Evidence: metadata file added under `agents/`

#### Shard 1.3: Create `README.md`

- Scope: Explain the repo shape, contents, and privacy posture.
- Dependencies: Shards 1.1 and 1.2
- Status: completed
- Contract: README explains the starter without introducing extra governance or local-only context.
- Failure conditions: undocumented repo purpose, privacy posture omitted, or git initialization implied as complete
- Concrete tests: inspect README sections for purpose, contents, privacy, and next step
- Evidence: concise root README added

### Shell 2: Scaffold and Reference Materials

- Objective: Provide the canonical full scaffold reference, privacy scrub guidance, and a sanitized example brief.
- Dependencies: IcarusShell++ Core requirements, public-safe release constraints
- Interactions: `references/scaffold-shape.md`, `references/privacy-scrub-checklist.md`, `examples/project-brief.md`, `scaffold.MD`
- Status: completed
- Measurable contracts:
  - The scaffold reference includes the full Icarus core text, operational disciplines, and usage instructions.
  - The project scaffold matches the required section order.
  - The privacy checklist bans the required classes of local-only data.
  - The example brief is sanitized and uses placeholders instead of live local context.
- Linked tests:
  - Compare the full Icarus content in `references/scaffold-shape.md` and `TEMPLATE-scaffold.IcarusShell.MD`.
  - Inspect the scaffold section order.
  - Inspect the privacy checklist for banned identifiers and safe replacements.
  - Search example content for absolute paths and personal identifiers.

#### Shard 2.1: Create `references/scaffold-shape.md`

- Scope: Capture scaffold order, minimum fields, recording rules, and the full Icarus reference content.
- Dependencies: Shell 2
- Status: completed
- Contract: the reference is sufficient to initialize future scaffolds consistently as a full Icarus reference, not a summary.
- Failure conditions: missing operational disciplines, missing prompt usage instructions, mutated core content, or incomplete scaffold guidance
- Concrete tests: inspect required headings and compare the full Icarus content against `TEMPLATE-scaffold.IcarusShell.MD`
- Evidence: scaffold reference added under `references/`

#### Shard 2.2: Create `references/privacy-scrub-checklist.md`

- Scope: Define what must be removed, what safe replacements look like, and how to verify.
- Dependencies: Shell 2
- Status: completed
- Contract: checklist covers personal names, usernames, home paths, machine names, connector IDs, local repo paths, and copied local examples.
- Failure conditions: one or more required privacy categories missing
- Concrete tests: inspect checklist bullets and verification search patterns
- Evidence: privacy checklist added under `references/`

#### Shard 2.3: Create `examples/project-brief.md`

- Scope: Provide a neutral example brief that exercises the bootstrap workflow.
- Dependencies: Shard 2.2
- Status: completed
- Contract: example is useful for testing the skill and contains no local-only identifiers.
- Failure conditions: copied live data, absolute paths, or real operator identifiers
- Concrete tests: inspect placeholders; run privacy searches against `examples/`
- Evidence: sanitized example brief added under `examples/`

#### Shard 2.4: Create canonical `scaffold.MD`

- Scope: Make this file the only source of truth for the project.
- Dependencies: Shards 2.1, 2.2, and 2.3
- Status: completed
- Contract: `scaffold.MD` contains the literal Core and complete initial decomposition for the repo.
- Failure conditions: parallel tracker added, missing required sections, or contracts/tests omitted
- Concrete tests: inspect section order; inspect Shells and Shards; verify only one root `scaffold.MD`
- Evidence: root scaffold created with three initial Shells

### Shell 3: Raw Template Publication

- Objective: Expose direct-copy scaffold contract artifacts for users who do not want to install or use the skill.
- Dependencies: Shell 2 scaffold source material, public-safe publication constraints
- Interactions: `TEMPLATE-scaffold.DaedalusShell.MD`, `TEMPLATE-scaffold.IcarusShell.MD`, `README.md`, `SKILL.md`
- Status: completed
- Measurable contracts:
  - The repo root contains two clearly named raw template artifacts.
  - The full template preserves the Daedalus contract path and embedded legacy Icarus path.
  - The pure-Icarus template is clearly labeled and excludes the Daedalus addendum.
  - Both README and SKILL point users to the raw templates and the full Icarus reference clearly.
- Linked tests:
  - Confirm both template files exist at the repo root.
  - Inspect the full template for Daedalus sections and embedded legacy Icarus content.
  - Inspect the pure-Icarus template for Icarus-only content.
  - Confirm `README.md` and `SKILL.md` both link to the root template files.

#### Shard 3.1: Publish full Daedalus-plus-Icarus template

- Scope: Add a root-level raw template artifact derived from the full contract source.
- Dependencies: Shell 3
- Status: completed
- Contract: the template is publishable, copyable, and preserves the Daedalus-plus-Icarus contract path.
- Failure conditions: missing Daedalus sections, missing embedded legacy core, or reliance on local-only context
- Concrete tests: inspect the template headings and privacy-search the file
- Evidence: `TEMPLATE-scaffold.DaedalusShell.MD` added at repo root

#### Shard 3.2: Publish pure-Icarus template

- Scope: Add a root-level raw template artifact for the lighter Icarus-only path.
- Dependencies: Shard 3.1
- Status: completed
- Contract: the template contains only the legacy Icarus path and is clearly labeled for direct use.
- Failure conditions: Daedalus addendum content included or Icarus operational disciplines missing
- Concrete tests: inspect the template content and confirm Daedalus sections are absent
- Evidence: `TEMPLATE-scaffold.IcarusShell.MD` added at repo root

#### Shard 3.3: Promote raw templates in public entry points

- Scope: Make README and SKILL direct users to the raw templates first.
- Dependencies: Shards 3.1 and 3.2
- Status: completed
- Contract: non-skill users can discover the raw templates immediately from the repo root documentation.
- Failure conditions: raw templates are undocumented or only discoverable through references
- Concrete tests: inspect `README.md` and `SKILL.md` for root template links near the top
- Evidence: raw template sections added to README and SKILL

### Shell 4: Repo-Ready Packaging

- Objective: Make the project ready for later git initialization without adding unnecessary extras.
- Dependencies: Shells 1, 2, and 3
- Interactions: repo root layout, `.gitignore`
- Status: completed
- Measurable contracts:
  - The repo root contains the expected starter files and directories.
  - `.gitignore` covers standard OS and editor clutter only.
  - No license file, git metadata, or executable bootstrap script is added.
- Linked tests:
  - List the repo root and confirm the expected files.
  - Inspect `.gitignore` for limited ignore rules.
  - Confirm no `.git/`, `LICENSE`, or `scripts/` path exists.

#### Shard 4.1: Create minimal root layout

- Scope: Create the root, `agents/`, `references/`, and `examples/`.
- Dependencies: Shell 4
- Status: completed
- Contract: the repo uses a standalone skill layout rather than a monorepo subtree.
- Failure conditions: missing required directories or extra unplanned structure
- Concrete tests: list directory tree to depth 2
- Evidence: minimal folder skeleton created

#### Shard 4.2: Create `.gitignore`

- Scope: Ignore common OS and editor clutter without hiding substantive project files.
- Dependencies: Shard 4.1
- Status: completed
- Contract: ignore list is minimal and does not include project content patterns.
- Failure conditions: broad ignore rules that could hide documentation or skill files
- Concrete tests: inspect `.gitignore` entries
- Evidence: root `.gitignore` added with OS and editor clutter rules only

#### Shard 4.3: Remove stray OS clutter from repo root

- Scope: Remove accidental OS-generated files that do not belong in the published project.
- Dependencies: Shard 4.2
- Status: completed
- Contract: no stray `.DS_Store` or equivalent OS clutter remains in the repo root.
- Failure conditions: accidental OS files remain in the publishable tree
- Concrete tests: list root files and confirm no `.DS_Store` exists
- Evidence: stray repo-root `.DS_Store` removed

## Ambiguities and Open Questions

- No blocking ambiguity remains for v1.
- License selection is intentionally deferred until a human chooses one.
- Scripted bootstrap automation is intentionally deferred until a later requirement calls for executable setup.
- The full raw template intentionally preserves contract semantics while omitting the local source file's worked examples.

## Decisions and Rationales

- The repo root is also the skill root to keep the project portable and easy to publish.
- The first release is documentation-first to reduce accidental local-environment leakage.
- The canonical project scaffold follows the `scaffold-icarusshellpp` workflow so the repo is publishable as an IcarusShell++ starter rather than only as a generic skill folder.
- Root-level raw template files are first-class public artifacts so non-skill users can copy a scaffold contract directly.
- Both a full Daedalus-plus-Icarus path and a pure-Icarus path are published to avoid forcing one workflow on all consumers.
- Reference material is split into `references/` so the main skill stays concise.
- Only one canonical `scaffold.MD` is used to avoid parallel source-of-truth drift.
- No git initialization or license selection is performed because both are deliberate release-time choices.

## Lessons Learned and Process Improvements

- A public-safe starter benefits from explicit privacy verification guidance rather than relying on author memory.
- A scaffold reference and an example brief are enough to make the first version usable without adding scripts too early.
- Keeping metadata, references, raw templates, and the scaffold aligned reduces drift when the skill evolves later.

## MCP / Tool Usage Log

- `find`: confirmed the target project did not exist before implementation and checked for more specific governance files in the ancestor area.
- `rg --files`: established the local pattern that reusable skills commonly expose `SKILL.md` and may include `agents/openai.yaml`, `references/`, and `examples/`.
- `sed`: reviewed the `scaffold-icarusshellpp` skill and its scaffold-shape reference, then matched this project's canonical scaffold and metadata structure to that workflow.
- `sed` and `rg`: reviewed the root scaffold source to identify the full Daedalus contract path and the embedded legacy Icarus path for publication-safe template artifacts.

## Execution Log

- Planned a standalone, public-safe skill repository with one canonical `scaffold.MD`.
- Created the minimal directory structure: `agents/`, `references/`, and `examples/`.
- Added the root skill definition, interface metadata, scaffold reference, privacy checklist, sanitized example brief, README, `.gitignore`, and canonical `scaffold.MD`.
- Added two root-level raw template artifacts for direct-copy use: one full Daedalus-plus-Icarus template and one pure-Icarus template.
- Updated README and SKILL so non-skill users see the raw templates first.
- Removed stray OS clutter from the repo root.
- Reserved git initialization, license selection, and any executable bootstrap tooling for later human-directed work.
