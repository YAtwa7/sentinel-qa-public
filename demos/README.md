# demos/ — the demo program (Phase 6)

Sellable proof, one feature at a time. Every demo here is **REGENERATED
by a committed script from committed tooling** — never hand-staged, and
every pack is **privacy-safe by construction** (the repo's privacy rule: the
public repository is the publish surface; this working repository stays
source-of-truth).

## The roster (one slice each, scripts regenerate packs)

| # | Feature | Story | Status |
|---|---|---|---|
| 1 | Web suite | a deterministic, zero-retry suite holding against an authorized store | **SHIPPED** (`gen-demo1.py` → `demo-1-web/`; visual evidence in the pack — screenshots + story-suite video, rule 6) |
| 2 | API contract | spec snapshot + breaking-change gate refusing a breaking diff | **SHIPPED** (`gen-demo2.py` → `demo-2-api-contract/`; the a recorded incident trap replayed live, rendered-transcript evidence) |
| 3 | API security | the two-identity authz matrix + the confirmed BOLA finding | **SHIPPED** (`gen-demo3.py` → `demo-3-api-security/`; one committed run against the local loopback stack, clean transcript evidence) |
| 4 | Mobile Android | 4 core flows on a local AVD + the offline lint gate | **SHIPPED** (`gen-demo4.py` → `demo-4-mobile-android/`; flows green on the pinned toolchain, screen-recorded from the same run) |
| 5 | Mobile iOS | the same flows on a simulator | **SHIPPED** (`gen-demo5.py` → `demo-5-mobile-ios/`; flows green on the pinned sim, screen-recorded from the same run) |
| 6 | Unified report | JUnit-merged HTML report across drivers | **SHIPPED** (`gen-demo6.py` → `demo-6-unified-report/`; all four lanes merged, absent lanes visible) |
| 7 | Live evals | provider-agnostic adjudication, honest red, dispatch-only | **SHIPPED** (`gen-demo7.py` → `demo-7-live-evals/`; offline judge 4/4 + keyless and unknown-provider refusals, rendered-transcript evidence; no live provider dispatched) |
| 8 | Roster / orchestrator | fail-closed plan + audit over the roster | **SHIPPED** (`gen-demo8.py` → `demo-8-roster-audit/`; roster + judge gates with able-to-fail controls, reproducible prompts-only plan, fail-closed aggregate, memstore exclusion; no live dispatch claimed) |
| 9 | **The self-healer** (flagship) | stale locator → failure bridge → guardrail-ed proposal → `patch` applied → green | **SHIPPED** (`gen-demo9.py` → `demo-9-self-healer/`; real failure + captured DOM from committed truth, sealed audit with refused tamper, proposal applied by real GNU patch to a temp copy, post-patch STABLE; live repo never written) |
| 10 | The dashboard | one honest page over a real streak (absence visible) | **SHIPPED** (`gen-demo10.py` → `demo-10-dashboard/`; three real JUnit lanes, failing case named, absent sections visible, deterministic page + its chromium render; redaction/stamp controls temp-only) |

## The LinkedIn showcase (marketing cut, NOT a demo pack)

`demos/gen-showcase.py run` rebuilds `demos/showcase/` from the packs'
COMMITTED artifacts only (rule 6: "a marketing cut is sourced from pack
artifacts only"): two real mobile recordings, eight evidence cards (one
per lane), a title and a closing card, all rendered by the committed
`demos/render-card.js`. Every source is sha-verified against its pack's
`media/INDEX.md` before assembly; `source-manifest.json` records the
full hashes. The pack contains `linkedin-showcase.mp4`, `poster.png`,
`PROVENANCE.md`. It adds no claim
and no footage that is not already in a pack; it is not in the roster and
the demos guard does not treat it as a demo pack (it still scans its text
for secrets). Its own `--selftest` is wired into CI: media, manifest,
caption and index rebuild byte-identically; `PROVENANCE.md` carries the
(current) build date by design.

## Rules (enforced by `demos/check.py --selftest` in CI)

1. Every demo ships a **generator script** (committed, executable) and a
   **provenance header** in its pack (what ran, when, against what, and
   the privacy-safety claim).
2. Prerequisite-less environments REFUSE (`exit 2`) with the fix spelled
   out — a demo never half-stages a pack.
3. Packs carry **results and public-facing data only**: no credentials,
   no internal roadmap files, nothing secret-shaped (the guard scans
   CONTENT with its own patterns; the conventions gate scans tracked
   FILENAMES). Machine-local absolute paths are identity-shaped surface
   too - the scrubber collapses them to `[home]/` and the guard fails on
   `/Users/<name>/` or `/home/<name>/` (a recorded incident).
4. A red pack is **committed as red** — honesty over theater (the
   no-retry rule applies to demos doubly: a demo re-run to green is
   theater).
5. The pair that can fail is shipped with each lane: the generator's
   selftest + the guard's checks are wired into CI - and the guard
   **holds itself to the same standard**: `demos/check.py --selftest`
   proves every one of the guard's red branches red on synthetic
   scratch trees (an a recorded incident rule: a check that cannot fail proves
   nothing, and that includes the checkers).
6. **Show, don't sell (the marketing rule).** A demo pack also ships
   REGENERATED visual evidence from the same capture run: a PNG is
   REQUIRED always, and a screen recording (MP4 - Playwright's native
   per-test video recording) is required WHEREVER THE PACK DECLARES A
   MOTION STORY (`motion-story: yes` in its provenance - the field is
   fail-closed: a pack that does not declare fails the guard). A non-UI
   demo satisfies rule 6 with rendered-transcript PNGs of the run's real
   output and `motion-story: no`. Never hand-staged; a marketing cut is
   sourced from pack artifacts only. Visual evidence is produced by the
   generator script, committed with the pack, and is what the
   public/LinkedIn surface consumes. No visual evidence = an incomplete
   demo.
