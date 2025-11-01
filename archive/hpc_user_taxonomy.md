


---

## 🧠 HPC User Role Taxonomy (Comprehensive Overview)

Below is a **structured table** and a **detailed breakdown** for each role, describing:

1. **Primary Responsibilities / Tasks**
2. **Knowledge & Skill Areas (what they study or must understand)**
3. **Typical Data or Tools They Interact With**
4. **Key Query or Requirement Themes (for your RAG agent / chatbot use)**


| **Category / Role**                                                       | **Main Tasks & Responsibilities**                                                                                                                                                                                                            | **What They Study / Need to Know**                                                                                                                                                                                                       | **Tools / Data Interacted With**                                                                              | **Example Query Categories**                                                                                                                                                                             |
| ------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 🧑‍💻 **Normal HPC Users (Application Users / Scientists / Engineers)**   | - Submit and monitor jobs<br>- Manage input/output data<br>- Request compute/storage quotas<br>- Use preinstalled scientific software<br>- Debug failed jobs<br>- Optimize scripts for runtime efficiency                                    | - Linux shell, SLURM/Job schedulers<br>- Basic parallel computing concepts<br>- File systems (Lustre, GPFS)<br>- Module systems<br>- Data transfer (scp, rsync, Globus)                                                                  | Job scheduler logs, output/error files, user quota, environment modules, project directories                  | - “Why did my job fail?”<br>- “How to request more GPU nodes?”<br>- “Which queue has shortest wait?”<br>- “How to use Python with MPI?”                                                                  |
| 🧪 **HPC Researchers (Computational Scientists / Performance Analysts)**  | - Develop new algorithms or parallel applications<br>- Profile, benchmark, and optimize applications<br>- Analyze performance and scalability<br>- Study power/energy efficiency<br>- Publish results                                        | - Advanced HPC programming (MPI, OpenMP, CUDA)<br>- Performance modeling (Roofline, scaling laws)<br>- Data analysis & profiling tools<br>- Energy efficiency & scheduling<br>- ML/AI for performance prediction                         | Profiling data (Perf, VTune, Arm MAP), benchmark results, telemetry (CPU/GPU metrics), cluster configurations | - “Which configuration gives best energy-performance tradeoff?”<br>- “How to interpret MPI imbalance metrics?”<br>- “Compare performance across nodes.”<br>- “How to integrate Kepler power metrics?”    |
| 🧰 **System Administrators (SysAdmins / DevOps)**                         | - Install, configure, and maintain cluster OS and middleware<br>- Manage user accounts and security<br>- Monitor resource utilization and job queues<br>- Patch and upgrade software<br>- Troubleshoot system failures                       | - Linux administration, network security<br>- Scheduler configuration (SLURM, PBS)<br>- Containerization (Singularity, Podman)<br>- Automation (Ansible, Terraform, Helm)<br>- Logging & observability stacks (Prometheus, Grafana, ELK) | System logs, node health data, configuration files, container images, CI/CD pipelines                         | - “Why is node n45 offline?”<br>- “Update CUDA driver on GPU partition.”<br>- “Set fair-share limits for projects.”<br>- “Check SLURM daemon health.”                                                    |
| 🏭 **Facility Admin / Technicians (Datacenter Ops / Facility Engineers)** | - Maintain physical infrastructure: racks, cooling, power, networking<br>- Monitor environmental parameters (temperature, humidity)<br>- Respond to hardware alarms<br>- Coordinate maintenance windows<br>- Support sustainability goals    | - Electrical and mechanical systems<br>- BMS / DCIM systems<br>- IPMI, Redfish, SNMP monitoring<br>- Energy management and PUE<br>- Safety and compliance standards                                                                      | IPMI sensor data, BMS telemetry, facility dashboards, maintenance schedules                                   | - “Which racks show thermal anomalies?”<br>- “Current PUE trend for datacenter?”<br>- “Alarm history for CRAC unit 3.”<br>- “Cooling efficiency comparison between zones.”                               |
| 🧱 **HPC System Designers / Architects**                                  | - Design new clusters and storage systems<br>- Plan hardware and software architecture<br>- Evaluate technology options (CPU/GPU/Network)<br>- Define scalability and redundancy strategies<br>- Collaborate with vendors and research teams | - HPC architecture principles<br>- Network topology (Infiniband, Slingshot)<br>- Storage architecture (Lustre, BeeGFS)<br>- Power & cooling design<br>- Cost-performance modeling<br>- Benchmarking methodologies                        | System specs, RFPs, design models, simulation results, capacity planning data                                 | - “What is the optimal node design for AI + CFD?”<br>- “Compare cost of AMD vs Intel nodes per TFLOP.”<br>- “Estimate cooling load for 1 MW rack density.”<br>- “Evaluate interconnect latency impacts.” |

---

## 🔍 Deep Dive by Role

### 1. **Normal HPC Users**

* **Main Studies**:

  * Linux basics, shell scripting
  * Batch scheduling systems (SLURM, PBS, LSF)
  * Data management, file systems
  * Basic parallel execution (MPI runs, OpenMP threads)
* **Key Learning Topics**: job efficiency, resource requests, error diagnostics
* **Focus of Queries**: usability, quick help, job debugging, module usage

---

### 2. **HPC Researchers**

* **Main Studies**:

  * HPC programming models (MPI, OpenMP, CUDA, SYCL)
  * Profiling & performance analysis (TAU, Score-P, HPCToolkit)
  * Energy efficiency research (Kepler, RAPL, PowerAPI)
  * AI/ML-based performance modeling
  * Parallel algorithms & scalability theory
* **Focus of Queries**: optimization, reproducibility, automation, energy modeling

---

### 3. **System Administrators**

* **Main Studies**:

  * Cluster provisioning & automation (Ansible, Terraform, Helm)
  * Security (RBAC, LDAP, key management)
  * Logging, monitoring & observability (Prometheus, Grafana, Loki)
  * Scheduler management (SLURM config tuning)
  * Networking (IPMI, VLANs, InfiniBand)
* **Focus of Queries**: system health, deployment, upgrades, troubleshooting

---

### 4. **Facility Admin / Technicians**

* **Main Studies**:

  * Electrical power systems, UPS, PDU design
  * Cooling technologies (air/water, liquid immersion)
  * Environmental monitoring (IPMI, Modbus, SNMP)
  * Facility management software (BMS, DCIM)
  * Maintenance procedures, alarm systems
* **Focus of Queries**: environmental health, energy efficiency, maintenance logs

---

### 5. **HPC System Designers / Architects**

* **Main Studies**:

  * Cluster design methodologies
  * Hardware selection, cost modeling, procurement
  * Scalability simulations and workload characterization
  * System software stack planning (OS, scheduler, middleware)
  * Future tech trends (RISC-V, CXL, liquid cooling)
* **Focus of Queries**: architecture tradeoffs, design simulation, cost/performance analysis

---

## 💡 Optional Add-on Categories (for completeness)

You could later extend taxonomy to include:

* **HPC Software Developers** (library/tool maintainers)
* **Data Scientists** using HPC-as-a-Service
* **Energy Managers** (cross between facility + sustainability)
* **AI/LLM Orchestrators** (future autonomous HPC optimization agents)


Excellent point — you’re absolutely right ✅

Modern **HPC Researchers** (especially in Exascale-era systems and EU projects like DECICE/SEANERGYS) are not only doing *application-level* performance research, but also **operational data analytics**, **anomaly detection**, and **energy optimization** using full-stack telemetry.

Let’s update and **expand** the “HPC Researchers” category to fully reflect that — integrating your additions into a structured breakdown suitable for taxonomy, RAG categories, and documentation.

---

## 🧪 HPC Researchers (Updated & Complete)

| **Aspect**                                      | **Description**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| ----------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Primary Mission**                             | Bridge scientific computing with data-driven optimization — analyze, model, and improve performance, energy efficiency, reliability, and sustainability across the entire HPC system stack.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **Core Tasks & Responsibilities**               | - Develop new parallel algorithms or machine learning models for HPC workloads.<br>- **Perform anomaly detection** on multi-year cluster monitoring datasets (thermal, power, performance, logs).<br>- Analyze **system logs, scheduler traces, and job metadata** to identify performance bottlenecks and failure patterns.<br>- Conduct **power consumption estimation** from job scripts and runtime telemetry (batch script → estimated Joules).<br>- Study **long-term facility & IT data** (cooling, temperature, power, humidity) to model correlations between compute load and energy usage.<br>- Perform **operational data analysis** for optimization and sustainability studies.<br>- Benchmark and profile scientific applications across architectures (CPU/GPU/FPGA).<br>- Develop predictive and prescriptive models for resource utilization, reliability, and cooling efficiency.<br>- Publish research results and propose novel HPC scheduling/energy-aware algorithms. |
| **Key Studies / Knowledge Areas**               | - **HPC performance engineering** (MPI, OpenMP, CUDA, SYCL)<br>- **Anomaly detection & time-series analysis** (ML/DL for logs & telemetry)<br>- **Operational data analytics** (Grafana/Prometheus data export, PostgreSQL, InfluxDB, parquet data)<br>- **Energy modeling & prediction** (Kepler, RAPL, PowerAPI, pod-level prediction models)<br>- **Cooling systems & facility telemetry interpretation** (BMS/DCIM data integration)<br>- **Data wrangling and visualization** (Pandas, PySpark, DVC, MLflow)<br>- **Scientific reproducibility** (experiment tracking, model versioning, FAIR datasets)<br>- **HPC workload characterization** (job patterns, resource usage clusters, performance variability)                                                                                                                                                                                                                                                                         |
| **Data Sources They Analyze**                   | - **Monitoring data:** node-level metrics (CPU/GPU utilization, power, temperature, fan speed)<br>- **Logs:** job scheduler logs, syslogs, application logs<br>- **Batch scripts:** SLURM/PBS job submission scripts (for workload classification & power estimation)<br>- **Databases:** Prometheus, PostgreSQL, InfluxDB, parquet archives<br>- **Facility telemetry:** PUE, cooling power, rack temperature distributions                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **Tools & Frameworks**                          | - HPC profiling tools (HPCToolkit, TAU, Score-P, VTune)<br>- Data analytics frameworks (Pandas, Dask, PySpark, SQL)<br>- Visualization (Grafana, Plotly, Matplotlib)<br>- ML/DL frameworks (Scikit-Learn, PyTorch, TensorFlow)<br>- Energy monitoring (Kepler, RAPL, IPMI)<br>- Cluster telemetry ingestion (Prometheus, ExaData, InfluxDB)<br>- Reproducibility stacks (MLflow, DVC, GitLab CI/CD)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Research Themes / Study Topics**              | - System-wide **anomaly detection** (thermal, power, network)<br>- **Predictive maintenance** from multi-year logs<br>- **Energy-aware job scheduling and node management**<br>- **Workload characterization** and job class detection<br>- **Cross-correlation of IT + facility data** (server vs cooling)<br>- **Data-driven optimization of cooling & compute efficiency**<br>- **Multi-modal telemetry fusion** (metrics + logs + job scripts)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| **Example Queries for Chat Agent / RAG System** | - “Detect anomalies in node power consumption over the last 3 years.”<br>- “Estimate power cost of this batch script.”<br>- “Which jobs caused thermal stress in 2023?”<br>- “Correlate cooling energy and compute load during summer 2024.”<br>- “Show temporal drift in node utilization distribution.”<br>- “Generate feature dataset for model training from Prometheus + SLURM logs.”                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |

---

### 🧩 Integration Note (for your overall table)

This version should **replace** or **expand** the HPC Researcher section in your previous taxonomy table.

If you like, I can merge this updated version back into the **full 5-role Markdown table (`hpc_user_roles_full.md`)** with this expanded research role, including explicit sub-categories such as:

* *Performance Researchers*
* *Energy & Anomaly Researchers*
* *Facility Data Scientists*

Would you like me to regenerate the full Markdown file including this enhanced HPC Researcher section?



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


---

## 3) Core Role Cards (compact)

Each card: **Responsibilities • Skills • Data/Tools • QCAT • Example queries**

### 3.1 Normal HPC Users (Scientists/Engineers)

* **Responsibilities**: Submit/monitor jobs, manage data, use preinstalled software, basic debugging, request quotas.
* **Skills**: Linux shell; schedulers (SLURM/PBS); modules; basic MPI/OpenMP; file systems; data transfer.
* **Data/Tools**: Job logs, stdout/err, project storage, environment modules; Singularity/Apptainer.
* **QCAT**: `JOB, SUP, DOCS, STOR, OBS`
* **Examples**: “Why did my job fail?” • “Which queue has the shortest wait?” • “How to use Python with MPI?”

### 3.2 HPC Researchers (Performance/Energy/Anomaly)

* **Responsibilities**: Profile/benchmark; optimize performance; study energy; anomaly detection on multi‑year telemetry; power estimation from batch scripts; reproducible studies.
* **Skills**: MPI/OpenMP/CUDA/SYCL; HPCToolkit/TAU/VTune; Pandas/Dask/SQL; ML (Scikit‑learn/PyTorch); Kepler/RAPL; FAIR/MLflow/DVC.
* **Data/Tools**: Prometheus/InfluxDB; SLURM traces; logs; facility telemetry (PUE/cooling); parquet archives.
* **QCAT**: `PERF, ENERGY, AIOPS, OBS, CAP, DOCS`
* **Examples**: “Detect thermal anomalies in 2024 racks” • “Estimate job energy from this batch script” • “Compare configurations for best energy‑performance”.

### 3.3 System Administrators (SysAdmins/DevOps)

* **Responsibilities**: OS & middleware; scheduler config; upgrades/patching; user management; troubleshooting.
* **Skills**: Linux/Networking; SLURM/PBS; automation (Ansible/Helm/Terraform); containers; observability stacks.
* **Data/Tools**: Logs, node health, configs, images, CI/CD.
* **QCAT**: `OBS, SEC, JOB, STOR, NET, SUP`
* **Examples**: “Why is node n45 drained?” • “Update CUDA driver for GPU partition” • “Fair‑share limits for project X”.

### 3.4 Facility Admin / Technicians (Datacenter Ops)

* **Responsibilities**: Racks/power/cooling/networking; environmental monitoring; alarms; maintenance; sustainability.
* **Skills**: Electrical/mechanical; BMS/DCIM; IPMI/Redfish/SNMP/Modbus; safety/compliance.
* **Data/Tools**: IPMI sensors; BMS telemetry; maintenance schedules.
* **QCAT**: `FAC, ENERGY, CAP, OBS`
* **Examples**: “Which racks show thermal anomalies?” • “PUE trend this quarter” • “Alarm history for CRAC‑3”.

### 3.5 HPC System Designers / Architects

* **Responsibilities**: Plan HW/SW architecture; evaluate CPU/GPU/network/storage; cost‑performance; resilience; vendor liaison.
* **Skills**: Topologies (IB/Slingshot); storage design; cooling/power sizing; cost/perf modeling; benchmarks.
* **Data/Tools**: RFPs/specs; simulation models; benchmark results; capacity data.
* **QCAT**: `ARCH, CAP, ENERGY, NET, STOR, DOCS`
* **Examples**: “AMD vs Intel cost per TFLOP” • “Cooling load estimate for 1 MW rack density” • “Latency impact of topology X”.

---

## 4) Extended Roles (optional but useful)

* **Monitoring Engineers / Observability** → `OBS, AIOPS`
* **Storage Admins** → `STOR, OBS`
* **Network Admins** → `NET, OBS`
* **Security/IAM Officers** → `SEC, OBS`
* **Support/Helpdesk** → `SUP, DOCS, JOB`
* **Data Scientists on HPC** → `JOB, PERF, STOR, DOCS`
* **Energy Managers** → `ENERGY, FAC, CAP`
* **Project/Center Managers, PIs** → `CAP, DOCS, ENERGY`
* **Vendors/Procurement** → `ARCH, CAP`
* **Automation/Agentic Components (virtual users)** → `AIOPS, OBS, ENERGY`

---

## 5) Role × Category Matrix (routing)

> ✅ = frequent • ◇ = occasional • – = rarely/never

| Role ↓ / QCAT → | JOB | PERF | ENERGY | OBS | STOR | NET | SEC | FAC | CAP | ARCH | SUP | AIOPS | DOCS |
| --------------- | :-: | :--: | :----: | :-: | :--: | :-: | :-: | :-: | :-: | :--: | :-: | :---: | :--: |
| Normal Users    |  ✅  |   ◇  |    ◇   |  ✅  |   ◇  |  –  |  –  |  –  |  –  |   –  |  ✅  |   –   |   ✅  |
| HPC Researchers |  ◇  |   ✅  |    ✅   |  ✅  |   ◇  |  ◇  |  –  |  ◇  |  ✅  |   ◇  |  –  |   ✅   |   ✅  |
| SysAdmins       |  ✅  |   ◇  |    ◇   |  ✅  |   ✅  |  ✅  |  ✅  |  –  |  ◇  |   –  |  ✅  |   ◇   |   ✅  |
| Facility Admins |  –  |   –  |    ✅   |  ✅  |   –  |  ◇  |  –  |  ✅  |  ✅  |   –  |  –  |   ◇   |   ✅  |
| Architects      |  –  |   ◇  |    ✅   |  ◇  |   ✅  |  ✅  |  –  |  ✅  |  ✅  |   ✅  |  –  |   ◇   |   ✅  |

---

## 6) Persona Schema & Export Snippets

Use these snippets to seed configs.

### 6.1 YAML Persona (example: HPC Researchers)

```yaml
id: hpc_researcher
role: HPC Researchers
qcat: [PERF, ENERGY, AIOPS, OBS, CAP, DOCS]
responsibilities:
  - Benchmark, profile, and optimize applications
  - Anomaly detection on multi-year telemetry
  - Energy modeling and job-level power estimation
skills: [MPI, OpenMP, CUDA, SYCL, HPCToolkit, TAU, VTune, Pandas, SQL, MLflow, Kepler]
data_sources: [Prometheus, InfluxDB, SLURM-traces, Logs, FacilityTelemetry]
tools: [HPCToolkit, TAU, VTune, Grafana, MLflow, DVC]
example_queries:
  - Detect thermal anomalies in racks during Aug 2024
  - Estimate energy of this SLURM batch script
  - Compare configurations for best energy-performance
```

### 6.2 CSV Export (sample rows)

```csv
id,role,qcat,responsibilities,skills,data_sources,tools,examples
hpc_user,Normal HPC Users,"JOB|SUP|DOCS|STOR|OBS","Submit jobs; debug failures; manage data","Linux; SLURM; Modules","JobLogs; ProjectStorage","Apptainer; rsync","Why did my job fail?"
hpc_researcher,HPC Researchers,"PERF|ENERGY|AIOPS|OBS|CAP|DOCS","Profile & optimize; anomaly detection; energy modeling","MPI; CUDA; TAU; Pandas; Kepler","Prometheus; SLURM; FacilityTelemetry","HPCToolkit; Grafana; MLflow","Estimate energy of this batch script"
```

---

## 7) Example Queries by Category (grab‑bag)

* **JOB**: Why pending? • Which queue shortest wait? • Increase GPU quota?
* **PERF**: MPI imbalance hotspots? • Roofline vs measured GFLOP/s • Node-to-node variability
* **ENERGY**: Node power cap at 250W? • PUE this month • Job J energy min/max/avg
* **OBS**: Top N nodes by CPU throttling • Alert history for exporter X • Dashboard link for partition Y
* **STOR**: Lustre OST with highest latency • Project Z quota • BeeGFS throughput anomaly
* **NET**: Fabric port errors • IB latency map • Oversubscription hotspots
* **SEC**: Failed logins by user • RBAC diff for group A • Expired tokens
* **FAC**: Rack R thermal map • CRAC-3 alarm history • Cooling efficiency by zone
* **CAP**: Predict 2026 GPU-hours • Utilization by project (monthly) • Headroom for new AI cluster
* **ARCH**: AMD vs Intel $/TFLOP • CXL benefits for workload W • Optimal topology for mixed AI+CFD
* **SUP**: Turn stdout/err into ticket • FAQ for OpenMP threads • Best practice for conda vs modules
* **AIOPS**: Train anomaly detector on 2022–2025 data • Autotune power caps • Explainable alert for power drift
* **DOCS**: Module usage for VASP • Policy for scratch purge • How to publish datasets FAIR

---

## 8) Governance & Guardrails

* Map QCAT → **allowed backends** (e.g., JOB can query SLURM but not BMS control APIs).
* Attach **PII/secret** handling to SEC/DOCS routes.
* Keep **facility control actions** behind approvals; read‑only by default for FAC.

---

## 9) Change Log

* **v1**: Unified compact roles + global QCAT + routing matrix + export snippets.
