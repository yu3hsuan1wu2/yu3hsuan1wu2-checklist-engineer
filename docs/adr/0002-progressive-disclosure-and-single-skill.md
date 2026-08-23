# ADR 0002 — One installable skill with progressive disclosure

Status: Accepted

## Context

Designing, auditing, and field-testing a checklist share the same domain rules. Splitting them into several independent skills would duplicate those rules or create fragile dependencies.

Matt Pocock's public agent-writing guidance emphasizes low context load, context pointers, progressive disclosure, completion criteria, and pruning duplication.

## Decision

Ship one installable skill: `checklist-engineer`.

Keep invariant rules in `SKILL.md`. Put branch-specific detail in sibling files under `references/`:

- design;
- audit;
- communication checks;
- field test;
- output contract;
- sources.

Repo-level `AGENTS.md` remains a pointer layer, while `CONTEXT.md` owns the ubiquitous domain language.

## Consequences

- The normal context surface stays small.
- A selected branch loads only the detail it needs.
- Shared checklist rules have one source of truth.
- The skill remains installable as one coherent package.
