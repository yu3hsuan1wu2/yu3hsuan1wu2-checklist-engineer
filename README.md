# Checklist Engineer

An installable agent skill for deciding what work artifact a problem needs, creating and auditing operational checklists, and improving them through field evidence.

The project operationalizes Atul Gawande's *The Checklist Manifesto* while using a repo workflow adapted from Matt Pocock's public engineering skills.

## What you can give it

### 1. Source text, workflow, or work plan

Checklist Engineer first classifies the artifact by function. Current Artifact Fitness outcomes include:

- `SOP`
- `CHECKLIST`
- `TASK PLAN`
- `SOP+CHECKLIST`
- `TASK PLAN+CHECKLIST`
- `DECISION SUPPORT`
- `RESEARCH-DESIGN`
- `MIXED ARTIFACT`

Checkboxes, bullets, or document length do not determine the classification.

### 2. An existing checklist

It can audit the artifact for reliability target, pause point, READ-DO / DO-CONFIRM mode, killer items, communication checks, procedural leakage, professional judgment, usability, and field evidence.

### 3. Real-use evidence

It can plan or interpret field tests, identify shortcutting or checkbox compliance, and revise the checklist around observed failure patterns and outcomes.

## Product loop

**Artifact Fitness → Create / Audit → Field Test → Improve**

## Core checklist model

**Failure pattern → Pause point → Mode → Killer items → Communication checks → Compression → Field test → Outcome**

A checklist is not a complete SOP or task plan. It is a deliberately small reliability intervention placed where a known, avoidable execution failure is most likely or most costly, while preserving professional judgment.

## Living principles

Checklist-engineering principles are governed in `docs/principles/PRINCIPLES.md`.

New ideas do not go directly into `SKILL.md`. They move through:

**CAPTURE → CLASSIFY → CHALLENGE → TEST → PROMOTE / REJECT → IMPLEMENT → REGRESSION → VERSION**

This lets the project learn from new sources and field evidence without turning the skill into an ever-growing prompt.

## Install

```bash
npx skills add yu3hsuan1wu2/yu3hsuan1wu2-checklist-engineer --skill checklist-engineer
```

## Repository shape

- `AGENTS.md` — short agent pointers.
- `CONTEXT.md` — canonical domain vocabulary.
- `docs/agents/` — repo-local tracker, triage, and domain pointers.
- `docs/adr/` — durable design decisions.
- `docs/principles/` — canonical principle registry.
- `docs/research/` — source maps and research notes.
- `skills/checklist-engineer/` — installable skill with progressive disclosure.
- `templates/` — checklist, field-test, and principle-candidate templates.
- `tests/` — behavior acceptance cases and pilot evidence.

## Status

The initial build is complete and the repository is in maintenance / evidence-driven evolution mode.

Future behavioral changes should enter through GitHub Issues and the Principle Evolution System. Installability is checked by `.github/workflows/skill-smoke.yml`; behavior is protected by the acceptance cases in `tests/acceptance.md`.
