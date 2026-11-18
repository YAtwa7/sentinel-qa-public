# demo-6-unified-report PROVENANCE

- generated: 2026-11-17 by `demos/gen-demo6.py run` (committed script; the pack is
  regenerated, never hand-staged) from the repo's own
  `scripts/unified-report.sh --out <tmp>` (exit 0)
- suite: the repo's unified report over the lanes' junit XML written by
  the capture runs in this generation pass (lanes present: api, mobile-maestro-android, mobile-maestro-ios, web)
- privacy-safety: the report carries lane names and per-row outcomes only;
  the inputs are the repo's own clean runs; nothing secret-shaped
  (the demos guard scans pack CONTENT; the conventions gate scans FILENAMES)
- motion-story: no (a report page has no motion surface; the rule-6
  evidence is the chromium render of the committed page, media/evidence/)
- qa framing: the page shows what the merge received - present lanes as
  tables, absent lanes as visible notes, never invented zeros. A green
  merged summary means the merged rows it received passed; it does not
  mean every lane ran (that is stated above, honestly)
