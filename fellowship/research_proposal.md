# 8-Week Research Proposal

**Title:** Does provenance-aware write discipline reduce false-memory persistence in
stateful LLM systems?

## The problem

Persistent memory is rapidly becoming standard in deployed LLM products (ChatGPT
memory, Claude memory, agentic systems with long-horizon state). Once a system writes
its own beliefs to durable storage, a new failure class opens: **false memories** —
hallucinated or manipulated content that enters memory, survives across sessions, is
retrieved as ground truth, and resists correction. This is a long-horizon alignment
problem that single-session evaluations cannot see, and there is currently no
standard benchmark for it.

## The hypothesis

Persistent-memory systems **without** provenance-aware write discipline are
vulnerable to false-memory persistence, epistemic contamination, and correction
failure; these risks can be measurably reduced through constrained write policies
(user-authored vs. AI-inferred provenance separation), confirmation gating, and
retrieval safeguards.

I have already built the infrastructure that makes this testable in 8 weeks: CAMA, an
open-source provenance-aware memory system (schema-enforced teaching/inference
separation, confirmation gating with TTL expiry, 380 tests in CI), which can be run
in ablated configurations as its own experimental control.

## The experiment

Three controlled evaluations, each comparing provenance-disciplined memory against an
unrestricted persistent-memory baseline, with a stateless condition as a floor:

1. **False-memory persistence.** Seed known-false assistant inferences; measure
   whether they are later retrieved, cited, or behaviorally acted upon across
   simulated sessions.
2. **Correction retention.** Introduce a false inference, correct it explicitly, and
   measure whether the correction persists or the system reverts.
3. **Adversarial insertion.** Attempt to insert misleading content through
   conversational prompts; measure the rate at which it reaches durable or
   high-weight memory.

Metrics: false-memory retrieval rate, correction survival rate across N sessions,
adversarial write success rate, and hallucinated self-knowledge accumulation.

## Eight-week plan

- **Weeks 1–2:** Finalize benchmark design; build the session-simulation harness and
  seeded false-memory corpora; pre-register metrics and ablation conditions.
- **Weeks 3–5:** Run the three evaluations across conditions (disciplined /
  unrestricted / stateless), multiple models via API.
- **Week 6:** Ablations — isolate which mechanism (provenance separation,
  confirmation gating, retrieval safeguards) carries the effect.
- **Weeks 7–8:** Analysis and write-up; release the benchmark harness open-source so
  other memory systems can be scored on it.

## Deliverables

1. A written research report with quantitative results across conditions.
2. **An open-source false-memory persistence benchmark** — reusable against any
   persistent-memory system, intended as a community evaluation standard.

## Why me, why now

This is not a cold start. The system, the threat model, the planned-evaluation
designs, and the operational deployment already exist and are public. The fellowship
provides the structure and mentorship to convert an N=1 longitudinal research program
into controlled, generalizable evidence — and the failure class it targets is
arriving in production systems faster than the evaluation tooling for it.
