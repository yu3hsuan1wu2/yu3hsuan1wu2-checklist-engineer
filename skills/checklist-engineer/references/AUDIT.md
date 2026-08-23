# Audit branch

Audit an existing checklist against reliability, not aesthetic preference.

## Audit sequence

### 1. Purpose
Can you name the avoidable failure being reduced?

- If no: `BLOCK` — the list has no reliability target.
- If it is mainly a tutorial/SOP: `CHANGE` — move procedure detail elsewhere.

### 2. Pause point
Is the trigger explicit and operational?

Look for vague triggers such as “before needed,” “regularly,” or a phase name with no actual stop condition.

### 3. Mode
Can a user tell whether to READ-DO or DO-CONFIRM?

Flag implicit mixing.

### 4. Killer items
For each item ask:

- meaningful consequence if omitted?
- plausible omission by target user?
- observable confirmation?
- belongs at this pause point?

Mark:
- `KEEP`
- `CUT`
- `MOVE`
- `REWRITE`

### 5. Communication
If risk comes from uncertainty, handoff, or split expertise, check whether the list creates a real information exchange.

A generic “communicate” item does not pass.

### 6. Judgment
Does the checklist clearly leave room for professional judgment, or does it pretend to encode the whole job?

### 7. Usability
Check:

- simple and exact wording;
- familiar domain language;
- low clutter;
- no rationale inside operational lines;
- short enough for the real environment.

Use 5–9 items and 60–90 seconds only as diagnostic heuristics.

### 8. Field evidence
Has the list been observed in realistic use?

Look for duration, skipped/shortcut items, confusion, catches/near misses, workflow interference, communication changes, and outcome changes.

## Audit output

Return:

1. **Verdict** — `PASS`, `REVISION NEEDED`, or `NOT A CHECKLIST PROBLEM`.
2. **Highest-risk findings** — ordered by reliability impact.
3. **Item decisions** — KEEP/CUT/MOVE/REWRITE.
4. **Missing communication checks**, if any.
5. **Revised operational surface** — only if requested or needed.
6. **Field-test target** — what the next real-world test must learn.

Do not reward a checklist for being comprehensive.
