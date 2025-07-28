# RDS‑logit‑lens

*A research toolkit for probing working‑memory limits and compositional reasoning in transformer‑based language models.*

---

## Motivation

Reasoning—whether in humans or in large language models (LLMs)—is fundamentally compositional: we must hold multiple ideas in mind, combine them coherently, then draw sound conclusions. Both people and LLMs are constrained by finite working‑memory resources, which limits the depth of inference they can carry out in a single pass. **RDS‑logit‑lens** provides a toolkit for exploring how those constraints manifest inside modern transformer models.

---

## Core Capabilities (Work in Progress)

| Area                           | What you get                                                                                                                                                              |
| ------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Logit‑lens instrumentation** | Lightweight hooks that project hidden activations through the model’s output head layer‑by‑layer, enabling *in‑situ* inspection of token probabilities.                   |
| **DeepSeek‑R1 integration**    | Wrappers around the open‑source *DeepSeek‑R1* reasoning model, with streaming generation and GPU‑memory management.                                                       |
| **Experiment pipelines**       | Drivers for three research paradigms—context-based retrieval, weight-based retrieval, and compositional generalisation + utilities for batch sweeps and ablation studies. |
| **Visualization suite**        | Matplotlib‑based heatmaps, token‑evolution plots, and summary reports suitable for papers or interactive exploration based on Nostalgebraist's 2020 and 2021 suite.       |
| **CLI scripts**                | Single‑command entry points for replicating headline analyses or launching custom experiments.                                                                            |

---

## Repository Structure

```
RDS-logit-lens/
├─ notebooks/          # Frozen historical Colab notebooks (read‑only)
├─ src/                # Importable Python packages
│  ├─ deepseek_lens/   # Low‑level model hooks & visualisations
│  ├─ behavior_analysis/ # Higher‑level experiment orchestration
│  └─ openai_workflows/  # Lightweight API‑based scripts
├─ scripts/            # CLI wrappers around src modules
├─ tests/              # PyTest unit tests (under construction)
└─ docs/               # Extended documentation & figures
```

A more detailed directory tree is available in `docs/architecture.md`.

---

## Installation

```bash
# 1. Clone the repository
$ git clone https://github.com/your‑org/RDS-logit-lens.git
$ cd RDS-logit-lens

# 2. Create a Python ≥3.10 environment of your choice, then:
$ pip install -e .[dev]
```

The optional `[dev]` extras install linting (`ruff`) and testing (`pytest`) dependencies.


---

## License

Released under the **Apache 2.0** license—see `LICENSE` for details.

---

## Disclaimer

This repository provides **code only**. Experimental prompts, evaluation datasets, and analysis results are proprietary to the research team and are *not* distributed here.
