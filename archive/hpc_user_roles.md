


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
