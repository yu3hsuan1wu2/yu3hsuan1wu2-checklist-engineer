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
**Principle:** Determine what artifact the work needs before designing a checklist. Do not classify by length, bullets, numbering, or checkboxes. Mixed sources may need section-level decomposition.

**Evidence:** Gawande distinguishes quick checklist tools from comprehensive how-to guidance and emphasizes preserving professional judgment; T003/T004 further show that bounded task plans and embedded checklist gates are functionally distinct.

**Failure prevented:** Turning every procedural or checkbox-formatted text into a checklist; checklist/SOP/task-plan conflation.

**Behavioral consequence:** Before creating or substantially redesigning a checklist from source material, classify the need using `SOP`, `CHECKLIST`, `TASK PLAN`, combined variants, `DECISION SUPPORT`, `RESEARCH-DESIGN`, or `MIXED ARTIFACT` as defined in `skills/checklist-engineer/references/ARTIFACT-FITNESS.md`.

**Regression coverage:** Acceptance Cases 4, 5, 7, 8, 9, 11.

**Supersedes / conflicts:** Extended by P-011; no conflict.

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

**Regression coverage:** Cases 1, 2, 3, 11.

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

**Regression coverage:** Cases 1, 4, 11.

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

**Regression coverage:** Cases 2, 3, 5, 11.

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

**Regression coverage:** Cases 6, 11.

**Supersedes / conflicts:** None.

### P-011 — Separate task plans from operational checklists

**Status:** ACTIVE  
**Type:** FIELD-DERIVED  
**Principle:** A bounded task/execution plan may sequence work, ownership, drafting, publication, follow-up, and decisions without functioning as either an SOP or an operational checklist. Keep production actions in the task plan and reserve checklist gates for high-risk transitions where critical omissions must be caught.

**Evidence:** Two real-world administrative pilots independently exposed the same pattern: `tests/results/T003-T1-12-pilot.md` and `tests/results/T004-2026-08-21-daily-todo-pilot.md`. ADR 0004 records the durable classification decision.

**Failure prevented:** Forcing every to-do sequence into SOP or Checklist; diluting operational checklists with ordinary production steps; treating unresolved decisions or status semantics as completed checks.

**Behavioral consequence:** Artifact Fitness now recognizes `TASK PLAN FIT`, `TASK PLAN + CHECKLIST FIT`, and `MIXED ARTIFACT`. When a source is mixed, separate production actions, operational checks, decisions, state distinctions, and completion criteria by function before designing checklist surfaces.

**Regression coverage:** Acceptance Case 11 plus T003/T004 pilot evidence.

**Supersedes / conflicts:** Extends P-001. No conflict.

---

## Candidate principles

No current candidate is promoted automatically from T004's completion-criteria observation. Additional evidence is required before creating a new first-class artifact type for completion criteria.

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
