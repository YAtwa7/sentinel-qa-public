# demo-8-roster-audit results

- summary: GREEN - 8 leg(s), 0 failed
  - OK: roster gate
- OK: roster selftest
- OK: judge invariants
- OK: judge selftest
- OK: orchestrator selftest
- OK: reproducible plan
- OK: fail-closed aggregate
- OK: memstore exclusion
- the headline: the roster is well-formed, both judges are cross-wired
  and memory-excluded, the plan is reproducible (prompts only), the
  committed failing sample aggregates to FAIL with exit 1, and no judge
  record leaked into the working-memory store
- expected red lines: the judge selftest's "FAIL broken-auditor" and
  the aggregate's "verdict: FAIL" are the controls working, not a
  broken pack (a gate that cannot fail proves nothing)
- what is NOT shown: a live specialist/judge run. The orchestrator
  explicitly does not spawn agents; that remains the agent harness/human
  layer. Nothing here claims a dispatch that did not happen
- media: four rendered transcripts of the REAL tool output
  (media/evidence/, sha-swept via media/INDEX.md)
- the bounded, redacted run log: .run-log.txt

## honest framing

An audit trail is a claim about tool behavior, with the red controls
kept visible next to the green ones. A rerun is regeneration, never a
retry-to-green: a leg that turns red is committed red.
