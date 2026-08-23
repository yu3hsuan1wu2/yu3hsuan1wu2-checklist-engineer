# Artifact Fitness Gate

Use this reference before creating or substantially redesigning a checklist from source material, a workflow, or an existing procedural artifact.

Classify by **primary function in the work system**, not by surface format.

Do **not** classify using length, number of bullets, numbering, tables, or checkboxes.

A single source may contain more than one artifact function. When it does, classify by section or role instead of forcing one label onto the whole document.

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

### Task Plan

A **task plan** sequences or tracks work that must be performed for a bounded task, project, case, or day.

It answers:

> **What work needs to happen next?**

Typical task-plan content includes researching, drafting, contacting, deciding, writing, publishing, following up, and recording work.

A task action does not become a checklist item merely because it is written with a checkbox.

A useful diagnostic:

> If removing the document mainly makes it harder to know what work remains, who should do it, or what comes next, the artifact is functioning as a task plan.

### SOP + Checklist

Use both when the system needs a complete standard process **and** contains one or more high-leverage pause points where known critical omissions still occur.

The SOP owns the whole route. The checklist protects the critical gates inside that route.

Do not duplicate the SOP into the checklist.

### Task Plan + Checklist

Use both when a bounded body of work needs an execution route **and** contains one or more high-leverage transitions where critical omissions, mismatches, privacy errors, false completion, or failed handoffs are plausible.

The task plan owns the work to perform. The checklist protects the reliability gates inside that work.

Do not move ordinary production actions into the checklist unless they independently pass the killer-item filter at a real pause point.

### Decision Support

Use decision support when the main problem is choosing among context-sensitive alternatives rather than remembering known minimum actions.

Examples include decision trees, criteria, escalation rules, or structured judgment aids.

An unresolved decision must remain visibly unresolved. Checkbox syntax must not create false certainty.

### Research-Design

Use research/decision work when the correct preventive action, standard, or best practice is still unresolved.

Do not fabricate a checklist standard to hide unresolved knowledge.

## Supporting functions that are not automatically artifact types

### State distinctions

Statements such as `created ≠ published ≠ completed` define workflow state semantics. Preserve them when they prevent false completion claims, but do not automatically turn them into checklist items.

### Completion criteria

Completion criteria define what must be true for a task, day, or deliverable to count as complete.

They may become an operational checklist only when they are actually invoked at a concrete pause point — for example, `before daily close` or `before closing the ticket` — and each confirmation earns checklist attention.

Do not create a new checklist merely because completion criteria are formatted as checkboxes.

## Artifact Fitness questions

Run these in order.

### 1. Primary Function Test

If this artifact disappeared, what capability would the user lose?

- Standard method / full reusable procedure → `SOP`
- Reliability against critical omission → `CHECKLIST`
- Bounded execution route / what work remains → `TASK PLAN`
- Full standard procedure plus reliability gates → `SOP+CHECKLIST`
- Bounded execution route plus reliability gates → `TASK PLAN+CHECKLIST`
- Context-sensitive choice → `DECISION SUPPORT`
- Correct method not yet established → `RESEARCH-DESIGN`

If different sections answer different questions, return a mixed classification and decompose by function.

### 2. Knowledge Assumption Test

Does the intended checklist user already know how to perform the underlying work?

- Mostly yes → checklist may fit.
- No → do not use a checklist as the primary teaching artifact.

A `READ-DO` checklist may guide an unusual or order-sensitive sequence, but the underlying steps must still be established and domain-valid. Do not invent them.

### 3. Completeness Test

Would the artifact fail if important procedural detail were intentionally omitted?

- Yes → likely SOP/procedure.
- No, because the omitted detail remains part of professional competence or another source of truth → checklist may fit.
- No, but the document is mainly tracking work still to be performed → likely task plan.

### 4. Pause Point Test

Can the checklist be tied to a specific operational trigger before the target failure becomes expensive or irreversible?

If no meaningful pause point exists, reconsider whether a checklist is the right artifact.

Do not treat the start of every task as a pause point merely to preserve checkbox formatting.

### 5. Item Selection Test

Checklist items must earn attention.

For each candidate ask:

1. Does omission have meaningful consequence?
2. Could this intended user realistically omit or miscommunicate it?
3. Is this the right pause point to catch it?
4. Can it be confirmed observably?

If the line is simply work that still needs to be done — draft, contact, publish, research, enter data — keep it in the task plan unless there is separate evidence that it functions as a killer check.

If the artifact must include every step to remain usable, it is probably functioning as an SOP rather than a checklist.

### 6. Mixed Artifact Test

If a source contains actions, confirmations, decisions, status definitions, and completion criteria together:

1. separate production actions into the task plan;
2. extract high-risk confirmations into checklist pause points;
3. keep unresolved choices as decisions;
4. keep state semantics explicit;
5. treat completion criteria as checklist material only when used at an actual close gate.

## Classification output

Return one or more of:

- `CHECKLIST FIT`
- `SOP FIT`
- `TASK PLAN FIT`
- `SOP + CHECKLIST FIT`
- `TASK PLAN + CHECKLIST FIT`
- `DECISION SUPPORT FIT`
- `RESEARCH-DESIGN FIRST`
- `MIXED ARTIFACT` when section-level decomposition is required

Then state briefly:

1. **Primary function** — what problem each artifact layer must solve.
2. **Knowledge assumption** — what the intended user already knows.
3. **Reason for classification** — functional evidence, not appearance.
4. **Next artifact** — what should be created, separated, or revised.

## Important edge case: identical text, different function

The same four-line sequence can be an SOP fragment or a checklist.

If a novice depends on those four lines to learn the complete shutdown process, they function as procedure/SOP content.

If trained operators already know the shutdown and invoke those four established steps at a specific emergency trigger to avoid a dangerous omission, they can function as a `READ-DO` checklist.

Likewise, a checked box can represent work to do, a decision to make, a state to verify, or a killer check. Classification follows **how the artifact is used**, not what it looks like.
