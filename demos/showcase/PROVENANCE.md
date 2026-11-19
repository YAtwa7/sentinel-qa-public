# showcase — provenance

- **generated:** 2026-11-18 by the project's own showcase generator (not published in this repository).
- **sources:** ten committed pack artifacts only — two real mobile recordings and eight evidence cards. Every source is sha256-verified against the pack it comes from before assembly; `source-manifest.json` records the full hashes.
- **web lane:** the committed screenshot, because the web suite's short MP4s open on a white load frame.
- **motion:** the Android and iOS windows were chosen to show the app in use, not the launcher.
- **toolchain:** ffmpeg 8.0.1 for assembly; all text is rendered by Chromium from HTML that quotes the packs' own `results.md` summaries (the local ffmpeg has no `drawtext`).
- **output:** 57.1 s, 1280x720, H.264/yuv420p, no audio.
- **privacy:** no secret, credential or PII shape in the rendered text; only public pack artifacts and the public repository URL appear.
- **scope:** a marketing cut of the packs, not a pack itself. It adds no claim and no frame that is not already in a pack.
