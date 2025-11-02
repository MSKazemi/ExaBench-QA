# ExaBench-QA
Benchmark and dataset for evaluating LLM-based HPC agents across user roles, telemetry domains, and observability tasks.

> Apache-2.0 • Datasets + taxonomies + schema for multi-role HPC agent evaluation

### Contents
- **Overview**
- **What’s in this repo**
- **Quick start**
- **Datasets** (queries, RAG docs/policies, taxonomies)
- **Schema** (multi-variant query JSON Schema + validation)
- **Prompts & notebooks**
- **Repository structure**
- **Contributing, Citation, License**

---

### Overview
ExaBench-QA provides a curated corpus of HPC-focused queries, taxonomies, and documentation to benchmark role-aware AI agents. It covers key domains such as jobs, performance, monitoring, energy, security, facilities, and system architecture, with role-specific perspectives (normal users, researchers, system administrators, facility admins, and system designers).

Core ideas:
- A single canonical query can have multiple role-specific variants.
- Datasets are split into human-readable docs and machine-readable tables/JSON.
- A JSON Schema defines the structure for robust validation and scoring.

---

### What’s in this repo
- **Docs and taxonomies**
  - Global query categories (QCAT): `docs/taxonomy/qcat.md`
  - HPC datacenter docs/policies taxonomy: `docs/taxonomy/hpc_datacenter_docs_and_policies_taxonomy.md` (+ table view)
  - Role taxonomies: `docs/taxonomy/roles/` (facility admins, normal users, researchers, sysadmins, system designers)
  - Permissions & access policy: `docs/policies/permissions_access_control.md`
- **Datasets**
  - Primary queries: `data/queries/exabench_qa.{csv,json,md}`
  - RAG queries for docs/policies: `data/rag/hpc_docs_policies_rag_queries.{csv,md}` (if present)
  - Taxonomy CSVs: `data/taxonomy/`
  - External sources snapshot: `data/external/ExaData/`
- **Schema**
  - Multi-variant query schema: `data/schemas/hpc_multi_variant_query.schema.json`
  - Example: `data/schemas/hpc_multi_variant_query.example.json`
- **Prompts**
  - Prompt/task templates: `ai_task_template/` (may be renamed to `prompts/`)
- **Notebooks**
  - Exploration/utilities: `notebooks/read_data.ipynb`
- **Archive**
  - Historical material: `archive/`

---

### Quick start
Install minimal tooling for exploring datasets and validating schema.

```bash
python -m venv .venv && source .venv/bin/activate
pip install -U pandas jsonschema
```

Validate JSON dataset against the schema:

```python
import json, pathlib
from jsonschema import validate

repo = pathlib.Path('.')
schema = json.loads((repo / 'data/schemas/hpc_multi_variant_query.schema.json').read_text())
data = json.loads((repo / 'data/queries/exabench_qa.json').read_text())

for i, item in enumerate(data):
    validate(instance=item, schema=schema)
print(f"Validated {len(data)} items ✔")
```

Load the CSV with pandas:

```python
import pandas as pd
df = pd.read_csv('data/queries/exabench_qa.csv')
df.head()
```

---

### Datasets
- **Primary queries** (`data/queries/`)
  - CSV/JSON/MD representations of benchmark questions spanning domains like jobs, performance, monitoring, energy, security, facility, architecture, AIOps, and docs.
  - Each row (or JSON object) includes fields such as `query_id`, `category`, `difficulty`, and role-specific `variants` with `intent`, `data_sources`, `expected_answer`, and `evaluation_signal`.

- **RAG docs/policies queries** (`data/rag/`)
  - Queries designed for retrieval over documentation and policy artifacts; complements telemetry-oriented queries.

- **Taxonomies** (`docs/taxonomy/` + `data/taxonomy/`)
  - Human-readable taxonomies and their machine-readable CSV counterparts to support filtering, coverage analysis, and dataset growth.

- **External sources** (`data/external/ExaData/`)
  - Snapshots of external HPC-related question sets and references used for inspiration and cross-checking.

---

### Schema
The multi-variant query schema in `data/schemas/hpc_multi_variant_query.schema.json` specifies a canonical query with role-specific variants.

Key fields (non-exhaustive):
- `query_id`, `query_template`, `category`, `description`, `difficulty`, `tags`
- `variants[]`: `user_type`, `intent`, `data_scope`, `data_sources[]`, `query_text`, `expected_answer`, `expected_output`, `difficulty`, `priority`, `evaluation_signal`, `dependencies[]`, `dedupe_of`, `notes`
- `created_at`, `version`, `notes`

Validation snippet is provided in Quick start. Consider pinning versions when building reproducible benchmarks.

---

### Prompts & notebooks
- Prompt/task templates for generating or classifying queries live in `ai_task_template/` (recommended future path: `prompts/`).
- `notebooks/read_data.ipynb` offers a lightweight starting point to explore and validate datasets.

---

### Repository structure
```bash
ExaBench-QA/
├── docs/
│   ├── policies/
│   │   └── permissions_access_control.md
│   └── taxonomy/
│       ├── qcat.md
│       ├── hpc_datacenter_docs_and_policies_taxonomy.md
│       ├── hpc_datacenter_docs_and_policies_taxonomy_table.md
│       └── roles/
│           ├── facility_admin.md
│           ├── normal_users.md
│           ├── researchers.md
│           ├── system_administrators.md
│           └── system_designers.md
├── data/
│   ├── queries/
│   │   ├── exabench_qa.csv
│   │   ├── exabench_qa.json
│   │   └── exabench_qa.md
│   ├── rag/
│   │   ├── hpc_docs_policies_rag_queries.csv
│   │   └── hpc_docs_policies_rag_queries.md
│   ├── taxonomy/
│   │   └── hpc_datacenter_docs_and_policies_taxonomy.csv
│   ├── external/
│   │   └── ExaData/
│   │       ├── CINECA_Questions.md
│   │       ├── ExaData.md
│   │       └── ODA_Agent_Queries.md
│   └── schemas/
│       ├── hpc_multi_variant_query.example.json
│       └── hpc_multi_variant_query.schema.json
├── ai_task_template/
├── notebooks/
│   └── read_data.ipynb
├── archive/
│   ├── hpc_user_taxonomy.md
│   └── queries_old.md
├── LICENSE
└── README.md
```

---

### Contributing
Contributions are welcome: taxonomy improvements, new queries, schema refinements, and utilities. Please use clear commit messages and keep datasets validated against the schema before PRs.

Suggested practices:
- Keep `query_id` stable; prefer appending variants over duplicating queries.
- Use `intent`, `category`, and `data_sources` consistently—these are core analytics dimensions.
- Provide `expected_answer` and `evaluation_signal` to support automated scoring.

---

### Citation
If you use ExaBench-QA in research or product evaluations, please cite this repository. You can add a `docs/citation.md` later with a formal reference. A suggested placeholder:

> ExaBench-QA: A Dataset and Schema for Evaluating Role-Aware HPC Agents (2025). GitHub repository. https://github.com/<org>/ExaBench-QA

---

### License
This project is licensed under the **Apache License 2.0**. See `LICENSE` for details.

