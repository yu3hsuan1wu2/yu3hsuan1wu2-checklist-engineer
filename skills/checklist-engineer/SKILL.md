---
name: checklist-engineer
description: Classify source text, workflows, work plans, or mixed procedural artifacts with Artifact Fitness, then design, audit, or field-test operational checklists when checklisting fits. Use when a user asks what kind of artifact a checkbox or procedural document really is, wants a checklist created or reviewed, or wants a draft tested in realistic use. Preserve expert judgment and do not turn checklists into SOPs or task plans.
---

# Checklist Engineer

Design for **reliable execution**, not completeness.

A checklist is a small intervention inside a workflow. It protects critical known actions and required communication without trying to encode all expertise.

## Select the branch

- Source text, workflow, procedure, or uncertain artifact type → read `references/ARTIFACT-FITNESS.md` first.
- New checklist or redesign from a workflow/failure pattern → read `references/DESIGN.md`.
- Audit/review of an existing checklist → read `references/AUDIT.md`; use `ARTIFACT-FITNESS.md` when SOP leakage or artifact misclassification is plausible.
- Field-test, pilot, revision, or validation planning → read `references/FIELD-TEST.md`.
- If communication checks may be needed → also read `references/COMMUNICATION.md`.
- Before finalizing any checklist branch → read `references/OUTPUT-CONTRACT.md`.

Do not load branch files that are irrelevant to the current request.

## Non-negotiable gates

### Artifact-fitness gate
Do not assume every procedural input should become a checklist. Classify by its function in the work system, not by length, bullets, numbering, or checkboxes.

### Failure gate
Name the known, avoidable execution failure the checklist is meant to reduce. If the problem is mainly missing knowledge, undefined best practice, or a need to teach the whole procedure, say a checklist is not the primary solution.

### Pause-point gate
Name exactly when the checklist is invoked. Prefer a moment before the relevant error becomes hard to recover from.

### Mode gate
Choose one intentionally:

- `READ-DO` — read, act, advance.
- `DO-CONFIRM` — act from expertise, pause, confirm.

Do not mix them implicitly.

### Killer-item gate
Keep an item only when omission has meaningful consequence **and** the intended user could realistically omit it.

Important-but-reliably-remembered actions do not automatically belong.

### Communication gate
When the main risk is uncertainty across people, roles, or handoffs, require an information exchange instead of inventing a long contingency script.

### Judgment gate
State what remains professional judgment. The checklist must not pretend to contain the whole job.

### Usability gate
Use simple, exact, familiar wording. Keep each pause point short enough to be completed under real working conditions.

Treat 5–9 items and 60–90 seconds as heuristics, not universal laws.

### Evidence gate
A first draft is provisional. Include a real-world test and revision loop before calling it stable.

## Working style

Use the user's existing conversation, incident evidence, source material, or workflow before asking for more. Do not re-interview for facts already established.

Prefer deletion over explanation inside the checklist itself. Put rationale outside the operational surface.

Do not claim domain correctness that the evidence does not establish. Flag items requiring subject-matter validation.

## Completion

Do not finish a checklist branch until the work satisfies `references/OUTPUT-CONTRACT.md`.
