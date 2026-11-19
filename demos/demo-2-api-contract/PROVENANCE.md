# demo-2-api-contract — provenance

- **generated:** 2026-11-16 by the project's own contract-gate generator (not published in this repository); the pack is regenerated from the run, never hand-staged.
- **what ran:** an OpenAPI breaking-change gate over a committed contract snapshot, using a pinned `oasdiff`.
- **the breaking candidate:** a deterministic transform (committed in the generator) removes `available_credit` from the 200-response schema's required list on `GET /identity/api/v2/user/dashboard`. Candidate sha256[:16]: `d5e71237273d9277`. The candidate lives in a temp directory; the committed snapshot is never modified.
- **verdicts:** a real breaking diff is refused (exit 1, as expected); the untouched spec passes (exit 0, as expected). Both verdicts are in the transcript.
- **the trap this exists for:** bare `oasdiff breaking` prints the breaking finding and still exits 0. The gate's guarded form is what turns that into a failing exit code, and the pack replays both so the difference is visible.
- **run:** offline; no target or network needed.
- **visual evidence:** rendered transcripts of the real command output under `media/evidence/`, with sha256 in `media/INDEX.md`.
- **privacy:** verdict text and rendered transcripts only; no credentials or tokens.
- **scope:** a specification-level gate. It blocks a breaking contract change; it does not exercise a live service.
