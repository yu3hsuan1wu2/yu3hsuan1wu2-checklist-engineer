# Checklist Engineer

An installable agent skill for designing, auditing, and field-testing operational checklists for complex work.

The project operationalizes Atul Gawande's *The Checklist Manifesto* while using a repo workflow adapted from Matt Pocock's public engineering skills.

## Core model

**Failure pattern → Pause point → Mode → Killer items → Communication checks → Compression → Field test → Outcome**

A checklist is not a complete SOP. It is a deliberately small reliability intervention placed where a known, avoidable execution failure is most likely or most costly, while preserving professional judgment.

## Install

```bash
npx skills add yu3hsuan1wu2/yu3hsuan1wu2-checklist-engineer --skill checklist-engineer
```

## Repository shape

- `AGENTS.md` — short pointers only.
- `CONTEXT.md` — canonical domain vocabulary.
- `docs/agents/` — repo-local issue tracker, triage, and domain pointers.
- `docs/adr/` — durable design decisions.
- `docs/research/` — source maps for Gawande and Matt Pocock.
- `docs/specs/` — multi-session build specs when needed.
- `skills/checklist-engineer/` — installable skill with progressive disclosure.
- `templates/` — checklist and field-test templates.
- `tests/` — behavior-level acceptance cases.

## Skill behavior

The skill can:

- design a checklist from a real failure pattern or workflow;
- audit an existing checklist for bloat, ambiguity, bad pause points, or missing communication checks;
- plan real-world field tests and revision loops.

It must preserve these gates: failure target, pause point, READ-DO/DO-CONFIRM mode, killer-item filtering, communication checks where needed, professional judgment, usability, field testing, and outcome measurement.

## v0.1.0 baseline

Bootstrap is complete when the repo contains the domain context, repo-local agent pointers, source maps, ADRs, installable skill, branch references, output contract, templates, and acceptance cases. This baseline is now present on `main`.
