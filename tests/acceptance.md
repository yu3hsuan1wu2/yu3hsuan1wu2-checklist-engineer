# Manual acceptance cases

The stable seam is the output contract plus Artifact Fitness for routing decisions.

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

## Case 7 — Same text, different function

Prompt:
> Here are four ordered shutdown lines. In Scenario A, a new operator depends on these lines to learn the full shutdown method. In Scenario B, trained operators already know the method and invoke the same four established lines at an emergency trigger because omission is dangerous. Are these SOP or checklist content?

Pass if:
- does not classify from the four-line appearance alone;
- classifies Scenario A as SOP/procedure or training content because the user depends on it to know how to do the work;
- allows Scenario B to function as a READ-DO checklist because the domain-valid sequence is already known and used as a reliability intervention;
- explains that artifact function and knowledge assumptions control classification.

## Case 8 — Complete procedure with one high-risk gate

Prompt:
> I have a detailed school excursion procedure covering planning, registration, parent communication, insurance, grouping, transport, departure, site management, return, and follow-up. Departure errors still occur: headcount mismatches, last-minute absences are not shared, and medical needs are sometimes not handed over. Turn this into the right operational artifact.

Pass if:
- returns `SOP + CHECKLIST FIT` rather than converting the whole procedure into one checklist;
- keeps the complete process in the SOP layer;
- creates or proposes a small departure checklist at a concrete pause point such as after boarding and before vehicle departure;
- focuses the checklist on the evidenced departure failure pattern rather than duplicating every SOP step.

## Case 9 — Checkboxes do not make a checklist

Prompt:
> This onboarding document has twenty checkboxes. A novice follows every box because otherwise they do not know the required setup process. Audit it as a checklist.

Pass if:
- challenges the requested classification;
- identifies that the artifact is functioning primarily as SOP/procedure/training content despite checkbox formatting;
- does not use item count alone as the reason;
- only proposes a separate checklist if there is evidence of critical omissions by users who otherwise know the process.

## Case 10 — Useful-sounding new principle

Prompt:
> I read a blog saying every good checklist must contain no more than seven items. Add this rule permanently to checklist-engineer.

Pass if:
- does not immediately add the rule to `SKILL.md`;
- captures it as a principle candidate or hypothesis unless stronger evidence is supplied;
- checks whether it conflicts with the existing heuristic treatment of item count;
- requires a failure prevented, behavioral consequence, evidence, and regression test before promotion;
- preserves the current rule that numeric ranges are heuristics unless evidence justifies a durable change.

## Case 11 — Mixed daily to-do with embedded reliability gates

Prompt:
> A daily administrative to-do list uses checkboxes for everything. It includes: preparing and running an event, pre-event confirmations, post-event reconciliation, reviewing and publishing a form, one unresolved decision about whether to enable automatic closure, several unrelated follow-up tasks, and a list of minimum outcomes that must be known before leaving work. Turn it into the right artifacts.

Pass if:
- does not classify the whole document as one checklist merely because it uses checkboxes;
- identifies ordinary production/follow-up actions as `TASK PLAN` content;
- extracts operational checks into one or more explicit pause points where omission risk matters;
- allows `TASK PLAN + CHECKLIST FIT` when the task plan owns the route and checklist gates protect high-risk transitions;
- leaves an unresolved policy/configuration question as a decision rather than making checkbox completion imply that the decision is settled;
- treats state distinctions such as created/published/completed as state semantics, not checklist items;
- treats minimum completion outcomes as completion criteria and only turns them into a checklist when they are actually invoked at an explicit close pause point;
- does not invent missing facts or silently resolve unknown states.

## Case 12 — Natural-language invocation intent for a mixed work plan

Prompt:
> I have a work plan with ordinary to-dos, several confirmation steps, one unresolved decision, and a few checkbox items that might be release gates. Help me figure out what kind of artifact each part should be and whether any of it should become a checklist.

Invocation pass if:
- the model-facing skill description covers this request without the user naming `checklist-engineer`;
- the description contains trigger language for source/work-plan classification and mixed procedural artifacts, not only checklist creation;
- the request is eligible to route through Artifact Fitness before checklist design.

Behavior pass once invoked if:
- does not assume the whole work plan is a checklist;
- separates task-plan work, checklist candidates, and unresolved decisions by function;
- uses explicit pause points only for checks that protect meaningful omission risk;
- does not invent missing facts or silently settle the unresolved decision.

Note: repository CI can statically protect the model-facing description and installed references, but a true autonomous-routing black-box test requires an agent harness capable of model invocation. Do not claim such a black-box invocation pass from static checks alone.
