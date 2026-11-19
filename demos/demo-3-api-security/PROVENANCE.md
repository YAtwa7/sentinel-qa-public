# demo-3-api-security — provenance

- **generated:** 2026-11-16 by the project's own security-lane generator (not published in this repository); the pack is regenerated from the run, never hand-staged.
- **what ran:** the security lane in one pytest run — a two-identity authorization matrix, broken function-level authorization, mass assignment and policy controls.
- **target:** a local, loopback-confined practice API stack (crAPI on `127.0.0.1` only). Practice accounts are printed by the target itself; the matrix's probe identities are registered at runtime.
- **result:** 13 rows, 0 failures, 0 errors, 0 skipped — including the confirmed findings (order-status BOLA among them). A green security lane means the target still behaves as the recorded evidence pins it, findings included.
- **run:** one run, no retries.
- **visual evidence:** the matrix rows and the redacted output tail, rendered under `media/evidence/`, with sha256 in `media/INDEX.md`.
- **privacy:** row outcomes and transcripts only; credentials and token/email shapes are removed before anything is written.
- **scope:** a snapshot against one local build of a practice stack. Not a claim about any production system.
