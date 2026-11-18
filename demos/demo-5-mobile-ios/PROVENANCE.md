# demo-5-mobile-ios PROVENANCE

- generated: 2026-11-17 by `demos/gen-demo5.py run` (committed script; the pack is
  regenerated, never hand-staged)
- suite: the repo's committed iOS Maestro flows (REQ-MOB-01..04) via
  `maestro test --udid D9CA6EE0-1951-4A6B-A396-8C72EBAE9F94 mobile/flows-ios/ --format=JUNIT
  --output <tmp>/junit.xml` (maestro 2.11 needs BOTH flags - a recorded incident)
  under DEVELOPER_DIR=/Applications/Xcode.app/Contents/Developer - one run, no retries
- toolchain: maestro 2.11.0 at the PIN; target: the
  sha-pinned Sauce Labs practice app (com.saucelabs.SwagLabsMobileApp) on the
  pinned simulator (iPhone); Xcode resolves through
  DEVELOPER_DIR (no sudo xcode-select - the a recorded incident no-sudo path)
- privacy-safety: the practice app is a public automation-practice target
  whose test credentials are printed on its own login screen (the flows
  already commit them); outputs clean of token/email shapes
- motion-story: yes (the flows ARE the motion story): media/video/
  demo5-ios-flows.mp4 recorded from the SAME run via `xcrun simctl io
  recordVideo` (recording captured); the guard demands this video for the pack
- qa framing: a green run shows the flows holding on iOS on the pinned
  toolchain; a red run is committed as red (flake-rule: no retries)
