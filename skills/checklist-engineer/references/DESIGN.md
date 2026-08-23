# Design branch

Use this branch to create a new operational checklist or redesign one from a workflow.

## 0. Run Artifact Fitness first

Read `ARTIFACT-FITNESS.md` when the input is source text, a workflow, a procedure, or an artifact whose function is not already settled.

Do not assume the requested output should be a checklist merely because the source contains steps, bullets, or checkboxes.

Proceed with this branch only for `CHECKLIST FIT`, the checklist portion of `SOP + CHECKLIST FIT`, or the checklist portion of `TASK PLAN + CHECKLIST FIT`.

If the result is `SOP FIT`, `DECISION SUPPORT FIT`, or `RESEARCH-DESIGN FIRST`, state that classification and do not force the material into a checklist.

## 1. Define the reliability target

State:

- desired outcome;
- recurring/plausible avoidable failure;
- who performs the work;
- consequence if the failure occurs.

Do not begin by listing the whole workflow.

## 2. Confirm whether a checklist fits the reliability problem

A checklist is a strong fit when:

- the necessary preventive action or information is already known;
- execution still varies or fails;
- omission/distraction/handoff is plausible;
- a brief intervention can occur before the failure becomes expensive.

Use another artifact when the real need is:

- training → tutorial/playbook;
- exhaustive standard procedure → SOP/manual;
- unresolved knowledge → research/decision work;
- continuous monitoring → dashboard/automation;
- nuanced judgment with no stable minimum checks → decision support, not a forced checklist.

## 3. Place pause points

Find the smallest number of moments where a brief stop gives high leverage.

For each pause point state:

- trigger;
- owner/facilitator;
- what cannot proceed until the check is complete.

Do not create a pause point merely because a phase exists.

## 4. Choose the mode

Choose separately per pause point if necessary.

Use `READ-DO` when order is important, the sequence is unusual or easy to confuse, or immediate guided execution is safer.

Use `DO-CONFIRM` when users are already trained, workflow fluency matters, and the list should verify rather than drive expert work.

## 5. Generate candidate items

Candidate sources:

- known incident/near-miss patterns;
- frequently omitted basics;
- irreversible or high-cost transitions;
- identity/resource/state mismatches;
- timing-sensitive actions;
- critical handoffs.

At this stage, over-generate. Do not publish yet.

## 6. Apply the killer-item filter

For each candidate ask:

1. If skipped, can the consequence matter?
2. Can this target user realistically skip/misremember/miscommunicate it?
3. Is this the right pause point to catch it?
4. Can it be stated as an observable confirmation?

Delete items that fail the filter.

If an action is critical but practitioners virtually always perform it, keep it outside the checklist unless local evidence shows otherwise.

## 7. Add communication checks

Read `COMMUNICATION.md` when no one person owns all relevant information, the situation has meaningful uncertainty, handoffs repeatedly fail, unexpected conditions matter, or team members need a shared mental model before proceeding.

## 8. Compress

For every remaining line ask:

- Does this change behavior?
- Can two words replace ten?
- Is rationale leaking into the operational surface?
- Is the wording ambiguous?
- Is the item really a manual step?

A pause point that users routinely shortcut is too long, badly timed, or both.

## 9. Produce the artifact

Use the output contract.

Separate:
- operational checklist;
- design rationale;
- exclusions/professional judgment;
- field-test plan.

Never hide rationale inside checklist wording.
