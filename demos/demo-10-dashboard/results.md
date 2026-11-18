# demo-10-dashboard results

- summary: GREEN - 4 leg(s), 0 failed
- OK: real streak page
- OK: deterministic rebuild
- OK: stamp opt-in differs
- OK: secret redacted
- the page: `report/index.html` is the committed deliverable built
  from three REAL JUnit inputs; `media/evidence/dashboard.png` is its
  chromium render from the SAME build (see media/INDEX.md)
- honest absence: working-memory and heal-audit sections say "No data
  yet" because no such input was passed - the page shows the shape of
  what exists and marks what does not, without fabricating counts
- the one failing case is named verbatim from the real fail-capture;
  the dashboard does NOT smooth it into a green average
- what is NOT shown: a live streak, a server, a chart of invented
  numbers, or a redacted secret. The redaction/stamp controls ran in
  temp only and are reported as verdicts, not staged as artifacts
- the bounded run log: .run-log.txt

## honest framing

A dashboard is only as honest as its inputs and its absences. This one
shows three real lanes, names the failing case, and leaves two sections
visibly empty rather than inventing data. No retries: a failed leg is
committed RED.
