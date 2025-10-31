

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
