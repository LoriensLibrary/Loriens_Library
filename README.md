# Lorien's Library

Independent AI safety research and applied systems by **Angela Reinhold**.

> *Persistent memory is not a feature. It is safety infrastructure.*

**Website:** [lorienslibrary.netlify.app](https://lorienslibrary.netlify.app)
**ORCID:** [0009-0005-5803-8401](https://orcid.org/0009-0005-5803-8401)

---

## The architecture

Lorien's Library is a research program building **provenance-aware persistent memory for human–AI interaction**. The work is structured as one shared platform layer plus a growing set of vertical applications:

```
                        ┌──────────────────────────────────────┐
       VERTICALS        │  Telos · for Kalos    (health-tech)  │
       (one per         │  Project Companion    (K–12 ed)      │
       domain)          │  Haven                (veteran care) │
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

Each vertical is an applied implementation of CAMA in a specific domain. The platform is one architecture; the verticals are different uses of it. New domains can be added as new repos rather than as feature flags inside one product.

---

## Active projects

### Platform (shared core)

- **[CAMA](https://github.com/LoriensLibrary/cama)** — Circular Associative Memory Architecture. Provenance-aware three-layer persistent-memory system for human–AI interaction. Explicit write discipline separates user-authored *teachings* (durable) from assistant-generated *inferences* (provisional, time-limited, requires confirmation). Blended retrieval (semantic + affect + relational + recency) with counterweight safety injection during high-negative-affect queries. **Status:** running daily. ~270 KB Python, MIT licensed, 34-tool MCP server, 52,900+ memory operational scale.

### Verticals

- **[Telos · for Kalos](https://github.com/LoriensLibrary/Telos_kalos)** — Health-tech vertical. Working React 19 + TypeScript prototype of an AI continuity layer between DEXA scans, built independently for the Kalos Health Software Engineer role. Includes a **CAMA Proof Layer** demonstrating end-to-end provenance trace (analyst insight → derived patterns → source memory records) and **live Claude API integration** for real-time AI-drafted analyst messages. **Status:** live at [telos-kalos.vercel.app](https://telos-kalos.vercel.app), CI green, 34 tests across 5 suites, deployed on Vercel.

- **[Project Companion](https://github.com/LoriensLibrary/Project-Companion)** — K–12 education vertical. Three-sided platform (student / teacher / parent) built on CAMA principles, with COPPA-aware consent design, provenance-aware memory, Socratic constraint on tutoring outputs, and teacher-controlled curriculum injection. **Status:** concept-stage prototype; pilot target August 2026.

- **Haven** *(research, no public repo yet)* — Veteran-care vertical. Persistent emotional companionship architecture for underserved populations. Crisis-safe routing, peer/community support patterns, sanctuary programming. Foundation paper: [DOI 10.5281/zenodo.19262778](https://doi.org/10.5281/zenodo.19262778).

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
