# demo-2-api-contract results

- summary: GREEN: the gate did its job - refuses a breaking diff (exit 1 expected) -> exit 1; passes the untouched spec (exit 0 expected) -> exit 0; a known trap: bare oasdiff exits 0 while printing an error -> exit 0; a known trap: the guarded command exits 1 -> exit 1
- the breaking mutation the gate refused: GET /identity/api/v2/user/dashboard: response property `available_credit` removed from the 200 schema's required list (required -> optional)
- media: rendered transcripts of the three verdicts under media/evidence/
  (see media/INDEX.md; listed with its sha256 in media/INDEX.md)
- the LAST 4000 CHARS of the (redacted) run log: .run-log.txt

## honest framing

This demo is the CONTRACT story: a breaking change to the declared API
contract is BLOCKED by the committed gate, and the tool's own trap
(bare `oasdiff breaking` exits 0 while printing the finding - that is the trap)
is replayed live so the audience sees why the guarded form matters.
A green run shows the gate working; it does NOT show the live target
agreeing with the spec (that is the deferred live contract gate, which
needs a self-hosted runner - documented in the roadmap).
