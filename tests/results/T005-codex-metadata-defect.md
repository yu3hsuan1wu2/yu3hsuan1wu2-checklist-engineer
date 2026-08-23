# T005 — Codex metadata closeout defect

## Scope

Second adversarial review of formal closeout found a third, independent packaging defect:

- the repository explicitly installs `checklist-engineer` for Codex;
- Matt Pocock's current dual-harness convention gives each skill an `agents/openai.yaml` beside `SKILL.md` for Codex interface metadata and invocation policy when applicable;
- `checklist-engineer` did not have that file, and the smoke workflow could not detect its absence.

This repair does not change checklist-engineering behavior, Artifact Fitness, principles, or the model-facing `SKILL.md` description.

## Repair

Added canonical:

`skills/checklist-engineer/agents/openai.yaml`

```yaml
interface:
  display_name: "Checklist Engineer"
  short_description: "Engineer reliable operational checklists"
```

No `policy.allow_implicit_invocation: false` is present because `checklist-engineer` is intentionally model-invoked.

## Smoke coverage

The Codex install smoke now requires:

- installed `agents/openai.yaml` exists;
- `interface.display_name` is present and expected;
- `interface.short_description` is present and expected;
- implicit invocation is not disabled;
- installed metadata equals canonical source via `cmp`.

The existing checks for `SKILL.md`, `ARTIFACT-FITNESS.md`, and other runtime references remain intact.

## Behavior impact

**No checklist-engineering runtime behavior change.**

Prior behavior evidence remains applicable because no instruction body or runtime reference was modified:

- Cases 1–11 behavior: 11 PASS / 0 FAIL;
- Case 12 static invocation pointer: PASS;
- Case 12 behavior once invoked: PASS;
- autonomous model-routing black-box: NOT TESTED.

## Closeout boundary

A successful PR-triggered smoke run is still required before T005 can close again. Formal closure may claim that the canonical Codex metadata is packaged and installed consistently; it must not claim deterministic autonomous model routing.
