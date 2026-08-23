# Issue tracker

Backend: **GitHub Issues**

This repository treats an issue as the durable work contract.

## Flow

For non-trivial changes:

1. Align on the problem and project vocabulary.
2. Publish one spec issue when the work spans multiple sessions.
3. Split the spec into tracer-bullet implementation tickets.
4. Declare blocking edges.
5. Implement one frontier ticket at a time.
6. Review against the ticket, output contract, and acceptance cases.
7. Close the ticket only when its completion criteria are observable.

For a bounded single-session change, skip the spec and implement directly.

## Ticket shape

Prefer a vertical, independently verifiable behavior change over a horizontal layer change.

Each implementation ticket should state:

- problem / behavior;
- acceptance criteria;
- blocked by;
- stable seam being changed or tested;
- out of scope;
- verification evidence.

## Checklist-specific seam

The main stable seam is the output contract described in `skills/checklist-engineer/references/OUTPUT-CONTRACT.md`.

Do not reopen settled domain definitions inside implementation tickets. If a durable domain decision changes, write an ADR.
