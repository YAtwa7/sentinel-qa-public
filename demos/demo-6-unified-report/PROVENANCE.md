# demo-6-unified-report — provenance

- **generated:** 2026-11-17 by the project's own report builder (not published in this repository); the pack is regenerated from the run, never hand-staged.
- **what ran:** the unified report builder over the JUnit XML produced by the capture runs in the same pass — four lanes (API, Android, iOS, web) merged into one HTML report.
- **result:** 102 rows merged, 0 failures, 0 errors, 0 skipped.
- **what the report shows honestly:** lanes that did not report appear as visible notes, never as invented zeros. A green merged summary means the rows it received passed; it does not mean every lane ran, and the page states which lanes reported.
- **visual evidence:** the committed report page and its chromium render under `media/`, with sha256 in `media/INDEX.md`.
- **privacy:** lane names and per-row outcomes only; the inputs are the project's own redacted runs.
- **scope:** a merge of four specific lane outputs from one capture pass.
