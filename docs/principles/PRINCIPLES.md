# Checklist Engineering Principle Registry

This is the canonical ledger for principles that may shape Checklist Engineer behavior.

`SKILL.md` is not the knowledge base. A principle belongs here first; only the small behavioral consequence needed at runtime belongs in the skill or a branch reference.

## Principle types

- `SOURCE-ANCHORED` — directly supported by a named source or research finding.
- `PROJECT-SYNTHESIS` — a project-level operationalization synthesized from one or more sources; do not attribute the framework itself to a source unless the source actually names it.
- `FIELD-DERIVED` — supported by repeated observation in realistic use.
- `HYPOTHESIS` — plausible but not yet supported enough to govern behavior.

## Status

- `CANDIDATE` — captured for evaluation; must not silently govern the skill.
- `ACTIVE` — admitted into the current behavioral model and protected by regression evidence.
- `DEPRECATED` — retained for traceability but no longer governs behavior.
- `REJECTED` — tested or reviewed and not admitted.

## Evolution loop

**CAPTURE → CLASSIFY → CHALLENGE → TEST → PROMOTE / REJECT → IMPLEMENT → REGRESSION → VERSION**

### Capture
Record the proposed principle and the evidence that triggered it. Do not edit `SKILL.md` first.

### Classify
Assign one principle type. Distinguish what the source says from what this project infers.

### Challenge
Ask:

1. What failure would this principle prevent?
2. What observable agent behavior should change?
3. Is it already represented by an existing principle?
4. Is the evidence general enough, or only a one-off case?
5. Would adding it create duplication, contradiction, or instruction sediment?

### Test
Create or identify an acceptance case that can fail if the principle is absent or misapplied.

### Promote / reject
Promote only when evidence, behavioral consequence, and regression coverage are explicit. A principle does not become `ACTIVE` merely because it sounds sensible.

### Implement
Change the smallest authoritative runtime document. Prefer a pointer or branch reference over adding always-loaded text.

### Regression
Re-run affected cases and existing protected behavior. A new principle must not silently break earlier gates.

### Version
Record durable model changes in an ADR when appropriate. Superseded principles remain traceable.

## Required fields for every principle

Each principle entry must include:

- **ID**
- **Principle**
- **Status**
- **Type**
- **Evidence**
- **Failure prevented**
- **Behavioral consequence**
- **Regression coverage**
- **Supersedes / conflicts**

---

## Active principles

### P-001 — Artifact fitness before checklist design

**Status:** ACTIVE  
**Type:** PROJECT-SYNTHESIS  
**Principle:** Determine what artifact the work needs before designing a checklist. Do not classify by length, bullets, numbering, or checkboxes.

**Evidence:** Gawande distinguishes quick checklist tools from comprehensive how-to guidance and emphasizes preserving professional judgment; the project operationalizes that distinction as an artifact-routing gate.

**Failure prevented:** Turning every procedural text into a checklist; checklist/SOP conflation.

**Behavioral consequence:** Before creating or substantially redesigning a checklist from source material, classify the need as `SOP`, `CHECKLIST`, `SOP+CHECKLIST`, `DECISION SUPPORT`, or `RESEARCH-DESIGN`. Read `skills/checklist-engineer/references/ARTIFACT-FITNESS.md`.

**Regression coverage:** Acceptance Cases 4, 5, 7, 8, 9.

**Supersedes / conflicts:** None.

### P-002 — Failure-first design

**Status:** ACTIVE  
**Type:** PROJECT-SYNTHESIS  
**Principle:** Start from a known or plausible avoidable execution failure, not from a complete workflow inventory.

**Evidence:** Gawande's examples repeatedly target recurring omissions and coordination failures despite existing knowledge.

**Failure prevented:** Checklist bloat; converting a workflow map into a checkbox inventory.

**Behavioral consequence:** Name the reliability target and avoidable failure before selecting checklist items.

**Regression coverage:** Cases 1, 4, 5, 6.

**Supersedes / conflicts:** None.

### P-003 — Explicit pause point

**Status:** ACTIVE  
**Type:** SOURCE-ANCHORED  
**Principle:** A checklist must have a clear operational trigger or pause point.

**Evidence:** *The Checklist Manifesto*, “The Checklist Factory.”

**Failure prevented:** Lists that exist but are not reliably invoked at the moment they can prevent an error.

**Behavioral consequence:** State exactly when the checklist starts and, when needed, what cannot proceed until it is complete.

**Regression coverage:** Cases 1, 2, 3.

**Supersedes / conflicts:** None.

### P-004 — Choose READ-DO or DO-CONFIRM intentionally

**Status:** ACTIVE  
**Type:** SOURCE-ANCHORED  
**Principle:** Match execution mode to the work rather than mixing guided action and expert confirmation implicitly.

**Evidence:** *The Checklist Manifesto*, “The Checklist Factory.”

**Failure prevented:** Ambiguous execution behavior and interruption of expert workflow.

**Behavioral consequence:** Use `READ-DO` when order/guidance matters; use `DO-CONFIRM` when trained users should work from expertise and confirm at a pause point.

**Regression coverage:** Cases 1, 2.

**Supersedes / conflicts:** None.

### P-005 — Killer items earn scarce attention

**Status:** ACTIVE  
**Type:** SOURCE-ANCHORED  
**Principle:** Importance alone is insufficient. A checklist item should normally have meaningful consequence if omitted and be realistically missable by the target user.

**Evidence:** *The Checklist Manifesto*, “The Checklist Factory,” including intentional omission of important actions professionals virtually never forget.

**Failure prevented:** Comprehensive but unusable lists; attention dilution.

**Behavioral consequence:** Keep, cut, move, or rewrite candidate items using consequence + plausible omission + right pause point + observable confirmation.

**Regression coverage:** Cases 1, 4.

**Supersedes / conflicts:** None.

### P-006 — Communication checks for distributed uncertainty

**Status:** ACTIVE  
**Type:** SOURCE-ANCHORED  
**Principle:** When failure comes from split expertise, assumptions, or handoffs, require a structured information exchange rather than scripting every contingency.

**Evidence:** *The Checklist Manifesto*, construction and surgical team examples.

**Failure prevented:** Critical information remaining isolated inside one role or team.

**Behavioral consequence:** Define `WHEN`, `WHO`, `WHAT`, and `CLOSURE` for communication checks.

**Regression coverage:** Case 3.

**Supersedes / conflicts:** None.

### P-007 — Preserve professional judgment

**Status:** ACTIVE  
**Type:** SOURCE-ANCHORED  
**Principle:** A checklist supports skilled work; it does not attempt to encode all expertise or eliminate adaptation.

**Evidence:** *The Checklist Manifesto* on balancing discipline, coordination, expertise, and freedom to handle unpredictability.

**Failure prevented:** Checklist-as-algorithm overreach; unsafe false completeness.

**Behavioral consequence:** State what remains professional judgment and what requires subject-matter validation.

**Regression coverage:** Cases 2, 3, 5.

**Supersedes / conflicts:** None.

### P-008 — Usability over formal completeness

**Status:** ACTIVE  
**Type:** SOURCE-ANCHORED  
**Principle:** Operational wording should be simple, exact, familiar, low-clutter, and fast enough for the real work environment.

**Evidence:** *The Checklist Manifesto*, “The Checklist Factory” and surgical field testing.

**Failure prevented:** Skipping, shortcutting, ambiguity, and checklist fatigue.

**Behavioral consequence:** Treat 5–9 items and 60–90 seconds as diagnostic heuristics, not universal laws; prefer deletion over explanation on the operational surface.

**Regression coverage:** Case 4.

**Supersedes / conflicts:** None.

### P-009 — Drafts require field evidence

**Status:** ACTIVE  
**Type:** SOURCE-ANCHORED  
**Principle:** A first checklist draft is a hypothesis and must be observed, revised, and retested in realistic work or the closest safe simulation.

**Evidence:** *The Checklist Manifesto*, checklist development and implementation examples.

**Failure prevented:** Treating desk-designed wording as validated behavior.

**Behavioral consequence:** Include a field-test learning question, observation plan, and revision criterion before calling a checklist stable.

**Regression coverage:** Case 1 and field-test branch tests.

**Supersedes / conflicts:** None.

### P-010 — Outcome over checkbox completion

**Status:** ACTIVE  
**Type:** SOURCE-ANCHORED  
**Principle:** Mechanical completion is not sufficient evidence that a checklist improves reliability.

**Evidence:** *The Checklist Manifesto* distinguishes disciplined teamwork/outcomes from box ticking and reports outcome-oriented evaluation.

**Failure prevented:** Checkbox compliance masquerading as effectiveness.

**Behavioral consequence:** Measure target failures, catches, defects, rework, coordination, or relevant outcomes; completion rate is secondary.

**Regression coverage:** Case 6.

**Supersedes / conflicts:** None.

---

## Candidate principles

### P-011 — Separate task plans from operational checklists

**Status:** CANDIDATE  
**Type:** HYPOTHESIS  
**Principle:** A one-off task or execution plan may sequence work, ownership, drafting, and publication without functioning as either an SOP or an operational checklist. Keep production actions in the task plan and reserve checklist gates for high-risk transitions where critical omissions must be caught.

**Evidence:** T003 real-world `T1-12` pilot. The six-step administrative list coordinated information gathering, drafting, approval, publication, and save verification. It did not teach a reusable standard procedure, yet several lines were production actions rather than reliability checks. See `tests/results/T003-T1-12-pilot.md`.

**Failure prevented:** Forcing every to-do sequence into SOP or Checklist; diluting operational checklists with ordinary production steps; misclassifying one-off execution plans as standard procedures.

**Behavioral consequence:** None yet. Do not change the runtime taxonomy from this single case. Challenge whether `TASK PLAN` or `TASK PLAN + CHECKLIST` should become a first-class Artifact Fitness category after additional real-world cases and an acceptance test.

**Regression coverage:** T003 pilot only; formal acceptance case not yet established.

**Supersedes / conflicts:** Potentially extends P-001 Artifact Fitness; does not currently supersede it.

---

## Candidate template

### P-XXX — Short name

**Status:** CANDIDATE  
**Type:** SOURCE-ANCHORED | PROJECT-SYNTHESIS | FIELD-DERIVED | HYPOTHESIS  
**Principle:**  
**Evidence:**  
**Failure prevented:**  
**Behavioral consequence:**  
**Regression coverage:**  
**Supersedes / conflicts:**  
