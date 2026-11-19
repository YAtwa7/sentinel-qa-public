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
A small agent roster sits alongside it: judges and an auditor, a working-memory
store with judge exclusion, and an orchestrator that plans work and aggregates
verdicts fail-closed.

## 5 — Agentic resilience

A deterministic self-healer proposes locator fixes as reviewable diffs from
a real failure and DOM snapshot, with guardrails against unsafe changes — it
does not write or auto-merge. A failure bridge feeds it real JUnit output; a
dashboard renders results, working memory, heal-audit state, and orchestrator
state, with absent inputs shown as "No data yet" rather than invented zeros.

Around that core, an operational layer: one fail-closed trigger entry point
over a grounded suite registry (the remote backend dispatches but never
executes), plain-English notifications composed from the same results reader,
and a scheduler that reuses the same registry with a lock and visible skips.

## 6 — Demos

Ten regenerated packs make the above auditable. Each pack ships provenance,
results, a bounded run log, and sha-swept media. The packs were produced by the
project's own tooling in single runs; the tooling itself is not published in
this repository, and the packs are published as output plus provenance. The
showcase video is a cut of those packs' own artifacts.

## What this repository publishes

The working codebase — suites, harness, evaluation stack, generators — is not
public here. This repository publishes the evidence layer: the results, the
provenance that explains them, the media with hashes, and the demonstration
video assembled from them. The [license](../LICENSE)
covers the published material and keeps copyright with the author.
