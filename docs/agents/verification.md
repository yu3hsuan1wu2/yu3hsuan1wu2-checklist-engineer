# Verification boundary

T001 uses two independent checks:

1. **Behavior evaluation** — run the six cases in `tests/acceptance.md` against the current skill instructions and record behavior traces in `tests/results/`.
2. **Installation smoke** — use `.github/workflows/skill-smoke.yml` to install the repository skill with the official `skills` CLI for Codex and verify the installed files.

Do not close T001 until both are complete.

A behavior pass does not prove installability. An installation pass does not prove the skill behaves correctly.
