# demo-4-mobile-android PROVENANCE

- generated: 2026-11-18 by `demos/gen-demo4.py run` (committed script; the pack is
  regenerated, never hand-staged)
- suite: the repo's committed Maestro flows (REQ-MOB-01..04: login
  success/failure, catalogue, menu drawer) via `maestro test mobile/flows/
  --format=JUNIT --output <tmp>/maestro-junit.xml` (maestro 2.11 needs
  BOTH flags: --output alone and the default NOOP format writes
  nothing, a recorded incident) - one run, no retries
- toolchain: maestro 2.11.0 at the PIN (a different
  version refuses, mobile/toolchain-pins.txt); target: the sha-pinned
  Sauce Labs practice app (com.swaglabsmobileapp) on the local AVD
  (`scripts/emulator.sh boot` per mobile/README.md section 3)
- privacy-safety: the practice app is a public automation-practice target
  whose test credentials are printed on its own login screen (the flows
  already commit them); outputs clean of token/email shapes; the
  pack carries row outcomes, the clean transcript, and the recording
- motion-story: yes (the flows ARE the motion story): media/video/
  demo4-android-flows.mp4 recorded from the SAME run via adb screenrecord
  (recording captured); the guard demands this video for the pack
- qa framing: a green run shows the four flows holding against the
  practice app on the pinned toolchain; a red run is committed as red
  (flake-rule: no retries exist here)
