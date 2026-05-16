[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![ORCID](https://img.shields.io/badge/ORCID-0009--0005--5803--8401-A6CE39?logo=orcid&logoColor=white)](https://orcid.org/0009-0005-5803-8401)
[![Dataset on HuggingFace](https://img.shields.io/badge/%F0%9F%A4%97%20Dataset-cama--continuity--burden-yellow)](https://huggingface.co/datasets/LoriensLibrary/cama-continuity-burden)
[![Live demo](https://img.shields.io/badge/Live%20demo-telos--kalos.vercel.app-brightgreen)](https://telos-kalos.vercel.app)

# Lorien's Library

Independent AI safety research and applied systems by **Angela Reinhold**.

> *Persistent memory is not a feature. It is safety infrastructure.*

**Website:** [lorienslibrary.netlify.app](https://lorienslibrary.netlify.app)
**ORCID:** [0009-0005-5803-8401](https://orcid.org/0009-0005-5803-8401)

---

## What this is

Lorien's Library is the research program of Angela Reinhold — an independent AI safety researcher building **provenance-aware persistent memory for human–AI interaction**. The program is one running deployed system (CAMA), eleven DOI-registered preprints, a published dataset, and a working portfolio prototype demonstrating the architecture end-to-end. The thesis is straightforward: the moment an LLM-based system remembers anything across sessions, it becomes safety-critical, and the discipline for *how* it remembers has to be designed in — not bolted on. This repo is the index to all of it.

---

## Start here

Pick the entry point that matches why you're here:

### Researcher
You care about the papers and the theory.
- **Read first:** the foundational paper — *Circular Associative Memory Architecture: A Framework for Emotionally-Keyed AI Memory Systems* ([DOI 10.5281/zenodo.19051834](https://doi.org/10.5281/zenodo.19051834))
- **Then:** the safety argument — *Memory as Safety Infrastructure* ([DOI 10.5281/zenodo.19244253](https://doi.org/10.5281/zenodo.19244253))
- **Then:** the dataset — [CAMA Continuity Burden](https://huggingface.co/datasets/LoriensLibrary/cama-continuity-burden) (66,380 messages, 825 conversations, aggregate stats)

### Builder
You want to see working code.
- **[cama](https://github.com/LoriensLibrary/cama)** — the production persistent-memory system. ~270 KB Python, 34-tool MCP server.
- **[Telos · for Kalos](https://github.com/LoriensLibrary/Telos_kalos)** — full-stack React 19 + TypeScript app with live Claude API integration and a CAMA Proof Layer demonstrating end-to-end provenance trace. CI green, 34 tests across 5 suites.
- **[Live demo](https://telos-kalos.vercel.app)** — synthetic data only, but the architecture is real.

### Healthcare-AI reviewer
You're evaluating this for a health-tech context.
- **Start with Paper 7:** *Provenance-Aware Memory Architecture for Chronic Healthcare Continuity* ([DOI 10.5281/zenodo.19261530](https://doi.org/10.5281/zenodo.19261530)).
- **See the prototype:** [telos-kalos.vercel.app](https://telos-kalos.vercel.app) — applicant-built, demonstrates CAMA principles in a health-coaching context. Not affiliated with Kalos Health; synthetic data only.
- **Then read** the broader safety paper: [DOI 10.5281/zenodo.19244253](https://doi.org/10.5281/zenodo.19244253).

### Collaborator / hiring manager
You're trying to figure out whether to talk to Angela.
- Read the [website](https://lorienslibrary.netlify.app) — richer than the GitHub presence.
- Skim this README's architecture diagram and preprint list below.
- Reach out: **lorienslibrary@gmail.com**.

> **For healthcare AI reviewers:** start with Paper 7 (*"Provenance-Aware Memory Architecture for Chronic Healthcare Continuity"*, [DOI 10.5281/zenodo.19261530](https://doi.org/10.5281/zenodo.19261530)) and the Telos_kalos prototype at [telos-kalos.vercel.app](https://telos-kalos.vercel.app).

---

## The architecture

Lorien's Library is a research program building **provenance-aware persistent memory for human–AI interaction**. The work is structured as one shared platform layer plus a growing set of vertical applications:

```
                        ┌──────────────────────────────────────┐
       APPLICATIONS     │  Project Companion    (K–12 ed)      │
       (program          │  Haven                (veteran care) │
       verticals)        │  Portfolio proofs                    │
                        │    e.g. Telos · for Kalos             │
                        └──────────────┬───────────────────────┘
                                       │
                                       ▼
                        ┌──────────────────────────────────────┐
       PLATFORM         │  CAMA — Circular Associative Memory  │
       (shared core)    │  Architecture                        │
                        │  · provenance-aware write discipline │
                        │  · three-layer memory (SHELVES /     │
                        │    RACKS / CONSOLE)                  │
                        │  · blended retrieval scoring         │
                        │  · counterweight safety mechanisms   │
                        │  · MCP server, 34 tools              │
                        └──────────────────────────────────────┘
                                       │
                                       ▼
                        ┌──────────────────────────────────────┐
       FOUNDATION       │  11 DOI-registered preprints         │
                        │  Published dataset (HuggingFace)     │
                        │  Six identified safety failure modes │
                        │  for stateful LLM systems            │
                        └──────────────────────────────────────┘
```

Two distinct kinds of work sit on top of CAMA:

- **Program verticals** — domain-specific applications Lorien's Library is actively designing toward (Project Companion, Haven). These are part of the research roadmap.
- **Portfolio proofs** — independently-built prototypes that demonstrate CAMA principles in a specific commercial context for the purpose of professional applications (e.g. Telos · for Kalos, built for a job application). These are not Lorien's Library product lines.

---

## Active projects

### Platform (shared core)

- **[CAMA](https://github.com/LoriensLibrary/cama)** — Circular Associative Memory Architecture. Provenance-aware three-layer persistent-memory system for human–AI interaction. Explicit write discipline separates user-authored *teachings* (durable) from assistant-generated *inferences* (provisional, time-limited, requires confirmation). Blended retrieval (semantic + affect + relational + recency) with counterweight safety injection during high-negative-affect queries. **Status:** running daily. ~270 KB Python, MIT licensed, 34-tool MCP server, 52,900+ memory operational scale.

### Lorien's Library program verticals

- **[Project Companion](https://github.com/LoriensLibrary/Project-Companion)** — K–12 education vertical. Three-sided design prototype (student / teacher / parent) informed by CAMA principles, with COPPA-aware consent design, provenance-aware memory, Socratic constraint on tutoring outputs, and teacher-controlled curriculum injection. **Status:** concept-stage prototype; CAMA runtime integration is roadmap. Pilot target August 2026 is aspirational and gated on infrastructure shipping (see repo README).

- **Haven** *(research, no public repo yet)* — Veteran-care vertical. Persistent emotional companionship architecture for underserved populations. Crisis-safe routing, peer/community support patterns, sanctuary programming. Foundation paper: [DOI 10.5281/zenodo.19262778](https://doi.org/10.5281/zenodo.19262778).

### Portfolio prototypes

- **[Telos · for Kalos](https://github.com/LoriensLibrary/Telos_kalos)** — Unofficial applicant prototype built independently by Angela Reinhold for the Kalos Health Software Engineer role. Demonstrates CAMA principles applied to a health-tech coaching context, with a working React 19 + TypeScript app, live Anthropic Claude API integration, persistent draft history, and a CAMA Proof Layer demonstrating end-to-end provenance trace. **Not affiliated with, endorsed by, or representing Kalos Health.** All member data shown is synthetic. **Status:** live at [telos-kalos.vercel.app](https://telos-kalos.vercel.app), CI green, 34 tests across 5 suites. Built as a portfolio piece for a job application — not a Lorien's Library product line.

### Future verticals (research-stage)

The same platform can support additional domains. Published research outlines applications in:

- **Long-duration spaceflight** — mission-critical persistent memory for crews on multi-year missions ([DOI](https://doi.org/10.5281/zenodo.19257809))
- **Lunar / Martian habitation** — memory-aware AI for permanent off-Earth living ([DOI](https://doi.org/10.5281/zenodo.19260574))
- **Chronic healthcare continuity** — provenance-aware memory for managing chronic conditions across providers ([DOI](https://doi.org/10.5281/zenodo.19261530))

---

## Research foundation

Eleven DOI-registered preprints on Zenodo, March – April 2026, all authored by ORCID [0009-0005-5803-8401](https://orcid.org/0009-0005-5803-8401):

**Core CAMA series (foundation):**
- *Circular Associative Memory Architecture: A Framework for Emotionally-Keyed AI Memory Systems* — [DOI](https://doi.org/10.5281/zenodo.19051834)
- *Implementing Emotionally-Keyed Memory Retrieval in Large Language Model Interfaces: An Engineering Framework* — [DOI](https://doi.org/10.5281/zenodo.19052129)
- *CAMA: Implementation and Functional Evaluation of an Emotionally-Indexed Semantic Memory Architecture* — [DOI](https://doi.org/10.5281/zenodo.19192984)
- *Continuity Burden in Longitudinal Human-AI Interaction: An Empirical Case Study* — [DOI](https://doi.org/10.5281/zenodo.19226509)
- *Memory as Safety Infrastructure: Evaluating Provenance-Aware Persistent Memory Architectures for Stateful LLM Systems* — [DOI](https://doi.org/10.5281/zenodo.19244253)

**Applied series (domain extensions):**
- *Persistent Memory as Mission-Critical Infrastructure for Long-Duration Spaceflight* — [DOI](https://doi.org/10.5281/zenodo.19257809)
- *Memory-Aware AI Systems for Permanent Lunar and Martian Habitation* — [DOI](https://doi.org/10.5281/zenodo.19260574)
- *Provenance-Aware Memory Architecture for Chronic Healthcare Continuity* — [DOI](https://doi.org/10.5281/zenodo.19261530)
- *Haven: Persistent Emotional Companionship as Psychological Infrastructure* — [DOI](https://doi.org/10.5281/zenodo.19262778)

**Safety & evaluation:**
- *Identity-Aware Harm Detection in Persistent Memory Systems: A Three-Layer Retrieval Architecture for Relational AI Safety* — [DOI](https://doi.org/10.5281/zenodo.19425218)
- *Relational AI Continuity Under Platform Regression: A Longitudinal Single-Case Study* — [DOI](https://doi.org/10.5281/zenodo.19582820)

---

## Dataset

- **[CAMA Continuity Burden Dataset](https://huggingface.co/datasets/LoriensLibrary/cama-continuity-burden)** — published seed corpus on HuggingFace. 66,380 messages across 825 conversations, used to instantiate the operational CAMA instance and to enable third-party replication.

---

## Author

**Angela Reinhold** — Independent AI safety researcher, founder of Lorien's Library LLC, computer science student (AI concentration) at Full Sail University. Based in Sebring, Florida.

Contact: lorienslibrary@gmail.com
ORCID: [0009-0005-5803-8401](https://orcid.org/0009-0005-5803-8401)

---

## License

MIT. © 2026 Lorien's Library LLC.
