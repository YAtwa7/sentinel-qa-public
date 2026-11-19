# demo-9-self-healer results

- summary: GREEN - 6 leg(s), 0 failed
- OK: failure bridge proposal
- OK: heal audit sealed
- OK: audit tamper refused
- OK: patch dry-run
- OK: patch applied
- OK: post-patch GREEN
- the chain: a stale locator in a REAL captured failure is mapped
  through the healer's own extractor, guarded by the engine/policy
  rules, emitted as a reviewable diff, applied with REAL GNU patch to
  a temp copy, then verified STABLE - with a sealed audit whose
  tampered copy is refused
- expected red: the tampered-audit refusal (rc != 0) is a control
  proving the chain can fail, not a pack failure
- what is NOT shown: a live mutation of the repo, an LLM-written fix,
  or an auto-merge. The flagship is deterministic (difflib scoring,
  no LLM), and the patch is applied to a temp replay only
- media: four rendered transcripts of the real tool output
  (media/evidence/, sha-swept via media/INDEX.md)
- the bounded, redacted run log: .run-log.txt

## honest framing

Green means the replay healed the captured stale locator in a temp
copy and the post-patch verifier went STABLE. It does not mean a live
suite ran green or that the repo was changed - the live file was never
touched. A failed leg is committed RED; no retries.
