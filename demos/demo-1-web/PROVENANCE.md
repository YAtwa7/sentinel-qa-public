# demo-1-web — provenance

- **generated:** 2026-11-16 by the project's own web-suite generator (not published in this repository); the pack is regenerated from the run, never hand-staged.
- **what ran:** the real end-to-end web suite — authentication, catalogue, cart, checkout, accessibility (axe against a committed findings baseline) and visual regression — with retries set to 0 in the real test configuration.
- **target:** https://www.saucedemo.com, the authorized public automation-practice store. Its test accounts are printed on its own login screen.
- **run:** one Chromium run. Every test produced a screenshot; the four story suites also produced video clips.
- **visual evidence:** 25 screenshots (one per test) and 11 clips under `media/`, each listed with its size and sha256 in `media/INDEX.md`.
- **privacy:** suite results and the store's own public surfaces only. No credentials, tokens or third-party data; the accounts used are the store's published practice accounts.
- **scope:** the run proves the suite's assertions held on that date against that target. It is not a claim about every browser or every future release of the store.
