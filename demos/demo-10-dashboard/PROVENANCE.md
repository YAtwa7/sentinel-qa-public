# demo-10-dashboard — provenance

- **generated:** 2026-11-17 by the project's own dashboard generator (not published in this repository); the pack is regenerated from the run, never hand-staged.
- **what ran:** the dashboard over three committed JUnit truths — the 102-row unified report, the 13-row security lane, and a 4-row failure capture (one failing case named verbatim, three skipped).
- **what is absent:** no working-memory or audit input was passed, so those sections show the tool's own "No data yet" notes instead of invented zeros.
- **safety:** the redaction control's secret-shaped string and its page exist only in a temporary directory and never enter the pack; token shapes are removed before writing.
- **determinism:** the committed page is byte-identical across rebuilds; an explicit timestamp option is the only intended way to change it.
- **visual evidence:** the committed page and its chromium render under `media/`, with sha256 in `media/INDEX.md`.
- **scope:** four specific committed inputs. The page states what it received and what it did not.
