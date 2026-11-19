# demo-8-roster-audit — provenance

- **generated:** 2026-11-17 by the project's own roster-audit generator (not published in this repository); the pack is regenerated from the run, never hand-staged.
- **what ran:** the decision tooling in one pass — the roster gate and its self-test, the judge gate and its self-test, an orchestrator plan built from a committed sample item, an aggregate over a committed failing sample (exit 1 is the expected result), and a working-memory exclusion check.
- **what did not run:** no specialist or judge was dispatched. The plan emits prompts only; the aggregate reads a committed failing sample. The FAIL line in the judge self-test is expected — it is the proof that the gate can fail.
- **visual evidence:** chromium renders of the real output under `media/evidence/`, with sha256 in `media/INDEX.md`.
- **privacy:** committed roster, judge and orchestrator text plus rendered gate output only; no keys, environment values or live transcripts.
- **scope:** this pack audits the tooling, not a pretend agent run. The expected red is labelled as expected.
