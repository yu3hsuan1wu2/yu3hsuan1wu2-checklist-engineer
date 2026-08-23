# ADR 0004 — Recognize task plans as distinct from operational checklists

Status: Accepted

## Context

T003 and T004 real-world administrative pilots both contained ordered work actions alongside reliability checks.

These artifacts were not SOPs: they did not teach a reusable standard procedure. They were also not pure operational checklists: several lines were the work itself — research, drafting, contacting, publishing, or recording — rather than confirmations placed at a reliability pause point.

Forcing these sources into `SOP` or `CHECKLIST` loses a useful distinction and encourages checklist bloat.

## Decision

Artifact Fitness recognizes two additional outcomes:

- `TASK PLAN FIT` — the primary need is to sequence or track work to be performed in a bounded task, project, or day.
- `TASK PLAN + CHECKLIST FIT` — the task plan owns the route while one or more operational checklists protect high-risk transitions inside it.

A task plan answers:

> **What work needs to happen next?**

An operational checklist answers:

> **At this pause point, what must not be missed before proceeding?**

Do not classify by checkbox syntax. A single source may contain task actions, checklist gates, decision points, state definitions, and completion criteria.

When a source is mixed, classify by section or function rather than forcing one label onto the entire document.

## Evidence

- `tests/results/T003-T1-12-pilot.md`
- `tests/results/T004-2026-08-21-daily-todo-pilot.md`
- Acceptance Case 11

## Consequences

- Production actions such as drafting, contacting, publishing, or data entry stay in the task plan unless they independently qualify as killer checks at a pause point.
- Reliability checks are extracted into explicit pause points instead of being mixed with ordinary to-do actions.
- Unresolved decisions remain decisions; checkbox completion must not create false certainty.
- Completion criteria are not automatically a new artifact type. They may become an end-of-task or end-of-day checklist only when used at an explicit pause point for reliability.
- P-011 is promoted from `CANDIDATE / HYPOTHESIS` to `ACTIVE / FIELD-DERIVED` after two real-world pilots plus regression coverage.
