# ADR 0001 — Use a failure-first checklist engineering model

Status: Accepted

## Context

Operational checklists easily decay into long SOPs or generic to-do lists. The source model for this project instead treats checklists as reliability interventions for complex work where knowledge exists but execution can still fail.

## Decision

All checklist design in this project follows:

**Failure pattern → Pause point → Mode → Killer items → Communication checks → Compression → Field test → Outcome**

A checklist must preserve a clearly named area of professional judgment.

Known critical actions become task checks. Unpredictable cross-role risk is handled with communication checks rather than an exhaustive contingency script.

## Consequences

- A complete process inventory is not automatically a checklist.
- An item can be important and still be intentionally omitted.
- Every checklist has a trigger.
- Every draft requires field testing before being treated as stable.
- Checklist success is judged by reliable execution and outcomes, not completion rate alone.
