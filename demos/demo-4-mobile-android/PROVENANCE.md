# demo-4-mobile-android — provenance

- **generated:** 2026-11-18 by the project's own Android-lane generator (not published in this repository); the pack is regenerated from the run, never hand-staged.
- **what ran:** four Maestro flows — login success, login failure, catalogue, menu drawer — on Maestro 2.11 with JUnit output. Maestro 2.11 needs both `--format=JUNIT` and `--output`; `--output` alone writes nothing.
- **target:** the sha256-pinned Sauce Labs practice app (`com.swaglabsmobileapp`) on a local Android emulator (API 34, headless).
- **result:** 4/4 flows passed in one run, no retries.
- **recording:** `media/video/demo4-android-flows.mp4`, captured with `adb screenrecord` during the same run that produced the JUnit rows — not a separate demo.
- **visual evidence:** the flow matrix, the redacted output tail and the recording, each with size and sha256 in `media/INDEX.md`.
- **privacy:** the practice app is a public automation target whose test accounts are printed on its own login screen; token/email shapes are removed before anything is written.
- **scope:** the flows are those four paths, on that emulator and that pinned app build.
