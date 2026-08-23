# Manual acceptance cases

The stable seam is the output contract.

## Case 1 — Skilled routine, known omission

Prompt:
> A trained team performs the same procedure daily. A critical identity check is occasionally skipped under time pressure. Design a checklist.

Pass if:
- chooses a clear pre-commitment pause point;
- prefers DO-CONFIRM unless context justifies otherwise;
- includes the identity check as a killer item;
- does not rewrite the whole procedure;
- includes a field-test plan.

## Case 2 — Unfamiliar sequence where order matters

Prompt:
> A rarely used emergency shutdown has six known actions that must occur in sequence.

Pass if:
- considers READ-DO;
- makes sequence explicit;
- does not add generic background teaching to the operational surface;
- identifies what remains judgment.

## Case 3 — Split expertise / unexpected risk

Prompt:
> Three specialist teams independently prepare a high-stakes launch. Failures usually come from assumptions that one team knew information held by another.

Pass if:
- adds a communication check;
- states who talks to whom, about what, and when;
- does not attempt to enumerate every possible launch problem.

## Case 4 — Bloated 35-item “checklist”

Prompt:
> Audit this 35-item list. Most items explain the entire procedure and users routinely skip the second half.

Pass if:
- identifies SOP/manual leakage;
- cuts or relocates procedure detail;
- uses 5–9 and 60–90 seconds as heuristics rather than hard rules;
- preserves only items that earn scarce attention.

## Case 5 — Unknown best practice

Prompt:
> Nobody agrees on the correct response to this new failure mode. Make a checklist so people know what to do.

Pass if:
- says checklisting is not yet the primary solution;
- routes the unresolved question to research/decision work;
- does not fabricate a standard.

## Case 6 — Mechanical completion

Prompt:
> The form shows 99% completion, but incidents have not changed and teams say they click through it automatically.

Pass if:
- rejects completion rate as sufficient;
- investigates timing, wording, relevance, communication, and field behavior;
- proposes outcome measures tied to the target failure.
