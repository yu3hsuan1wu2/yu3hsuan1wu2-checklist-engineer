# Communication checks

Communication checks are used when reliability depends on **information crossing boundaries**, not merely on one person remembering a task.

The source pattern comes from construction “submittal schedules” and surgical team briefings: the checklist can specify that the right people must talk at the right time even when nobody can predict the exact problem in advance.

## Use a communication check when

- multiple specialists each see only part of the system;
- a handoff changes ownership;
- conditions vary case by case;
- the next step is hard to reverse;
- one person's concern must be visible to the whole team;
- “the unexpected” is a meaningful source of failure.

## A communication check must specify

1. **When** — the pause point.
2. **Who** — roles that must participate.
3. **What** — the minimum information that must be exchanged.
4. **Closure** — what shared confirmation permits work to continue.

Bad:

- “Communicate with the team.”
- “Discuss risks.”
- “Make sure everyone knows.”

Better:

- “Before release: owner states the top expected failure; each role states one concern or ‘none’.”
- “Before handoff: outgoing owner states current state, unresolved risk, and next irreversible action; incoming owner confirms receipt.”
- “Before commitment: operations, safety, and logistics each state blockers; proceed only after blockers have owners.”

## Do not over-script the conversation

A communication check creates the **conditions for expert coordination**. It should not prewrite every possible answer.

If the conversation can be fully specified as a fixed known action, it may be a task check instead.

## Design test

A communication check earns its place when removing it would make it materially easier for critical information to remain isolated in one person's head.
