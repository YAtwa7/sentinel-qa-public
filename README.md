# sentinel-qa

**Evidence-first test engineering: web, API, mobile, and agentic quality — with the receipts.**

[![showcase poster](demos/showcase/poster.png)](demos/showcase/showcase.mp4)

**[Watch the 57-second showcase →](demos/showcase/showcase.mp4)**

The video is a cut of the project's own committed test artifacts: real run recordings, rendered transcripts and report pages. No re-enactments, no invented numbers, no voiceover. Every source is sha-verified before assembly ([source manifest](demos/showcase/source-manifest.json)).

**The source code is not published in this repository.** What is public is the evidence: what the system produced, how each result was produced, and the artifacts behind it. The suites, harness and generators that made them stay private. That is a deliberate boundary, not an omission.

## What this demonstrates

| Area | What shipped | Proof |
| :--- | :--- | :--- |
| Web | Playwright suite — 25 tests, zero retries; accessibility and visual regression gates; anti-bot abort contract and a loopback challenge sandbox | [demo 1](demos/demo-1-web/results.md) |
| API | OpenAPI breaking-change gate that refuses a real breaking diff; two-identity authorization matrix; fuzz, OWASP, and rate-limit lanes | [demo 2](demos/demo-2-api-contract/results.md) · [demo 3](demos/demo-3-api-security/results.md) |
| Mobile | Four Maestro flows on Android (emulator) and iOS (simulator), each recorded during the same run that produced its results | [demo 4](demos/demo-4-mobile-android/results.md) · [demo 5](demos/demo-5-mobile-ios/results.md) |
| Agentic quality | Eval gate with honest live-provider refusal; roster/orchestrator audit; deterministic self-healer that applies a real patch; dashboard over real results with absence visible | [demo 7](demos/demo-7-live-evals/results.md) · [demo 8](demos/demo-8-roster-audit/results.md) · [demo 9](demos/demo-9-self-healer/results.md) · [demo 10](demos/demo-10-dashboard/results.md) |
| Reporting | One unified report over four lanes (102 rows), built from the same capture pass | [demo 6](demos/demo-6-unified-report/results.md) |

The [evidence index](docs/EVIDENCE.md) lists every pack; the [architecture note](docs/ARCHITECTURE.md) explains how the pieces fit together.

## How to read a pack

Each folder under [`demos/`](demos/) is self-contained:

| File | What it holds |
| :--- | :--- |
| `results.md` | Headline verdict, the numbers, and what the run does and does not prove |
| `PROVENANCE.md` | When it ran, against what, on which toolchain, and what was not exercised |
| `.run-log.txt` | The bounded, redacted tail of the actual run output |
| `media/INDEX.md` | Every screenshot and recording, with size and sha256 |
| `media/` | The artifacts themselves |

## How the work is held to a standard

- **Every claim has a pack.** Each pack was produced by the project's own tooling in one run; nothing is hand-staged. Media carries a two-way sha256 sweep, so a swapped or stale artifact fails.
- **A check must be able to fail.** Each gate ships with a control that proves it can go red, and the checks that guard the packs are themselves tested on synthetic scratch trees.
- **Red is published red.** No retry-to-green. A suite that needs a second attempt is a stability finding, not a pass.
- **Independent review.** Changes land through branch, pull request, independent review, merge, and a versioned release.
- **Privacy by construction.** Credentials live outside the repository; fixtures, logs and traces are treated as public surface. Token and email shapes are removed, and machine-local paths are scrubbed, before anything is written.
- **Authorized targets only.** Public practice stores and loopback services. A bot challenge aborts the run as "blocked by bot protection" — it is never solved, masked or retried away.

## Author

Built by Joey — [@YAtwa7](https://github.com/YAtwa7).

## License

[PolyForm Noncommercial 1.0.0](https://polyformproject.org/licenses/noncommercial/1.0.0) — free to study, fork, and use for non-commercial (including portfolio) purposes; written permission is required for commercial use. Using or forking it does not transfer ownership: copyright stays with the author. See [LICENSE](LICENSE).

*Packs built at version 2.33.2.*
