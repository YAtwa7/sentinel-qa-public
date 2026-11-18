# demo-3-api-security PROVENANCE

- generated: 2026-11-16 by `demos/gen-demo3.py run` (committed script; the pack is
  regenerated, never hand-staged)
- suite: the repo's OWN committed security lane (two-identity authorization
  matrix, BFLA, mass assignment, policy controls) -
  `cd api && .venv/bin/pytest tests/security -m security`
- target: the LOCAL authorized practice stack (crAPI, loopback-confined,
  127.0.0.1 only per api/README.md; the suite's fail-closed gate re-proves
  the loopback contract by marker on every run). Practice accounts are
  printed on the target's own login screen; the matrix's probe identities
  are runtime-registered practice accounts
- command: committed pytest pin, one run, no retries (the repo's no-retry
  rule applies doubly)
- privacy-safety: outputs are SANITIZED of token/email shapes before any
  write (agreement 6) - the pack carries row outcomes and the clean
  transcript only, never credentials or internal roadmap docs
- motion-story: no (a terminal demo has no motion surface; the visual
  evidence is rendered transcripts of the run's real output - demos/README
  rule 6, screenshots yes, recordings only where a motion story matters)
- qa framing: a GREEN run means the target still behaves the way the wire
  records pin it - INCLUDING the confirmed findings (order-status BOLA,
  role-user-reachable admin routes) that the matrix rows document. That is
  a security finding about the practice target, reported as such - never
  "the API is secure" (test-strategy-phase-2.md, section 8.5). A RED run is
  committed as red: either the target drifted from the wire records or the
  lane is broken, and both are findings
