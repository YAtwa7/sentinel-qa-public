# demo-7-live-evals — provenance

- **generated:** 2026-11-17 by the project's own eval-gate generator (not published in this repository); the pack is regenerated from the run, never hand-staged.
- **what ran:** the eval gate's deterministic mode (rc 0) plus two refusals on the live path, both dispatch-only: no provider key (rc 2) and an unknown provider (rc 2).
- **what did not run:** no live model was adjudicated. A real live call belongs to a manual dispatch where a key can exist. This pack's green means the deterministic leg held **and** both refusals refused — never that a provider was reached.
- **visual evidence:** chromium-rendered transcripts of the real output under `media/evidence/`, with sha256 in `media/INDEX.md`.
- **privacy:** no key is read, printed or forwarded; the environment file is bypassed; token/email shapes are removed before anything is written.
- **scope:** the point of the pack is the refusal. A system that says "I cannot run this, and here is why" is more useful than one that invents a verdict.
