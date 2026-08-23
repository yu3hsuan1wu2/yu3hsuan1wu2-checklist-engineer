# Domain Context

This is the shared vocabulary for Checklist Engineer.

## SOP
A procedural source of truth whose primary function is to define how standard work should be performed consistently and reproducibly.

An SOP may need scope, roles, prerequisites, complete workflow, branches, exceptions, records, and completion conditions. Completeness is usually a virtue for an SOP.

## Checklist
A compact reliability tool used at a defined point in work to prevent known, avoidable execution failures while preserving professional judgment.

A checklist assumes the underlying work or preventive actions are already established. It is **not** a comprehensive SOP, manual, tutorial, knowledge base, or substitute for expertise. Selectivity is a virtue for a checklist.

## Artifact fitness
The functional classification of what work artifact a problem needs before design begins.

Canonical classifications:
- `SOP`
- `CHECKLIST`
- `SOP+CHECKLIST`
- `DECISION SUPPORT`
- `RESEARCH-DESIGN`

Classify by the artifact's role in the work system, not by length, bullets, numbering, tables, or checkboxes.

## Failure pattern
A recurring or plausible way work fails even though the necessary knowledge or preventive action is already known.

## Pause point
The explicit moment when work stops briefly and the checklist is invoked. Prefer a point before the error becomes difficult or impossible to recover from.

## READ-DO
Read an item, perform it, then move to the next item. Use when sequence or immediate guided execution matters.

## DO-CONFIRM
Perform work from training and experience, then stop at the pause point and confirm the critical items were completed. Use when skilled practitioners should retain workflow and judgment.

## Killer item
A check worth occupying scarce checklist attention because:
1. omission has meaningful consequences; and
2. the target user could realistically omit it.

Importance alone is not enough.

## Task check
Confirms a known critical action, state, resource, identity, or condition.

## Communication check
Forces a necessary information exchange at a defined moment: who must talk to whom, about what, before work continues.

Use communication checks when uncertainty cannot be exhaustively scripted but coordinated expert judgment can reduce risk.

## Professional judgment
Everything the expert or team still decides using context, expertise, and current evidence. A good checklist protects judgment instead of trying to encode all of it.

## Field test
Use of a draft checklist in realistic work, followed by observation, revision, and retesting.

## Checkbox compliance
A failure mode where the list is completed mechanically but the intended verification, communication, discipline, or outcome does not occur.

## Principle Registry
The canonical ledger at `docs/principles/PRINCIPLES.md` that records which checklist-engineering principles are candidate, active, deprecated, or rejected and what evidence/tests justify their status.
