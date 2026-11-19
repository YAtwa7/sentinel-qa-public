# demos — ten evidence packs

Each folder here is one capability, captured in a single run and published with its output, its provenance and its media.

| # | Pack | What it shows |
| :-- | :--- | :--- |
| 1 | [demo-1-web](demo-1-web/) | A deterministic, zero-retry web suite against an authorized practice store: auth, catalogue, cart, checkout, accessibility, visual regression |
| 2 | [demo-2-api-contract](demo-2-api-contract/) | An OpenAPI breaking-change gate that refuses a real breaking diff — and the exit-code trap it exists for |
| 3 | [demo-3-api-security](demo-3-api-security/) | A two-identity authorization matrix over a local practice API, confirmed findings included |
| 4 | [demo-4-mobile-android](demo-4-mobile-android/) | Four Maestro flows on an Android emulator, recorded during the same run |
| 5 | [demo-5-mobile-ios](demo-5-mobile-ios/) | The same four flows on an iOS simulator, recorded during the same run |
| 6 | [demo-6-unified-report](demo-6-unified-report/) | One JUnit-merged report over four lanes — 102 rows, absent lanes visible |
| 7 | [demo-7-live-evals](demo-7-live-evals/) | An eval gate that reports honestly and refuses a live path it cannot run |
| 8 | [demo-8-roster-audit](demo-8-roster-audit/) | A roster and orchestrator audit with fail-closed controls and an expected red |
| 9 | [demo-9-self-healer](demo-9-self-healer/) | A real stale-locator failure turned into a guarded proposal, applied by real `patch` to a temp copy, verified stable |
| 10 | [demo-10-dashboard](demo-10-dashboard/) | A dashboard over real results where missing inputs stay visibly missing |

## Anatomy of a pack

| File | What it holds |
| :--- | :--- |
| `results.md` | The headline verdict, the numbers, and what the run does and does not prove |
| `PROVENANCE.md` | When it ran, against what, on which toolchain, and what was deliberately not exercised |
| `.run-log.txt` | The bounded, redacted tail of the real run output |
| `media/INDEX.md` | Every screenshot and recording, with size and sha256 |
| `media/` | The evidence itself |

Start with `results.md`, then check `PROVENANCE.md` for scope, then open `media/INDEX.md` to see the artifacts and their hashes.

## What "green" means here

- **One run, no retries.** A suite that needs a second attempt is a stability finding, not a pass.
- **A red run is published red.** Nothing is re-run until it looks better.
- **Confirmed findings stay in.** The authorization matrix reports the BOLA finding instead of hiding it.
- **Absence stays visible.** Missing inputs render as "No data yet", never as invented zeros.
- **Every number is traceable.** `results.md` quotes the run; the log and the media are committed next to it.

The packs were produced by the project's own tooling. That tooling — the suites, the harness and the generators — is not published in this repository; what is published is the output and the provenance that explains it.

## The showcase

[`showcase/`](showcase/) holds the 57-second video assembled from these packs' artifacts only: two real mobile recordings and eight evidence cards. `source-manifest.json` records the sha256 of every source; `PROVENANCE.md` explains how it was assembled.
