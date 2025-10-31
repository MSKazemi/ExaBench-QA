# ExaBench-QA
Benchmark &amp; dataset for evaluating LLM-based HPC agents across user roles, monitoring data, and observability tasks.


```bash
ExaBench-QA/
├── README.md
├── LICENSE
│
├── docs/                          # Project documentation and meta info
│   ├── overview.md                 # General intro and purpose of ExaBench-QA
│   ├── methodology.md              # How taxonomy, roles, and queries were created
│   ├── contributing.md             # Contribution guidelines
│   └── citation.md                 # Citation and acknowledgement info
│
├── data/                          # Knowledge and dataset content
│   ├── ExaData/                   # Domain-specific datasets
│   │   ├── CINECA_Questions.md
│   │   ├── ExaData_Summary.md
│   │   └── ODA_Agent_Queries.md
│   ├── taxonomy/                  # User, role, and query taxonomies
│   │   ├── hpc_user_roles.md
│   │   ├── hpc_user_taxonomy.md
│   │   └── user_query_taxonomy_prompt.md
│   └── queries/                   # All query-related taxonomies (split by user type)
│       ├── normal_users.md
│       ├── researchers.md
│       ├── system_administrators.md
│       ├── facility_admins.md
│       └── system_designers.md
│
├── benchmarks/                    # Datasets and evaluation for benchmarking agents
│   ├── benchmark_overview.md
│   ├── oda_agent_benchmark.md
│   └── hpc_query_benchmark_set.md
│
├── scripts/                       # (Optional) Python/Notebook tools for generation or parsing
│   ├── generate_taxonomy.py
│   ├── merge_queries.py
│   └── evaluate_benchmark.ipynb
│
└── assets/                        # Figures, diagrams, or charts for README/docs
    ├── exabench_structure.png
    └── taxonomy_map.png
```
