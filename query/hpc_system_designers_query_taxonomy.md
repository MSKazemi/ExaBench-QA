# 🧠 HPC User Type: **HPC System Designers / Architects**

## 1️⃣ Category List (High-Level Overview)

| # | Category | Priority |
|---|-----------|-----------|
| 1 | System Architecture Design & Topology Planning | H |
| 2 | Hardware Configuration & Sizing | H |
| 3 | Network & Interconnect Design | H |
| 4 | Energy Efficiency & Thermal Modeling | H |
| 5 | Storage & I/O Subsystem Design | H |
| 6 | Facility & Environmental Integration | M |
| 7 | Software Stack Architecture (OS, schedulers, libraries) | H |
| 8 | Performance Modeling & Simulation | H |
| 9 | Reliability, Availability, Maintainability (RAM) & Resilience | M |
| 10 | Monitoring Framework Design (Telemetry & Sensors) | H |
| 11 | Security, Access Control & Multi-Tenancy | M |
| 12 | Benchmarking, Validation & Scalability Testing | H |
| 13 | Cost Modeling & Procurement Optimization | M |
| 14 | Sustainability & Lifecycle Management | L |
| 15 | Documentation, Standards & Best Practices | M |

---

## 2️⃣ Detailed Table Version

| Category | Description | Example Queries | Agent(s) to Fulfill Request |
|-----------|--------------|----------------|-----------------------------|
| **System Architecture Design & Topology Planning** | Define compute node layout, rack grouping, interconnect hierarchy, and node composition. | “What’s the optimal ratio of GPU to CPU nodes for mixed workloads?” • “How many racks do I need for 1000 dual-socket nodes?” • “Show me a visualization of the current logical topology.” | RAG Agent, ExaSage Monitoring, Data Analytics |
| **Hardware Configuration & Sizing** | Select CPU/GPU models, memory size, accelerators, and interconnect cards based on workloads. | “Compare AMD EPYC vs Intel Sapphire Rapids for CFD workloads.” • “Estimate performance per watt for different GPU models.” | RAG Agent, Data Analytics Agent |
| **Network & Interconnect Design** | Model and optimize fabric topology (InfiniBand, Ethernet, NVLink). | “Simulate bisection bandwidth for a fat-tree topology.” • “What’s the expected latency between racks?” | RAG, Monitoring, Simulation Agent |
| **Energy Efficiency & Thermal Modeling** | Study energy usage, cooling efficiency, and power delivery. | “Show energy efficiency curves under 80% load.” • “Predict thermal hotspots using IPMI + facility data.” | ExaSage Monitoring, Facility Agent, Data Analytics |
| **Storage & I/O Subsystem Design** | Design parallel storage systems (Lustre, BeeGFS, Ceph) and I/O topology. | “Which configuration yields the best I/O throughput for 5 PB of scratch storage?” • “Compare NVMe vs HDD for cost per TB.” | RAG Agent, Data Analytics |
| **Facility & Environmental Integration** | Map compute layout to physical space, cooling zones, and power distribution. | “How should I distribute racks to balance cooling zones?” • “Show current rack power density map.” | Facility Agent, ExaSage Monitoring |
| **Software Stack Architecture** | Design OS images, compilers, middleware, and scheduler configuration. | “Recommend kernel parameters for high-frequency trading workloads.” • “Compare SLURM vs PBS for heterogeneous cluster scheduling.” | RAG, HPC Job Executor |
| **Performance Modeling & Simulation** | Predict performance metrics using benchmarks or models. | “Estimate LINPACK performance for 500 nodes.” • “Run a scalability simulation for AI workloads.” | Data Analytics Agent, Simulation Agent |
| **Reliability, Availability, Maintainability (RAM) & Resilience** | Model fault tolerance, MTBF, and redundancy. | “What’s the expected downtime per year?” • “Which nodes have highest failure rate trend?” | Monitoring Agent, Analytics |
| **Monitoring Framework Design** | Define telemetry granularity, metrics collection, and alerting. | “Which sensors should be monitored via IPMI?” • “Recommend metrics for GPU thermal anomalies.” | ExaSage Monitoring, RAG |
| **Security, Access Control & Multi-Tenancy** | Define authentication, role policies, and network isolation. | “How to isolate network for different research groups?” • “Recommend RBAC model for shared infrastructure.” | RAG Agent, Admin Control Agent |
| **Benchmarking, Validation & Scalability Testing** | Design benchmark suites and validation protocols. | “Run STREAM and report memory bandwidth per node.” • “Compare scaling of AI vs CFD codes.” | HPC Job Executor, Analytics |
| **Cost Modeling & Procurement Optimization** | Estimate CAPEX/OPEX, procurement trade-offs. | “What’s cost per TFLOP for this configuration?” • “Generate TCO comparison between vendors.” | Data Analytics Agent |
| **Sustainability & Lifecycle Management** | Manage decommissioning, recycling, and upgrade paths. | “When should we plan the next hardware refresh?” • “Estimate CO₂ footprint per node.” | Facility Agent, Data Analytics |
| **Documentation, Standards & Best Practices** | Maintain architectural documentation and compliance with standards. | “Show ISO/IEC guidelines relevant to HPC datacenter design.” • “Generate architecture report for funding proposal.” | RAG Agent |

---

## 3️⃣ Permissions & Access Control Notes

| Access Level | Applies To | Notes |
|---------------|-------------|-------|
| **Public/User-Level** | RAG queries, simulation, performance modeling, documentation | Safe to expose; no sensitive data |
| **Privileged (Architect/Admin)** | Real telemetry data (power, temperature, node stats), network config, security models | Requires architect/admin role; restrict ExaSage + Facility access |
| **Highly Sensitive** | Procurement, security, and access-control design | Use isolated RAG + approval gating |
| **Read-Only Mode** | Monitoring and topology visualization | Default safe mode for architects without write privileges |

---

## 4️⃣ Extended Example Question Corpus (25+ Examples)

1. What is the optimal CPU–GPU ratio for mixed AI and CFD workloads?  
2. How can we model interconnect latency for our current rack layout?  
3. Show me the thermal map of racks in zone C.  
4. Which cooling strategy offers the best PUE for 1 MW load?  
5. Compare the energy efficiency of liquid vs air cooling.  
6. How can we predict failures from IPMI temperature logs?  
7. Which nodes consume the most power during idle periods?  
8. What’s the impact of NUMA tuning on job performance?  
9. Suggest scheduler partitioning for hybrid CPU–GPU workloads.  
10. How much would it cost to upgrade from 100 Gbps to 400 Gbps fabric?  
11. Simulate LINPACK performance scaling for 512 nodes.  
12. What are best practices for topology-aware job scheduling?  
13. How to set up monitoring for InfiniBand port errors?  
14. Generate a performance baseline report for the new node configuration.  
15. Predict cooling demand if utilization rises to 90%.  
16. What redundancy model should we adopt for the power feeds?  
17. List recent node failures and their probable causes.  
18. How to integrate DCIM telemetry with HPC monitoring stack?  
19. What’s the expected network congestion under 70% load?  
20. Recommend rack placement to minimize cable length.  
21. Estimate the total CO₂ footprint of our current deployment.  
22. What firmware versions are compatible with our cluster design?  
23. Suggest benchmarking suite for AI and CFD combined workloads.  
24. What’s the best practice for container isolation in HPC?  
25. Generate architecture documentation in JSON/YAML for export.  
26. Predict hardware obsolescence timeline based on warranty data.  
27. Recommend job profiling tools for design validation.  
28. Compare facility metrics from 2024 vs 2025 installations.  

---

## 5️⃣ Priority Tags Summary

| Priority | Meaning | Example Categories |
|-----------|----------|--------------------|
| **H** | High frequency / mission-critical | Architecture design, performance modeling, monitoring, benchmarking |
| **M** | Medium frequency | Facility integration, software stack design, documentation |
| **L** | Low frequency but strategic | Sustainability, lifecycle planning |

---

📄 **Suggested filename:**  
`hpc_system_designers_query_taxonomy.md`
