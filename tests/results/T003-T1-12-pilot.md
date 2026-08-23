# T003 — Real-world pilot: T1-12 administrative checklist

Date: 2026-08-23
Pilot input: user-provided `T1-12` administrative work checklist
Stable seams:
- `skills/checklist-engineer/references/ARTIFACT-FITNESS.md`
- `skills/checklist-engineer/references/AUDIT.md`
- `docs/principles/PRINCIPLES.md`

## Source constraints

The pilot source states:

1. Confirm actual Outdoor Activities Team report items from the 8/17 department meeting.
2. Confirm the correct 8/17 adjournment time.
3. Select the 8/24 administrative meeting report content.
4. Draft two formal texts.
5. User confirms the content.
6. Write to the shared document and verify the saved result.

The source also explicitly states that the 8/24 meeting has not yet occurred. Therefore only pre-meeting report content can be prepared now; post-meeting decisions must not be treated as evidence yet.

This pilot does not retrieve or invent the missing 8/17 facts.

## Artifact Fitness

### Classification

**Nearest current classification: `CHECKLIST FIT`, with task-plan leakage and a taxonomy gap.**

The artifact is not functioning as an SOP: it does not teach a standard reusable procedure, methods, branches, or complete operating instructions. The intended user already knows how to perform the underlying work.

It does have a reliability function: without the list, the operator could draft from unverified facts, include future meeting outcomes prematurely, publish before user approval, or fail to verify persistence in the shared document.

However, items 4 and part of 6 are production actions rather than reliability checks. The artifact also sequences a one-off task from information gathering through publication. That behavior is closer to an **execution plan / task plan** than to either an SOP or a pure operational checklist.

The current taxonomy has no explicit `TASK PLAN` artifact type, so this pilot should not be used to silently redefine SOP or Checklist.

### Primary function

Coordinate completion of a one-off administrative task while preventing premature or unverified publication.

### Knowledge assumption

The operator already knows how to verify meeting information, draft formal text, obtain user approval, and update the shared document. The artifact does not teach those methods.

### Reliability target

Prevent these avoidable failures:

- drafting from unverified 8/17 report facts;
- using an unverified 8/17 adjournment time;
- recording 8/24 post-meeting decisions before the meeting occurs;
- publishing text before user approval;
- closing the task without confirming the shared document contains the approved content.

## Audit

**Verdict: `REVISION NEEDED`**

The main problem is not length. The six-line list mixes three different things:

1. information-gathering / decision work;
2. production work;
3. reliability gates.

That makes the list useful as a task plan, but less precise as an operational checklist.

### Item decisions

| # | Original function | Decision | Reason |
|---|---|---|---|
| 1 | Confirm 8/17 actual report items | `REWRITE` | Strong reliability check, but should be an observable verified state rather than an activity instruction. |
| 2 | Confirm correct 8/17 adjournment time | `REWRITE` | Same: important source verification before drafting. |
| 3 | Select 8/24 report content | `REWRITE` | Mixes decision work with a critical temporal boundary. Preserve the boundary: pre-meeting content only; no future decisions. |
| 4 | Draft two formal texts | `MOVE` | This is production work, not a killer check. Keep it in the task/execution plan. |
| 5 | User confirms content | `REWRITE` | This is a real communication/proceed gate; make the closure condition explicit. |
| 6 | Write to shared document and verify saved result | `REWRITE` | Mixed action + verification. Move the write action to task plan; keep saved-content verification as the checklist check. |

## Revised structure

### A. Task / execution plan

1. Verify the required 8/17 source facts.
2. Decide the 8/24 pre-meeting report scope.
3. Draft two formal texts.
4. Obtain user confirmation.
5. Write the approved text to the shared document.
6. Verify the saved result.

This plan owns the route. It is not presented as the operational checklist.

### B. Operational checklist

#### Pause point 1 — Before drafting formal text

**Mode:** `DO-CONFIRM`

- [ ] 8/17 actual report items are verified against an authoritative source.
- [ ] 8/17 adjournment time is verified against an authoritative source.
- [ ] 8/24 scope is explicitly pre-meeting only; no post-meeting decision is written as fact.

**Proceed condition:** Drafting may begin only when factual gaps are either verified or clearly marked unresolved.

#### Pause point 2 — Before writing to the shared document

**Mode:** `DO-CONFIRM`

- [ ] Both formal texts have been shown to the user.
- [ ] User approval is explicit, or requested revisions have been resolved.

**Communication check**

- **WHEN:** after draft, before publication;
- **WHO:** assistant and user;
- **WHAT:** both formal texts plus any unresolved factual uncertainty;
- **CLOSURE:** explicit approval or completed revision request.

#### Pause point 3 — Before closing T1-12

**Mode:** `DO-CONFIRM`

- [ ] The shared document contains the approved text.
- [ ] The saved result has been re-checked rather than assumed from the write action alone.

## Field-test question

**Does separating task-plan actions from reliability gates make the work easier to execute while reducing premature drafting/publication and false completion?**

Observe:

- whether the operator still needs the six-step execution route;
- whether the three pause points feel natural or excessive;
- whether verification wording prevents unsupported facts from entering the draft;
- whether approval and save verification are actually performed rather than clicked through;
- whether the split reduces or increases cognitive load.

## Principle-evolution finding

This pilot reveals a plausible artifact-category gap:

> A one-off **task plan / execution plan** can sequence work and ownership without being an SOP, while only some transitions deserve operational checklist gates.

This is captured as a **candidate**, not an active principle. One pilot is insufficient evidence to change the runtime Artifact Fitness taxonomy.

Recommended challenge before promotion:

- test at least two additional real-world one-off task lists;
- write an acceptance case where a task plan is incorrectly forced into SOP or Checklist;
- determine whether `TASK PLAN` should become a first-class Artifact Fitness category or remain a non-runtime explanatory concept.

## Pilot decision

- Existing principles P-001 through P-010 remain intact.
- No runtime `SKILL.md` change is justified by this single case.
- Candidate: distinguish **task/execution plans** from SOPs and operational checklists.
