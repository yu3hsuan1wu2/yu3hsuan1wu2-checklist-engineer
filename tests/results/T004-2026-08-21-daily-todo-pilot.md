# T004 — 2026-08-21 daily to-do pilot

Source: user-provided real administrative work list titled `8/21 今日待辦`.

## Purpose

Challenge P-011 (`Separate task plans from operational checklists`) with a second real-world artifact and test whether one document can contain multiple artifact functions.

## Top-level classification

**Result: mixed artifact.**

The whole document should not be classified as one checklist merely because most lines use checkboxes.

It contains at least four functions:

1. task / execution planning;
2. operational checklist gates;
3. a decision point requiring judgment;
4. end-of-day completion / close criteria that can function as a checklist only when tied to a real closing pause point.

## Section A — On-site ID photo session

### Classification

`TASK PLAN + CHECKLIST`

The work includes production/coordination actions and two natural reliability gates.

### Pause point A1 — Before the first class is called

Checklist candidates:

- vendor present and equipment usable;
- venue confirmed as 3棟2樓藝游軒;
- final class set confirmed as `1134 / 1135 / 1136`;
- class gathering / shooting schedule verified;
- required photo appearance reminder delivered;
- official method for recording absence / non-participation established.

Why this is checklist-like: these are known conditions whose omission can disrupt or invalidate the session at a high-leverage transition.

### Task-plan actions during/after the session

- run the shooting session;
- obtain actual counts;
- follow up on missing participants;
- coordinate vendor follow-up.

These are work to perform, not automatically checklist checks.

### Pause point A2 — Before closing the session record

Checklist candidates:

- actual shot count confirmed with vendor;
- missing-shot total reconciled;
- missing cases categorized as absence / opted out / unresolved;
- personal names remain only in authorized administrative source; Project Control stores anonymized counts only;
- vendor intake method and delivery timeline confirmed, or explicitly recorded as `UNKNOWN`.

This second gate protects reconciliation, privacy, and unknown-state integrity.

## Section B — Self-upload form

### Classification

Mostly `CHECKLIST`, with one embedded `DECISION SUPPORT / JUDGMENT` item.

### Pause point — Immediately before publication

Checklist candidates:

- Human review completed;
- class / seat number / name / non-participation reason fields verified;
- upload restriction verified: image, one file, 10 MB;
- Google sign-in / account-recording notice verified;
- photo-spec reminder verified;
- displayed deadline verified as 8/28;
- distribution scope verified: only people who still need self-upload receive the form.

### Decision point

`Whether automatic submission closure should be enabled` is not merely a binary reliability check unless policy has already been decided. It requires a decision and should not be disguised as a completed checklist item.

### Proceed condition

Publish only after the pre-publication checks pass and the unresolved auto-close decision is either resolved or explicitly accepted as open.

### State invariant

`Form created ≠ form published ≠ collection completed` is not itself a checklist item. It is a state distinction that prevents false completion claims.

## Section C — Administrative records to restore

### Classification

`TASK PLAN`

The section mainly names work that must be performed:

- recover 8/20 meeting facts and decisions;
- contact two absent students;
- confirm paper return-slip distribution / return status;
- check seven Google Classroom history-record assignments.

These actions may contain local verification checks, but the section itself is an execution backlog, not an operational checklist.

## Today's minimum completion standard

### Classification

`COMPLETION CRITERIA` at document level; can become an `END-OF-DAY CHECKLIST` only when explicitly invoked at the pause point `before closing the workday`.

The listed outcomes are useful because they define what must be true for the day to be considered minimally complete. They do not automatically become checklist items merely because they are checkbox-shaped.

If used operationally at end of day, the reliable surface becomes:

### Pause point — Before daily close

- ID-photo session completion status known;
- anonymous counts for shot / missed / self-upload known;
- self-upload form review/publication state known;
- 8/20 meeting occurrence and main decisions known or explicitly unresolved;
- follow-up state for the two absent students known.

## Reliability findings

### Finding 1 — Checkbox syntax hides artifact boundaries

The source uses checkbox syntax for task actions, verifications, decisions, and completion criteria. Surface syntax therefore cannot identify artifact type.

### Finding 2 — Task-plan leakage is repeatable

As in T003, production actions and reliability checks coexist in one list. Moving every action into the checklist would dilute attention.

### Finding 3 — One document can contain multiple artifact functions

Artifact Fitness must be able to classify sections or lines when a source is mixed, rather than forcing one label on the whole document.

### Finding 4 — Unresolved decisions and unknown states need explicit treatment

`Decide whether to enable automatic closure` and `UNKNOWN` delivery information must remain visibly unresolved. A checkbox must not convert an unresolved decision or unknown fact into apparent completion.

## P-011 evaluation

This pilot independently supports P-011:

- T003: one-off administrative drafting workflow mixed execution actions and checklist gates.
- T004: daily administrative plan again mixes task actions and multiple operational checklist gates across a different work context.

P-011 is no longer supported by a single case. Promotion still requires a formal acceptance case and regression check before runtime taxonomy changes.

## Candidate follow-on

A possible future principle is that **mixed artifacts should be decomposed by function before checklist design**. This may be an extension of P-001/P-011 rather than a separate principle; do not promote a new principle from this pilot alone.
