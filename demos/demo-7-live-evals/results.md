# demo-7-live-evals results

- summary: GREEN - deterministic leg rc 0;
  keyless live refusal rc 2; unknown-provider refusal rc 2;
  dispatch-only workflow confirmed
- what is proven: the offline judge holds the golden dataset at its
  threshold, and the live path REFUSES without a configured provider -
  including a provider-agnostic refusal that names all 5 known providers
  (gemini, groq, grok, openai, generic)
- what is NOT proven: that any live provider answered correctly. This
  pack is dispatch-only by design; a live adjudication is a manual
  workflow run with a configured key, never a demo re-run to green
- media: three rendered transcripts of the REAL gate output
  (media/evidence/, sha-swept via media/INDEX.md)
- the bounded, redacted run log: .run-log.txt

## honest framing

The headline is the REFUSAL, not a faked live score. A gate that runs a
live LLM without a key is a gate that lies; this one exits 2 and names
the missing configuration. A red leg is committed as red - no retries.
