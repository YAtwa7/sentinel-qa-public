# Architecture — how the pieces fit

The project is built in layers, each independently runnable and verifiable.

## 1 — Web

Playwright with strict TypeScript, page objects, and role/text locators. A
setup project signs in once and reuses storage state. The suite covers
authentication, catalogue, cart, checkout, accessibility (axe with a filed
baseline), and visual regression with per-platform PNG baselines. An
anti-bot contract aborts a challenged page as "blocked by bot protection";
a loopback-only practice target proves that abort end to end.

## 2 — API

A local, loopback-confined practice stack. Functional and contract suites are
grounded in a recorded, sha-recorded OpenAPI snapshot; a pinned breaking-change
gate refuses a real breaking diff. Security lanes include a two-identity
authorization matrix, fuzzing, OWASP-category checks, an endpoint crawler, and
a rate-limit test on our own tenant.

## 3 — Mobile

Maestro flows for the practice app on a local Android emulator and an iOS
simulator. Both lanes record the screen during the same run that produces
their JUnit results, so the video is evidence of the run — not a separate demo.

## 4 — Evaluation harness

A deterministic golden-dataset gate with a live-LLM adapter that is
provider-agnostic. Live execution is dispatch-only: without a configured
provider the gate refuses with a named reason. RAG retrieval and RAGAS-style
metrics are thresholded and reported honestly when results fall below target.

## 5 — Agentic resilience

A deterministic self-healer proposes locator fixes as reviewable diffs from
a real failure and DOM snapshot, with guardrails against unsafe changes. A
failure bridge feeds it real JUnit output; a dashboard renders results,
working memory, heal-audit state, and orchestrator state — absent inputs show
as "No data yet" rather than invented zeros.

## 6 — Demos

Ten script-regenerated packs make the above sellable and auditable. Each
pack ships provenance, results, a bounded run log, and sha-swept media. A
guard verifies every pack, every generator's selftest, roster coverage, and
content privacy; the LinkedIn video is a cut of those packs' own artifacts.
