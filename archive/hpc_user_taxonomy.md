# 🏗️ HPC & Monitoring System User Taxonomy

This document defines a **complete taxonomy of all user types** that interact with an **HPC system** and its **monitoring ecosystem** (IT + facility).  
It includes scientific users, operations teams, facility managers, researchers, and emerging AI-driven agents — suitable for use in RAG models, chat systems, or knowledge graphs such as **ExaAgent**.

---

## 🧑‍🔬 1. Scientific & Application Users

| **Sub-Role** | **Description / Objectives** | **Typical Data / Tools Used** | **Example Queries** |
|---------------|------------------------------|-------------------------------|---------------------|
| **Normal HPC Users (Scientists / Engineers)** | Submit and monitor jobs, manage data, use pre-installed scientific software. | SLURM/PBS, job logs, project storage, modules, Singularity containers. | “Why did my job fail?”<br>“How to request more GPU nodes?” |
| **HPC Researchers (Performance, Energy, Anomaly Studies)** | Analyze performance and energy efficiency; perform anomaly detection and long-term monitoring studies; estimate power from job scripts; optimize workloads and scheduling. | Monitoring DBs, Prometheus, InfluxDB, Kepler, logs, SLURM traces, facility data, DVC datasets. | “Detect anomalies in 3-year power data.”<br>“Estimate energy of this batch script.” |
| **Data Scientists / AI Researchers on HPC** | Use HPC for ML/AI workloads; study scalability and data handling; integrate with model registries. | PyTorch, TensorFlow, MLflow, DVC, JupyterHub. | “Train transformer model on GPU nodes.” |
| **Computational Domain Scientists** | Domain-specific workloads (CFD, MD, weather, etc.) using tuned software. | OpenFOAM, GROMACS, VASP, WRF, LAMMPS. | “How to enable OpenMP in VASP job?” |
| **Industrial / Enterprise Users** | External customers accessing HPC through portals or APIs. | Web portals, REST APIs, workflow managers. | “Submit workflow through API.” |

---

## 🧰 2. Infrastructure & Operations Users

| **Sub-Role** | **Description / Objectives** | **Typical Data / Tools Used** | **Example Queries** |
|---------------|------------------------------|-------------------------------|---------------------|
| **System Administrators (SysAdmins / DevOps)** | Maintain OS, scheduler, user accounts, and reliability of nodes. | Linux, SLURM, Prometheus, Ansible, Helm, Kubernetes, logs. | “Why is node n45 offline?” |
| **Monitoring Engineers / Observability Specialists** | Manage metric collection, alerting, and dashboarding. | Prometheus, Grafana, Loki, Alertmanager, Kepler. | “CPU utilization trend per partition.” |
| **Storage Administrators** | Manage parallel file systems and backups. | Lustre, BeeGFS, Ceph, GPFS, object storage telemetry. | “Check Lustre throughput anomalies.” |
| **Network Administrators** | Monitor and maintain interconnects. | SNMP, Infiniband, Slingshot, Grafana dashboards. | “Latency statistics for fabric ports.” |
| **Security Officers / IAM Managers** | Oversee authentication, RBAC, and compliance. | Keycloak, LDAP, IAM logs, audit trails. | “List failed login attempts.” |
| **Support Engineers / Helpdesk Staff** | Resolve user issues, collect logs, maintain FAQs. | Ticketing systems, job reports. | “User job exceeded time limit.” |
| **Software Stack Maintainers** | Build and containerize HPC toolchains. | Spack, EasyBuild, CI/CD pipelines. | “Rebuild GCC 13 toolchain with CUDA.” |

---

## 🏭 3. Facility & Hardware Operations Users

| **Sub-Role** | **Description / Objectives** | **Typical Data / Tools Used** | **Example Queries** |
|---------------|------------------------------|-------------------------------|---------------------|
| **Facility Administrators / Technicians** | Manage racks, cooling, power, sensors, and safety. | IPMI, Redfish, BMS/DCIM, Modbus, SNMP. | “Report temperature map per rack.” |
| **Energy Managers / Sustainability Analysts** | Analyze PUE, energy efficiency, and sustainability. | Power meters, facility telemetry, PUE logs. | “Compute PUE for past quarter.” |
| **Hardware Engineers / Maintenance Staff** | Diagnose and replace faulty components. | IPMI logs, service tickets. | “Which nodes reported fan failure?” |
| **Procurement & Vendor Liaisons** | Manage warranties and evaluate new hardware. | RFPs, inventory DBs. | “Track warranty status for GPU nodes.” |

---

## 🧱 4. Architecture, Design & Strategic Planning Users

| **Sub-Role** | **Description / Objectives** | **Typical Data / Tools Used** | **Example Queries** |
|---------------|------------------------------|-------------------------------|---------------------|
| **HPC System Architects / Designers** | Design and size new clusters; define topology and storage. | RFPs, simulation models, benchmark data. | “Evaluate AMD vs Intel node cost/TFlop.” |
| **Capacity Planners** | Forecast usage, hardware refreshes, and expansion needs. | Historical metrics, queue statistics. | “Predict CPU core demand in 2026.” |
| **Performance Modelers** | Build performance and cost trade-off models. | Telemetry archives, simulators. | “Simulate scalability for 1k-node workload.” |
| **Policy & Project Managers** | Plan budgets, define priorities, align R&D goals. | KPI dashboards, utilization reports. | “Monthly utilization summary by project.” |

---

## 📊 5. Data Analytics & Observability Researchers (Cross-Layer)

| **Sub-Role** | **Description / Objectives** | **Typical Data / Tools Used** | **Example Queries** |
|---------------|------------------------------|-------------------------------|---------------------|
| **Operational Data Scientists** | Analyze long-term telemetry for optimization and sustainability. | SQL, Pandas, PySpark, parquet datasets. | “Correlate cooling power and CPU load.” |
| **Anomaly Detection Researchers** | Use AI/ML to detect abnormal thermal/power/network patterns. | Kepler, ThermADNet, HazardNet, Grafana alerts. | “Find nodes with thermal drift.” |
| **Digital Twin Developers** | Create virtual replicas of HPC behavior for predictive control. | InfluxDB, ML models, simulation tools. | “Train digital twin on 2022-2025 telemetry.” |
| **AIOps / MLOps Engineers** | Build autonomous pipelines for anomaly detection and optimization. | MLflow, DVC, FastAPI, LangGraph, Prometheus APIs. | “Deploy model to optimize node power caps.” |

---

## 🧩 6. Management, Policy, and External Stakeholders

| **Sub-Role** | **Description / Objectives** | **Typical Data / Tools Used** | **Example Queries** |
|---------------|------------------------------|-------------------------------|---------------------|
| **Center Directors / Project PIs** | Oversee operations, KPIs, and collaborations. | KPI dashboards, energy reports. | “Show overall energy savings since 2023.” |
| **Funding Agencies / Auditors** | Evaluate efficiency, utilization, and sustainability. | Reports, compliance datasets. | “Generate annual energy audit report.” |
| **External Collaborators (EU Partners / Vendors)** | Access shared telemetry or datasets for research. | Shared dashboards, APIs, data exports. | “Request metrics subset for WP3 analysis.” |

---

## 🤖 7. Automation & Agentic Components (Emerging Virtual Users)

In AIOps-enabled HPC frameworks (e.g., **ExaAgent**, **KubeIntellect**), automated agents act as *virtual users* interacting with monitoring and control layers.

| **Agent Type** | **Purpose / Function** | **Interacts With** |
|----------------|------------------------|--------------------|
| **Monitoring Agent (ExaSage / Kepler)** | Collects metrics and logs across nodes and facilities. | Prometheus, IPMI, InfluxDB. |
| **Anomaly Detection Agent (ThermADNet / HazardNet)** | Detects and explains abnormal system behavior. | Telemetry DBs, alert systems. |
| **AI Scheduler Agent** | Dynamically optimizes job scheduling and resource allocation. | SLURM APIs, Prometheus metrics. |
| **Chat / RAG Agent (User Assistant)** | Provides conversational access to data, documentation, and monitoring systems. | Vector DB, documentation corpus, APIs. |

---

## 🌐 8. Hierarchical Summary (Mind-Map)

```plaintext
HPC & Monitoring Users
├── Scientific Users
│ ├── Normal Users
│ ├── HPC Researchers
│ ├── AI/ML Researchers
│ ├── Domain Scientists
│ └── Industrial Users
├── Infrastructure & Operations
│ ├── SysAdmins
│ ├── Monitoring Engineers
│ ├── Storage / Network Admins
│ ├── Security Officers
│ └── Support Staff
├── Facility & Hardware
│ ├── Facility Technicians
│ ├── Energy Managers
│ ├── Hardware Engineers
│ └── Vendors / Procurement
├── Architecture & Planning
│ ├── System Architects
│ ├── Capacity Planners
│ ├── Policy Managers
│ └── Project Directors
├── Data Analytics & Research
│ ├── Operational Data Scientists
│ ├── Anomaly Detection Researchers
│ ├── Digital Twin Developers
│ └── AIOps Engineers
├── Management & External
│ ├── Center Directors
│ ├── Funding Agencies
│ └── External Collaborators
└── Automation Agents
├── Monitoring Agent
├── Anomaly Detection Agent
├── AI Scheduler Agent
└── Chat / RAG Agent
```


---

## 🧩 Notes for RAG / Chat Integration

- Each **user type** can be mapped to:
  - `knowledge_domains` → what they need (e.g., “energy telemetry”, “scheduler logs”)
  - `query_categories` → what they ask (e.g., “why job failed?”, “detect anomalies?”)
  - `data_sources` → where data is located (Prometheus, IPMI, InfluxDB)
- This structure can directly populate:
  - ExaAgent persona registry (`personas.yaml`)
  - Query category table for the HPC chat system (`query_taxonomy.csv`)

---

**File:** `hpc_user_taxonomy.md`  
**Version:** 1.0 — October 2025  
**Maintainer:** _ExaAgent Team_

---
