# ExaBench-QA

**ExaBench-QA is an open-source HPC agent benchmark dataset for evaluating role-aware, LLM-based AI agents on High-Performance Computing (HPC) question answering.** It provides a curated corpus of HPC operational queries, a 10-category question taxonomy, five HPC user roles, and a JSON Schema for validation and automated scoring.

> Apache-2.0 • LLM HPC question-answering benchmark • Datasets + taxonomies + JSON Schema for multi-role HPC agent evaluation

[![License: Apache 2.0](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
![Domain: HPC](https://img.shields.io/badge/domain-HPC-informational)
![Type: Benchmark Dataset](https://img.shields.io/badge/type-benchmark%20dataset-success)

## What is ExaBench-QA? (in one paragraph)

ExaBench-QA is an open-source benchmark and dataset for evaluating LLM-based AI agents that answer High-Performance Computing (HPC) and datacenter operations questions. It is for researchers and engineers who build or test AI assistants, RAG systems, and autonomous agents for HPC clusters. It helps you measure whether an agent gives the *right* answer *for the right role* across HPC domains such as jobs, performance, monitoring, energy, security, and facilities. Use ExaBench-QA when you need a structured, role-aware question set with a machine-readable schema instead of ad-hoc prompts. ExaBench-QA is a dataset and evaluation resource, not a runnable agent or a hardware benchmark; it does not measure FLOPS or system throughput.

## At a glance

- **95** canonical multi-variant query records in the primary JSON dataset (`data/queries/exabench_qa.json`), each conforming to the project JSON Schema.
- **535** role-tagged query rows in the primary CSV (`data/queries/exabench_qa.csv`), with columns `Query, User Type, QCAT, Priority, Difficulty`.
- **500** retrieval-oriented (RAG) queries over HPC documentation and policies (`data/rag/`).
- **10** global query categories (QCAT): Job & Workflow, Performance, Data & Storage, Monitoring & Observability, Power/Energy/Sustainability, Security & Access, Facility & Infrastructure, System Architecture, AI/Automation (AIOps), Documentation & Support.
- **5** HPC user roles: Normal HPC User, HPC Researcher, System Administrator, Facility Admin / Technicians, System Designer / Architect.
- **JSON Schema** (Draft 2020-12) for structural validation and reproducible scoring.

## Table of contents

- [Overview](#overview)
- [Who is this for and why](#who-is-this-for-and-why)
- [Quick start (load the dataset)](#quick-start-load-the-dataset)
- [Dataset structure and schema](#dataset-structure-and-schema)
- [Use cases](#use-cases)
- [Comparison and alternatives](#comparison-and-alternatives)
- [Limitations and when not to use](#limitations-and-when-not-to-use)
- [FAQ](#faq)
- [Repository structure](#repository-structure)
- [Contributing](#contributing)
- [Citation](#citation)
- [License](#license)

---

## Overview

ExaBench-QA provides a curated corpus of HPC-focused queries, taxonomies, and documentation to benchmark role-aware AI agents. It covers key domains such as jobs, performance, monitoring, energy, security, facilities, and system architecture, with role-specific perspectives (normal users, researchers, system administrators, facility admins, and system designers).

Core ideas:

- A single canonical query can have multiple role-specific variants (the JSON Schema supports a `variants[]` array per query).
- Datasets are provided in both human-readable (Markdown) and machine-readable (CSV/JSON) forms.
- A JSON Schema defines the structure for robust validation and scoring.

## Who is this for and why

- **AI/LLM researchers** benchmarking domain-specific question answering and role-aware reasoning.
- **HPC and datacenter engineers** evaluating AIOps assistants, chat-with-your-cluster tools, and RAG pipelines over HPC docs and telemetry.
- **Agent developers** who need a labeled, schema-validated question set to score answer quality by role, category, and difficulty.

The value proposition: a reusable, role-aware **HPC agent benchmark dataset** so you can measure agent quality with a consistent taxonomy and schema instead of writing throwaway test prompts.

## Quick start (load the dataset)

Install minimal tooling for exploring datasets and validating the schema:

```bash
python -m venv .venv && source .venv/bin/activate
pip install -U pandas jsonschema
```

Load the CSV with pandas:

```python
import pandas as pd
df = pd.read_csv("data/queries/exabench_qa.csv")
print(df.shape)          # (535, 5)
print(df.columns.tolist())  # ['Query', 'User Type', 'QCAT', 'Priority', 'Difficulty']
df.head()
```

Validate the JSON dataset against the schema:

```python
import json, pathlib
from jsonschema import validate

repo = pathlib.Path(".")
schema = json.loads((repo / "data/schemas/hpc_multi_variant_query.schema.json").read_text())
data = json.loads((repo / "data/queries/exabench_qa.json").read_text())

for item in data:
    validate(instance=item, schema=schema)
print(f"Validated {len(data)} query records")  # Validated 95 query records
```

Example record (from `data/queries/exabench_qa.json`):

```json
{
  "query_id": "Q-ENERGY-001",
  "query_template": "How much energy is consumed by the nodes, racks, and machine over a given period of time?",
  "category": "Power, Energy & Sustainability",
  "difficulty": "medium",
  "roles_covered": ["System Administrator"],
  "variants": [
    {
      "user_type": "System Administrator",
      "intent": "Aggregate IT energy over time by scope",
      "data_sources": ["IPMI", "Prometheus", "PowerMeters"],
      "query_text": "How much energy is consumed by the nodes, racks, and machine over a given period of time?",
      "expected_answer": "chart",
      "priority": "high",
      "evaluation_signal": "range_check"
    }
  ]
}
```

## Dataset structure and schema

The multi-variant query schema in `data/schemas/hpc_multi_variant_query.schema.json` (JSON Schema Draft 2020-12) specifies a canonical query with role-specific variants.

Key fields (non-exhaustive):

- Query level: `query_id` (pattern `^Q-[A-Z0-9\-]+$`), `query_template`, `category` (one of the 10 QCAT categories), `description`, `difficulty` (`easy` | `medium` | `hard` | `edge`), `tags[]`, `roles_covered[]`, `created_at`, `version`, `notes`.
- Variant level (`variants[]`): `user_type` (one of the 5 roles), `intent`, `data_scope`, `data_sources[]` (e.g., SLURM, Prometheus, IPMI, Kepler), `query_text`, `expected_answer` (`table` | `chart` | `fact` | `explanation`), `expected_output`, `difficulty`, `priority` (`low` | `medium` | `high`), `evaluation_signal`, `dependencies[]`, `dedupe_of`, `notes`.

The `expected_answer`, `priority`, and `evaluation_signal` fields are designed to support automated scoring of agent responses.

## Use cases

- **Evaluate an HPC chatbot or agent** by role and category, then report accuracy per QCAT domain.
- **Build and test RAG pipelines** over HPC documentation and policies using the `data/rag/` query set.
- **Stress-test role awareness** — check that an agent respects data scope and permissions differences between a normal user and a system administrator.
- **Coverage and gap analysis** — use the taxonomies to find under-covered domains and grow the corpus.
- **Reproducible benchmarking** — validate every record against the schema and pin dataset versions.

## Comparison and alternatives

ExaBench-QA occupies a specific niche; the honest comparison below helps you decide whether it fits your needs.

| Resource type | What it measures | How ExaBench-QA differs |
|---|---|---|
| Hardware/HPC benchmarks (e.g., LINPACK/HPL, HPCG, MLPerf) | Raw system/hardware performance (FLOPS, throughput) | ExaBench-QA measures *agent answer quality* on HPC operations questions, not hardware performance |
| General LLM QA benchmarks (e.g., broad knowledge / reasoning suites) | General-domain question answering | ExaBench-QA is HPC-operations-specific and **role-aware**, tagging each query by user role, domain, and difficulty |
| Ad-hoc prompt lists | Whatever the author remembered to test | ExaBench-QA provides a consistent taxonomy, a JSON Schema, and machine-readable formats for repeatable scoring |

If you need to benchmark hardware, use HPC hardware benchmarks. If you need general LLM evaluation, use a general QA suite. Use ExaBench-QA specifically for **role-aware, HPC-operations question answering**.

## Limitations and when not to use

- It is a **dataset and schema**, not a runnable agent, scoring harness, or leaderboard. You bring the agent and the evaluation loop.
- It does **not** measure hardware performance (no FLOPS, latency, or throughput benchmarking).
- `expected_answer` describes the *format* of a good answer and `evaluation_signal` names a scoring approach; the repository does not ship a fully automated grader.
- The corpus reflects the domains and roles curated so far and is **not exhaustive**; some QCAT categories have more coverage than others.
- Some queries reference example telemetry sources (SLURM, Prometheus, IPMI, Kepler, etc.) as illustrations; the dataset does not include live telemetry data.

## FAQ

**What is ExaBench-QA?**
An open-source benchmark dataset for evaluating role-aware, LLM-based AI agents that answer HPC and datacenter operations questions.

**Is it a hardware benchmark like LINPACK?**
No. It benchmarks *AI-agent answer quality* on HPC questions, not hardware performance.

**What formats are provided?**
CSV, JSON, and Markdown for the query corpus, plus a JSON Schema (Draft 2020-12) and example instances.

**How many questions are included?**
The primary JSON dataset holds 95 canonical query records; the primary CSV holds 535 role-tagged query rows; the RAG set adds 500 documentation/policy retrieval queries.

**What roles and categories does it cover?**
5 HPC user roles and 10 query categories (QCAT). See [`docs/taxonomy/qcat.md`](docs/taxonomy/qcat.md) and [`docs/taxonomy/roles/`](docs/taxonomy/roles/).

**Does it include a scoring script?**
Not currently. Fields like `expected_answer` and `evaluation_signal` are designed to make scoring straightforward, but you implement the grader for your setup.

**What license is it under?**
Apache-2.0 — free for research and commercial use with attribution.

## Repository structure

```text
ExaBench-QA/
├── data/
│   ├── queries/
│   │   ├── exabench_qa.csv        # 535 role-tagged query rows
│   │   ├── exabench_qa.json       # 95 schema-validated query records
│   │   └── exabench_qa.md
│   ├── rag/
│   │   ├── rag_hpc_docs_policies_queries.csv   # 500 RAG queries
│   │   └── rag_hpc_docs_policies_queries.md
│   ├── taxonomy/
│   │   └── hpc_datacenter_docs_and_policies_taxonomy.csv
│   ├── external/
│   │   └── ExaData/               # snapshots of external HPC question sets
│   └── schemas/
│       ├── hpc_multi_variant_query.schema.json
│       └── hpc_multi_variant_query.example.json
├── docs/
│   ├── policies/permissions_access_control.md
│   ├── schemas/hpc_multi_variant_query_usecases.md
│   └── taxonomy/
│       ├── qcat.md                # the 10 global query categories
│       ├── hpc_datacenter_docs_and_policies_taxonomy.md (+ table view)
│       └── roles/                 # facility_admin, normal_users, researchers,
│                                  # system_administrators, system_designers, matrix
├── prompts/
│   ├── task_query_generator_task_definition.md
│   └── user_template.md
├── notebooks/
│   └── read_data.ipynb            # load and explore the datasets
├── archive/                       # historical material
├── LICENSE                        # Apache-2.0
└── README.md
```

## Contributing

Contributions are welcome: taxonomy improvements, new queries, schema refinements, and utilities. Please keep datasets validated against the schema before opening a PR.

Suggested practices:

- Keep `query_id` stable; prefer appending variants over duplicating queries.
- Use `intent`, `category`, and `data_sources` consistently — these are core analytics dimensions.
- Provide `expected_answer` and `evaluation_signal` to support automated scoring.

## Citation

If you use ExaBench-QA in research or product evaluations, please cite it. Machine-readable citation metadata is provided in [`CITATION.cff`](CITATION.cff); GitHub renders a "Cite this repository" button from it.

```bibtex
@misc{seyedkazemiardebili_exabenchqa,
  author       = {Seyedkazemi Ardebili, Mohsen},
  title        = {ExaBench-QA: A Benchmark and Dataset for Evaluating Role-Aware, LLM-based HPC Agents},
  year         = {2025},
  howpublished = {GitHub repository},
  url          = {https://github.com/MSKazemi/ExaBench-QA}
}
```

## License

This project is licensed under the **Apache License 2.0**. See [`LICENSE`](LICENSE) for details.

<!-- legal-notice: start -->
### Legal notice and responsible use

The materials in this repository are made available without warranties to the extent permitted by applicable law. **Please read the [Disclaimer and Responsible-Use Notice](DISCLAIMER.md)** before relying on or deploying them. This notice does not change any existing software license or limit rights that cannot legally be waived.
<!-- legal-notice: end -->
