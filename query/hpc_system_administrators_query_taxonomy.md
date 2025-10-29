# 🧠 HPC User Query Taxonomy  
## User Type: **System Administrators**

---

## 1️⃣ Category List (High-Level Overview)

1. Cluster Resource Management (H)
2. User & Access Management (H)
3. Job Scheduling & Queue Control (H)
4. Monitoring & Health Status (H)
5. Performance & Utilization Analysis (H)
6. Storage & Filesystem Management (H)
7. Network & Interconnect Diagnostics (M)
8. Security & Compliance (H)
9. Software Environment & Modules (H)
10. Node Maintenance & Lifecycle (H)
11. Power & Thermal Management (M)
12. Facility & Infrastructure Awareness (M)
13. Backup & Disaster Recovery (L)
14. Automation & Scripting Assistance (H)
15. Logs, Alerts, and Troubleshooting (H)
16. Documentation & Admin Support (M)
17. Integration & API Management (L)
18. License and Quota Management (M)
19. AI/LLM Agent Configuration & Policy (L)
20. User Support & Incident Response (H)

---

## 2️⃣ Detailed Table Version

| Category | Description | Example Queries | Agent(s) to Fulfill Request |
|-----------|--------------|-----------------|-----------------------------|
| **Cluster Resource Management** | Manage compute, GPU, and storage resources across partitions or queues | “Show node allocation per partition.” / “Resize compute node pool.” / “Drain node n101.” / “Show available GPUs in queue gpu_long.” | HPC Job Executer, ExaSage Monitoring |
| **User & Access Management** | Control users, groups, SSH access, LDAP, and privileges | “Add user alice to group decice.” / “List inactive users.” / “Rotate SSH keys for all admins.” | Admin Agent, RAG (docs), Control |
| **Job Scheduling & Queue Control** | Monitor and control job queues, SLURM/PBS scheduler state | “Pause queue gpu_long.” / “Cancel all jobs from user test.” / “Reprioritize job 52432.” | Job Executer, ExaSage Monitoring |
| **Monitoring & Health Status** | Real-time node, GPU, network, and service health | “Show failed nodes in last 24h.” / “Check GPU utilization trends.” / “List nodes with ECC errors.” | ExaSage Monitoring Agent |
| **Performance & Utilization Analysis** | Aggregate metrics: CPU load, I/O, job efficiency | “Top 10 users by CPU usage.” / “Average MPI job efficiency this week.” / “Detect underutilized nodes.” | Data Analytics, Monitoring |
| **Storage & Filesystem Management** | Lustre, BeeGFS, Ceph, NFS operations and usage checks | “Show OST usage by project.” / “Check I/O throughput per user.” / “Mount new filesystem.” | Admin Agent, Monitoring |
| **Network & Interconnect Diagnostics** | InfiniBand/Fabric performance and errors | “Show latency per switch.” / “List ports with packet drops.” / “Monitor Mellanox counters.” | Facility Agent, Monitoring |
| **Security & Compliance** | Ensure proper configs, updates, and access policies | “Audit sudo access.” / “List failed login attempts.” / “Check CIS compliance.” | Admin Agent, RAG |
| **Software Environment & Modules** | Manage loaded modules, environments, containers | “List loaded modules for user bob.” / “Add new module OpenMPI 5.0.” / “Check Spack installation logs.” | RAG Agent, Control |
| **Node Maintenance & Lifecycle** | Provision, decommission, or reboot nodes | “Reboot node n102.” / “Mark node n108 as maintenance.” / “Check BIOS/IPMI firmware versions.” | Control, Facility Agent |
| **Power & Thermal Management** | Analyze rack/pod energy use and thermal maps | “Average rack power for R5.” / “Detect overheating nodes.” / “List top 5 high-energy jobs.” | Facility Agent, Monitoring |
| **Facility & Infrastructure Awareness** | Map system racks, cooling zones, power feeds | “Show spatial layout of racks in room A.” / “Which racks share PDU B4?” | Facility Agent |
| **Backup & Disaster Recovery** | Manage snapshots and restoration procedures | “Check backup status for /home.” / “Restore /projects/decice.” | Admin Agent |
| **Automation & Scripting Assistance** | Auto-generate shell or SLURM scripts | “Generate SLURM restart script for failed jobs.” / “Automate GPU utilization report.” | RAG + Code Agent |
| **Logs, Alerts, and Troubleshooting** | Query logs, system alerts, failed service states | “Show dmesg logs for node n107.” / “Which jobs failed due to OOM?” | ExaSage Monitoring, RAG |
| **Documentation & Admin Support** | Retrieve admin SOPs, wiki, or procedure docs | “How to reset a failed SLURM node?” / “Procedure to replace GPU.” | RAG Agent |
| **Integration & API Management** | Manage APIs, webhooks, Grafana/Prometheus links | “List all Prometheus targets.” / “Check API token validity.” | RAG Agent, Admin Agent |
| **License and Quota Management** | Monitor license usage and user quotas | “Check ANSYS license usage.” / “Set 10TB quota for project UC3.” | Control, Monitoring |
| **AI/LLM Agent Configuration & Policy** | Manage HPC AI assistant permissions | “Limit monitoring data to admins.” / “Review LLM privacy policies.” | Admin Agent |
| **User Support & Incident Response** | Track incidents, notify users, resolve issues | “List all open tickets.” / “Notify users about downtime.” | Admin Agent, RAG |

---

## 3️⃣ Permissions & Access Control Notes

| Level | Description | Relevant Categories |
|--------|--------------|---------------------|
| **Admin / Elevated** | Full system privileges needed | Resource Management, User Management, Node Maintenance, Security, Backup, Integration |
| **Operator / Limited** | Monitoring, diagnostics, read-only analytics | Monitoring, Performance Analysis, Facility Awareness |
| **User / General** | Access to documentation or read-only queries | Docs & Support, Scripting Help |
| **Security Cautions** | Agent responses involving config changes, SSH, LDAP, or job cancellation must route through **authenticated Admin Control Path** with audit logging |

---

## 4️⃣ Extended Example Questions Corpus (≥25)

1. “Which nodes are currently offline or drained?”
2. “Show me top 10 jobs by memory usage today.”
3. “What’s the GPU error rate trend on rack A2?”
4. “List users who haven’t logged in for 30 days.”
5. “Restart SLURM controller service.”
6. “Check job 54231 efficiency breakdown.”
7. “Update BIOS firmware on nodes n120–n125.”
8. “Which filesystem is 90% full?”
9. “Show network latency matrix for InfiniBand switches.”
10. “Monitor fan speed anomalies.”
11. “Who is using more than 5TB in /scratch?”
12. “List failed login attempts from unknown IPs.”
13. “Audit sudoers configuration.”
14. “Generate daily power consumption report.”
15. “What is causing the SLURM queue to be blocked?”
16. “Show historical CPU utilization for the past week.”
17. “Predict next cooling alert based on current rack temps.”
18. “Create an automated backup schedule for /projects.”
19. “Which node had kernel panic yesterday?”
20. “Compare CPU temperature of n107 and n108.”
21. “Show module dependencies for OpenFOAM.”
22. “Send system maintenance notice to all users.”
23. “Enable maintenance mode for GPU partition.”
24. “Detect thermal hotspots using IPMI sensor data.”
25. “Summarize performance anomalies from last night’s run.”

---

## 5️⃣ Priority Tags (Summary)

| Category | Priority |
|-----------|-----------|
| Cluster Resource Management | H |
| User & Access Management | H |
| Job Scheduling & Queue Control | H |
| Monitoring & Health Status | H |
| Performance & Utilization Analysis | H |
| Storage & Filesystem Management | H |
| Network & Interconnect Diagnostics | M |
| Security & Compliance | H |
| Software Environment & Modules | H |
| Node Maintenance & Lifecycle | H |
| Power & Thermal Management | M |
| Facility & Infrastructure Awareness | M |
| Backup & Disaster Recovery | L |
| Automation & Scripting Assistance | H |
| Logs, Alerts, and Troubleshooting | H |
| Documentation & Admin Support | M |
| Integration & API Management | L |
| License and Quota Management | M |
| AI/LLM Agent Configuration & Policy | L |
| User Support & Incident Response | H |

---
