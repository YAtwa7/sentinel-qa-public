# demo-6-unified-report results

- summary: unified report over 4 lane(s) - merged: 102 row(s), 0 failure(s), 0 error(s), 0 skipped
- merge exit code: 0 (the REAL contract, verified: 0 = the merge ran
  and wrote the page over what it received - a missing lane is a stderr
  note, not fatal; 1 = zero sources anywhere OR failures in the merged
  rows; 2 = broken pipeline. "Exit 1" never means "a lane was missing")
- lanes present: api, mobile-maestro-android, mobile-maestro-ios, web
- pack artifacts: report/index.html (the committed page) +
  report/junit-merged.xml; media/evidence/report.png is the chromium
  render of the SAME page (see media/INDEX.md)
- the LAST 4000 CHARS of the (clean) run log: .run-log.txt

## honest framing

This demo is the REPORTING story: one page over every lane the repo
actually ran, with absent lanes visible as notes rather than empty
columns. The "unified" claim is exactly as wide as the lanes listed
above - no more.
