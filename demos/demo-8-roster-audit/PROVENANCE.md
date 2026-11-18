# demo-8-roster-audit PROVENANCE

- generated: 2026-11-17 by `demos/gen-demo8.py run` (committed script; the pack is
  regenerated, never hand-staged)
- suite: the repo's committed decision tooling in ONE pass:
  `scripts/check-roster.sh` (+ --selftest), `scripts/check-judges.sh`
  (+ --selftest), `scripts/orchestrate.py --selftest` + `plan
  evals/orchestration-samples/sample-item-security.json` + `aggregate
  evals/orchestration-samples/sample-verdicts-fail.json`, and
  `evals/memstore.py check-exclusion`
- privacy-safety: only committed roster/judge/orchestrator text and
  rendered gate output appear; no secret, credential, environment
  value or live agent transcript; outputs clean of token/email
  shapes before any write
- motion-story: no (an audit transcript has no motion surface; rule 6
  evidence is the chromium renders under media/evidence/)
- honest scope: NO specialist or judge was dispatched. `plan` emits
  spawn prompts only; the aggregate reads a COMMITTED failing sample
  (exit 1 / verdict FAIL is the expected red control). The FAIL line in
  the judge selftest output is also expected - it proves the gate can
  fail. This pack audits tooling, not a pretend agent run
