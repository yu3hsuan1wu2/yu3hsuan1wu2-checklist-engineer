# Artifact Fitness Gate

Use this reference before creating or substantially redesigning a checklist from source material, a workflow, or an existing procedural artifact.

Classify by **primary function in the work system**, not by surface format.

Do **not** classify using length, number of bullets, numbering, tables, or checkboxes.

## Operational definitions

### SOP

A **Standard Operating Procedure (SOP)** is a procedural document whose primary function is to define how standard work should be performed consistently and reproducibly.

It answers:

> **How should this work be done?**

An SOP may include scope, roles, prerequisites, complete workflow, methods, branches, exceptions, records, and completion conditions.

A useful diagnostic:

> If removing the document means the intended user no longer knows the standard process well enough to perform it, the artifact is functioning as an SOP or training/procedure document.

Completeness is usually a virtue for an SOP.

### Checklist

An **operational checklist** is a compact reliability tool invoked at a defined pause point to prevent known, avoidable execution failures by confirming a small set of critical and realistically missable actions, states, or communications while preserving professional judgment.

It answers:

> **At this point, what must not be missed before we proceed?**

A useful diagnostic:

> If removing the document leaves trained users knowing how to do the work but makes critical omissions, mismatches, or coordination failures more likely, the artifact is functioning as a checklist.

Selectivity is a virtue for a checklist. Important actions may be intentionally absent when the target users reliably perform them without prompting.

### SOP + Checklist

Use both when the system needs a complete standard process **and** contains one or more high-leverage pause points where known critical omissions still occur.

The SOP owns the whole route. The checklist protects the critical gates inside that route.

Do not duplicate the SOP into the checklist.

### Decision Support

Use decision support when the main problem is choosing among context-sensitive alternatives rather than remembering known minimum actions.

Examples include decision trees, criteria, escalation rules, or structured judgment aids.

### Research-Design

Use research/decision work when the correct preventive action, standard, or best practice is still unresolved.

Do not fabricate a checklist standard to hide unresolved knowledge.

## Artifact Fitness questions

Run these in order.

### 1. Primary Function Test

If this artifact disappeared, what capability would the user lose?

- Standard method / full procedure → `SOP`
- Reliability against critical omission → `CHECKLIST`
- Both → `SOP+CHECKLIST`
- Context-sensitive choice → `DECISION SUPPORT`
- Correct method not yet established → `RESEARCH-DESIGN`

### 2. Knowledge Assumption Test

Does the intended checklist user already know how to perform the underlying work?

- Mostly yes → checklist may fit.
- No → do not use a checklist as the primary teaching artifact.

A `READ-DO` checklist may guide an unusual or order-sensitive sequence, but the underlying steps must still be established and domain-valid. Do not invent them.

### 3. Completeness Test

Would the artifact fail if important procedural detail were intentionally omitted?

- Yes → likely SOP/procedure.
- No, because the omitted detail remains part of professional competence or another source of truth → checklist may fit.

### 4. Pause Point Test

Can the checklist be tied to a specific operational trigger before the target failure becomes expensive or irreversible?

If no meaningful pause point exists, reconsider whether a checklist is the right artifact.

### 5. Item Selection Test

Checklist items must earn attention.

For each candidate ask:

1. Does omission have meaningful consequence?
2. Could this intended user realistically omit or miscommunicate it?
3. Is this the right pause point to catch it?
4. Can it be confirmed observably?

If the artifact must include every step to remain usable, it is probably functioning as an SOP rather than a checklist.

## Classification output

Return one of:

- `CHECKLIST FIT`
- `SOP FIT`
- `SOP + CHECKLIST FIT`
- `DECISION SUPPORT FIT`
- `RESEARCH-DESIGN FIRST`

Then state briefly:

1. **Primary function** — what problem the artifact must solve.
2. **Knowledge assumption** — what the intended user already knows.
3. **Reason for classification** — functional evidence, not appearance.
4. **Next artifact** — what should be created or revised.

## Important edge case: identical text, different function

The same four-line sequence can be an SOP fragment or a checklist.

If a novice depends on those four lines to learn the complete shutdown process, they function as procedure/SOP content.

If trained operators already know the shutdown and invoke those four established steps at a specific emergency trigger to avoid a dangerous omission, they can function as a `READ-DO` checklist.

Classification follows **how the artifact is used**, not what it looks like.
