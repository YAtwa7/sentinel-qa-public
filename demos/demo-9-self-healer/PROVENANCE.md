# demo-9-self-healer PROVENANCE

- generated: 2026-11-17 by `demos/gen-demo9.py run` (committed script; the pack is
  regenerated, never hand-staged)
- suite: the repo's real self-healer chain from committed truth - the
  real failure `harness/fixtures/fail-capture/junit.xml` (2026-10-31,
  stale locator deliberately mutated) + the real captured DOM; then
  `harness/ingest.py bridge --format diff`, `harness/healer.py heal`
  with a sealed audit, real GNU `patch -p1` (dry-run then applied), and
  a post-patch heal verifier. The mutation, proposal and patch are a
  REPLAY on a TEMP COPY of `web/pages/LoginPage.ts` - the live repo file
  is never written (verified: no repo diff)
- privacy-safety: no credential/token/email shape is written; outputs
  clean; only committed fixtures + generated transcripts in the
  pack; the audit JSONL lives only in the temp replay root
- motion-story: no (a replay transcript has no motion surface; rule 6
  evidence is the four chromium renders under media/evidence/)
- honest scope: the source failure and DOM are REAL; the mutation and
  patch are a controlled replay, never a claim that the live repo was
  healed or that anything was auto-merged. The proposal is reviewable
  and applied here by a real patch tool to a temp copy only
- determinism: the heal audit event carries a wall-clock timestamp at
  SECOND granularity, so its seal HASH can change between runs in
  different seconds (two runs in the same second collide). The rendered
  seal is redacted to a placeholder for byte-identical regeneration.
  The REAL seal still drives the verify and tamper commands, and their
  exit codes are the evidence (redact_volatile is tested in the
  generator's selftest)
