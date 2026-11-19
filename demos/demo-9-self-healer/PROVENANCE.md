# demo-9-self-healer — provenance

- **generated:** 2026-11-17 by the project's own self-healer generator (not published in this repository); the pack is regenerated from the run, never hand-staged.
- **what ran:** the healer chain on committed truth — a real Playwright failure with a stale locator (captured 2026-10-31) plus the real captured DOM. The failure bridge maps the failure to a site and emits a diff; the healer proposes a guarded locator fix; real GNU `patch` applies it (dry-run first, then applied) to a temp copy; a post-patch verifier reports STABLE.
- **what was replayed:** the mutation and the patch apply to a temporary copy of the login page object. The live source file is never written, and the pack records that the working tree stayed clean.
- **audit:** the proposal carries a tamper-evident audit chain; a deliberately altered record is refused.
- **visual evidence:** four chromium renders of the chain under `media/evidence/`, with sha256 in `media/INDEX.md`.
- **privacy:** committed fixtures and generated transcripts only; no credentials or PII.
- **scope:** the failure and the DOM are real. The fix is a controlled replay applied only to a temp copy, and nothing was auto-merged. The proposal is reviewable by design.
- **determinism:** the audit record carries a wall-clock timestamp, so the rendered seals are redacted for a byte-identical rebuild.
