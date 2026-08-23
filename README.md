# Checklist Engineer

An installable agent skill for deciding when a checklist is the right artifact, creating operational checklists from source material or workflows, auditing existing checklists, and improving them through field evidence.

The project operationalizes Atul Gawande's *The Checklist Manifesto* while using a repo workflow adapted from Matt Pocock's public engineering skills.

## What you can give it

### 1. Source text or a workflow

Checklist Engineer first asks what artifact the work actually needs:

- `SOP`
- `CHECKLIST`
- `SOP+CHECKLIST`
- `DECISION SUPPORT`
- `RESEARCH-DESIGN`

It does not turn every procedural text into a checklist.

### 2. An existing checklist

It can audit the artifact for failure target, pause point, READ-DO / DO-CONFIRM mode, killer items, communication checks, SOP leakage, professional judgment, usability, and field evidence.

### 3. Real use evidence

It can plan or interpret field tests, identify shortcutting or checkbox compliance, and revise the checklist around observed failure patterns and outcomes.

## Product loop

**Create → Audit → Improve**

Before that loop, an **Artifact Fitness Gate** asks whether the problem should be solved with a checklist at all.

## Core checklist model

**Failure pattern → Pause point → Mode → Killer items → Communication checks → Compression → Field test → Outcome**

A checklist is not a complete SOP. It is a deliberately small reliability intervention placed where a known, avoidable execution failure is most likely or most costly, while preserving professional judgment.

## Living principles

Checklist-writing principles are governed in `docs/principles/PRINCIPLES.md`.

New ideas do not go directly into `SKILL.md`. They move through:

**CAPTURE → CLASSIFY → CHALLENGE → TEST → PROMOTE / REJECT → IMPLEMENT → REGRESSION → VERSION**

This lets the project learn from new sources and field evidence without turning the skill into an ever-growing prompt.

## Install

```bash
npx skills add yu3hsuan1wu2/yu3hsuan1wu2-checklist-engineer --skill checklist-engineer
```

## Repository shape

- `AGENTS.md` — short pointers only.
- `CONTEXT.md` — canonical domain vocabulary.
- `docs/agents/` — repo-local issue tracker, triage, and domain pointers.
- `docs/adr/` — durable design decisions.
- `docs/principles/` — canonical checklist-engineering principle registry.
- `docs/research/` — source maps for Gawande and Matt Pocock.
- `docs/specs/` — multi-session build specs when needed.
- `skills/checklist-engineer/` — installable skill with progressive disclosure.
- `templates/` — checklist, field-test, and principle-candidate templates.
- `tests/` — behavior-level acceptance cases and evaluation results.

## Skill behavior

The skill can:

- classify whether source material calls for SOP, checklist, both, decision support, or research/design first;
- design a checklist from a real failure pattern or workflow;
- audit an existing checklist for bloat, ambiguity, bad pause points, or missing communication checks;
- plan real-world field tests and revision loops.

It must preserve these gates: artifact fitness, failure target, pause point, READ-DO/DO-CONFIRM mode, killer-item filtering, communication checks where needed, professional judgment, usability, field testing, and outcome measurement.

## Status

`v0.1.0` established the checklist-engineering baseline. T002 adds the Principle Evolution System and Artifact Fitness Gate for the next baseline.
