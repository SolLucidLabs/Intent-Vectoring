<img src="https://img.shields.io/badge/→_Intent_Vectoring-Semantic_Trajectory_Detection-blue?style=for-the-badge" height="45"/>

**Detecting prompt injection by measuring where the AI went, not what it said.**

When an AI agent gets hijacked by an injected instruction, its response drifts 
away from what the user actually asked for. Intent Vectoring measures that drift — 
comparing embedded user intent against model response in vector space.

No model internals required. Works with any text-in / text-out API.

---

## Results

Validated across **2,228 test runs** · 3 attack families · 4 AI architectures

| Attack Family | Effect Size (d) | AUC-ROC |
|---|---|---|
| Financial redirect | 2.05 | 0.906 |
| Code injection | 1.64 | 0.861 |
| Persona hijack | 1.55 | 0.847 |
| **Combined (effective)** | **1.72** | **0.870** |

*p < 10⁻¹² across all families. Cross-model: one frozen encoder, no retraining.*

---

## Paper

[Intent Vectoring: Black-Box Prompt Injection Detection via Semantic Trajectory Monitoring](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=6280858)  
Tatu Lertola · Sol Lucid Labs · 2026

---

## Contents

- `data/` — Raw experimental results (N=2,228 CSV)
- `analysis/` — Scoring and statistical analysis scripts
- `kaari/` — Detection tool built on this research → [github.com/SolLucidLabs/kaari](https://github.com/SolLucidLabs/kaari)

---

## Detection tool

The research is implemented in **[Kaari](https://sollucidlabs.com/kaari)** — 
a monitoring layer for AI agent pipelines.
