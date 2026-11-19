# demo-5-mobile-ios — provenance

- **generated:** 2026-11-17 by the project's own iOS-lane generator (not published in this repository); the pack is regenerated from the run, never hand-staged.
- **what ran:** the same four Maestro flows — login success, login failure, catalogue, menu drawer — on Maestro 2.11 against the iOS build, with JUnit output. Maestro 2.11 needs both `--format=JUNIT` and `--output`; `--output` alone writes nothing.
- **target:** the sha256-pinned Sauce Labs practice app (`com.saucelabs.SwagLabsMobileApp`) on an iPhone simulator. Xcode is selected through `DEVELOPER_DIR`; no `sudo` and no `xcode-select` mutation is used.
- **result:** 4/4 flows passed in one run, no retries.
- **recording:** `media/video/demo5-ios-flows.mp4`, captured with `xcrun simctl io recordVideo` during the same run that produced the JUnit rows.
- **visual evidence:** the flow matrix, the redacted output tail and the recording, each with size and sha256 in `media/INDEX.md`.
- **privacy:** the practice app is a public automation target whose test accounts are printed on its own login screen; token/email shapes are removed before anything is written.
- **scope:** the same four paths on one simulator and one pinned app build. Platform behaviour is not generalised beyond that.
