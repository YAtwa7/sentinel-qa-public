# demo-7-live-evals PROVENANCE

- generated: 2026-11-17 by `demos/gen-demo7.py run` (committed script; the pack is
  regenerated, never hand-staged)
- suite: the repo's committed eval gate (`evals/eval_gate.py`): the
  deterministic `--mode fixed` leg (rc 0) plus two DISPATCH-ONLY
  live refusals - keyless (rc 2) and unknown-provider (rc 2);
  the dispatch-only home is `.github/workflows/live-evals.yml`
  (dispatch-only + refusal control confirmed)
- privacy-safety: no key is read, printed or forwarded (all 6
  provider/key vars scrubbed; .env.local bypassed via a nonexistent
  SENTINEL_ENV_FILE); captured output clean of token/email shapes;
  only committed gate/dataset/workflow output appears in the pack
- motion-story: no (a gate transcript has no motion surface; rule 6's
  visual evidence is the chromium-rendered transcripts under media/evidence/)
- honest scope: NO live model was adjudicated here. A real live run
  belongs to a manual CI dispatch where a key can exist. This pack's
  green means the offline judge held AND both refusals refused - never
  that a live provider was reached
