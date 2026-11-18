# demo-10-dashboard PROVENANCE

- generated: 2026-11-17 by `demos/gen-demo10.py run` (committed script; the pack is
  regenerated, never hand-staged) from the repo's own
  `harness/dashboard.py build --junit <three committed JUnit truths>`
- suite: the REAL streak from committed truth - the 102-row unified
  report, the 13-row pytest security lane, and the 4-row fail-capture
  (1 failing case named verbatim, 3 skipped). No memstore/audit input
  was passed: those sections render the tool's own "No data yet" notes,
  never invented zeros
- privacy-safety: no key read, no server/network, no live data; the
  redaction control's secret-shaped string and its page live ONLY in a
  temp dir and never enter the pack; outputs clean before writing
- motion-story: no (a static page has no motion surface; rule 6 evidence
  is the chromium render of the SAME committed report/index.html)
- determinism: the committed page is byte-identical across rebuilds;
  `--stamp` is the explicit opt-in (proven to differ in a temp build).
  Both controls, plus the [REDACTED] control, are tested in the
  generator's selftest and verified on every run
