# Questionnaire — Draft Answers

Adapt to the actual form fields. Written in first person, ready to trim.

---

## Background

I'm an independent AI safety researcher and founder of Lorien's Library LLC, currently
completing a computer science degree (AI concentration) at Full Sail University. My
research program centers on one thesis: **the moment an LLM-based system remembers
anything across sessions, it becomes safety-critical** — and the discipline for *how*
it remembers has to be designed in, not bolted on.

Over the past year I've built and published that argument end-to-end, working
independently:

- **Eleven DOI-registered preprints** (Zenodo, ORCID 0009-0005-5803-8401) covering
  the core memory architecture, an empirical continuity-burden case study, a safety
  evaluation framework, and applied extensions (healthcare, education, long-duration
  spaceflight, veteran care).
- **CAMA**, a working provenance-aware persistent-memory system: a Python MCP server
  plus HTTP API with 380 tests in CI, an 18-row threat model, 27/27 safety benchmarks
  passing against a live 53,000-memory corpus, and published retrieval-latency
  benchmarks (p50 43 ms / p99 61 ms at that scale).
- **A published dataset** (aggregate statistics from a 66,380-message longitudinal
  corpus) on HuggingFace.
- **Two applied prototypes** — a live-deployed health-tech app with Claude API
  integration and an end-to-end provenance trace, and a K-12 education design
  prototype with COPPA-aware consent design.

I have no institutional affiliation and no alignment publication in a peer-reviewed
venue — everything above was self-directed, self-funded, and shipped with the proofs
and scope boundaries documented (see the evidence matrix in the CAMA repo).

## What I'm currently working on

CAMA's core safety claim — that provenance-aware write discipline (separating
user-authored durable "teachings" from AI-generated provisional "inferences" that
require confirmation) reduces false-memory persistence and epistemic contamination in
stateful LLM systems — is currently supported by architecture, contract tests, and
N=1 longitudinal observation. I've designed the controlled evaluations that would
test it properly (false-memory persistence benchmarking, correction retention across
sessions, adversarial memory insertion, write-discipline ablations) and I'm now
building toward running them. That is exactly the project I'd bring to this
fellowship — see my proposal.

I'm also maintaining the operational CAMA deployment (running daily), and recently
shipped the multi-tenant generalization of the architecture and its public HTTP API
with architecturally-enforced provenance contracts.

## Links to relevant work

- Portfolio index: https://github.com/LoriensLibrary/Loriens_Library
- CAMA (core system + evidence matrix + threat model): https://github.com/LoriensLibrary/cama
- *Memory as Safety Infrastructure* (safety argument): https://doi.org/10.5281/zenodo.19244253
- *Continuity Burden in Longitudinal Human-AI Interaction* (empirical case study): https://doi.org/10.5281/zenodo.19226509
- Continuity Burden dataset: https://huggingface.co/datasets/LoriensLibrary/cama-continuity-burden
- Live applied prototype: https://telos-kalos.vercel.app
- All publications: https://orcid.org/0009-0005-5803-8401
