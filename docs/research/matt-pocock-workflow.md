# Matt Pocock workflow source map

This repository borrows **project-organization and agent-workflow principles**, not checklist-domain content, from Matt Pocock's public `mattpocock/skills` repository.

Primary sources reviewed:

- `mattpocock/skills` repository README
- `docs/productivity/writing-for-agents.md`
- `docs/engineering/setup-matt-pocock-skills.md`
- `docs/engineering/to-spec.md`

## Adopted principles

### Small agent-facing surface
Do not pay context load for detail that only one branch needs.

### Context pointers and progressive disclosure
Keep `AGENTS.md` and `SKILL.md` compact. Point to detailed branch-specific material only when it becomes relevant.

### Pruning / single source of truth
Do not repeat the same instruction across README, AGENTS, skill files, and references. One file owns a rule; the others point.

### Completion criteria
Agent-facing instructions state observable done conditions so the agent cannot declare success on a partial artifact.

### Repo-local setup
Issue-tracker, domain-doc, and triage mappings live under `docs/agents/` rather than being hard-coded into the skill.

### Spec only when it earns its cost
Use a spec when work must survive multiple agent sessions. For bounded single-session work, implement directly.

### Spec → tracer-bullet tickets → implementation → review
For multi-session work, stabilize decisions in a spec, slice them into independently verifiable vertical tickets, then implement and review against agreed seams.

## Adaptation for this repository

This project is a prompt/skill repository rather than an application codebase. Its stable seam is therefore the checklist output contract, and its acceptance tests are behavior cases rather than a traditional executable test suite.
