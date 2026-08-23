# ADR 0003 — Govern artifact fitness and principle evolution explicitly

Status: Accepted

## Context

Checklist Engineer is intended to evolve as new source material, field evidence, failures, and acceptance-test results appear.

Without an explicit governance layer, two failure modes are likely:

1. every useful-sounding idea accumulates directly in `SKILL.md`, creating duplicated or contradictory instruction sediment;
2. procedural source material is routinely converted into a checklist even when the actual need is an SOP, decision aid, or unresolved research/design work.

## Decision

### Artifact fitness comes first

Before checklist creation or substantial redesign from source material, classify the required artifact by primary function:

- `SOP`
- `CHECKLIST`
- `SOP+CHECKLIST`
- `DECISION SUPPORT`
- `RESEARCH-DESIGN`

Classification is functional rather than visual. Length, bullets, numbering, tables, and checkboxes are not sufficient evidence.

Operationally:

- **SOP** defines how standard work should be performed consistently and reproducibly.
- **Checklist** protects trained execution at a defined pause point against critical, realistically missable omissions, mismatches, or communication failures.
- **SOP+CHECKLIST** uses a complete procedure as the process source of truth and small checklists at high-leverage gates.

### Principles have a lifecycle

`docs/principles/PRINCIPLES.md` is the canonical principle ledger.

A proposed principle moves through:

**CAPTURE → CLASSIFY → CHALLENGE → TEST → PROMOTE / REJECT → IMPLEMENT → REGRESSION → VERSION**

A principle must not become runtime guidance only because it sounds sensible.

Every principle records a stable ID, status, evidence type, failure prevented, behavioral consequence, regression coverage, and supersession/conflict information.

### Runtime instructions stay small

`SKILL.md` remains a routing and invariant layer. Detailed artifact classification and governance live behind pointers.

## Consequences

- Checklist Engineer may correctly refuse to produce a checklist.
- The same text may classify differently depending on how trained users rely on it.
- SOP completeness and checklist selectivity are treated as different design virtues.
- New knowledge can accumulate without automatically increasing always-loaded prompt size.
- Principle changes require evidence and behavioral tests, reducing regression and prompt sediment.
- Durable changes remain traceable even when an older principle is deprecated or superseded.
