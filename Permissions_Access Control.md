## Permissions & Access Control

| Category | Access Level | Notes |
|-----------|---------------|-------|
| Job Submission, Monitoring, Profiling | **User-level** | Allowed for authenticated HPC users. |
| Resource Discovery | **User-level** | Can expose aggregated, non-sensitive info. |
| Data Management | **User-level** (home/project dirs) | Access limited to owned/group directories. |
| Software Installations | **Elevated** | Admin approval required for cluster-wide packages. |
| Facility / Power Awareness | **Restricted** | Aggregated, anonymized data view only for researchers. |
| Security & Access | **Sensitive** | Must route through secure admin-only agent. |


## **Permissions & Access Control Notes**

| Category | Access Level | Notes |
|-----------|---------------|-------|
| Job Submission, Monitoring, Profiling | **User-level** | Allowed for authenticated HPC users. |
| Resource Discovery | **User-level** | Can expose aggregated, non-sensitive info. |
| Data Management | **User-level** (home/project dirs) | Access limited to owned/group directories. |
| Software Installations | **Elevated** | Admin approval required for cluster-wide packages. |
| Facility / Power Awareness | **Restricted** | Aggregated, anonymized data view only for researchers. |
| Security & Access | **Sensitive** | Must route through secure admin-only agent. |

| Category | Access Level | Security Notes |
|-----------|---------------|----------------|
| Job Submission, Queue, Data, Modules | **User-level** | Standard HPC user permissions. |
| Debugging & Logs | **User-level** | Access only to own jobs. |
| Storage, GPU Requests | **User-level with limits** | Quota-controlled. |
| Collaboration, Security Mgmt | **Privileged / Admin-assisted** | Needs project-level or sysadmin privileges. |
| Facility & Energy Awareness | **Read-only (restricted)** | Some data may be anonymized or aggregated. |

| Access Level | Applies To | Notes |
|---------------|-------------|-------|
| **Public/User-Level** | RAG queries, simulation, performance modeling, documentation | Safe to expose; no sensitive data |
| **Privileged (Architect/Admin)** | Real telemetry data (power, temperature, node stats), network config, security models | Requires architect/admin role; restrict ExaSage + Facility access |
| **Highly Sensitive** | Procurement, security, and access-control design | Use isolated RAG + approval gating |
| **Read-Only Mode** | Monitoring and topology visualization | Default safe mode for architects without write privileges |