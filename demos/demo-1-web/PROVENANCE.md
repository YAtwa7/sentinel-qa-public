# demo-1-web PROVENANCE

- generated: 2026-11-16 by `demos/gen-demo1.py run` (committed script; the pack is
  regenerated, never hand-staged)
- suite: repo's real phase-1 web suite (auth/catalogue/cart/checkout/a11y/visual)
- target: https://www.saucedemo.com - the authorized public automation-practice
  store; its test accounts are printed on its own login screen
- command: `cd web && npx playwright test --project=chromium` with
  `DEMO_CAPTURE=1` (the repo's playwright.config.ts owns retries=0,
  artifacts, the junit reporter, and the demo-capture video/screenshot
  override - one flag on the REAL config, no demo-only fork of it)
- playwright/node: whichever the local install pins at generation time
- visual evidence (rule 6, show don't sell): 25 screenshot(s) (every test) + 11 video clip(s) (story suites; webm->mp4 where ffmpeg allowed) under media/. The committed
  selection rule lives in the generator (screenshots: every test; video:
  the 4 story suites); a marketing cut may crop/trim these
  pack artifacts but may not introduce a frame they do not come from
- motion-story: yes (the web suite IS the motion story - the recordings
  are the point; the demos guard demands the video for this pack)
- privacy-safety: this pack carries suite RESULTS and the store's own public
  surfaces only - no credentials, no internal roadmap docs, nothing
  secret-shaped (the demos guard scans pack CONTENT for that; the
  conventions gate scans tracked FILENAMES). The practice store's own
  login form may be filled in the media with its PUBLIC practice
  credentials - that is the target's own published surface
- qa framing: a green run shows the deterministic suite holding; a red run is
  NOT hidden - the pack reports it honestly (flake-rule: no retries exist here)
