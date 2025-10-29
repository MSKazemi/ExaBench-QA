# 🧠 HPC Researchers — Query & Need Taxonomy for HPC Agentic Chat System

---

## 1️⃣ Category List (High-Level Overview)

| # | Category | Priority |
|--|------------|-----------|
| 1 | Job Submission & Workflow Management | H |
| 2 | Resource Discovery & Allocation | H |
| 3 | Monitoring & Performance Metrics | H |
| 4 | Debugging & Troubleshooting | H |
| 5 | Profiling & Optimization | H |
| 6 | Data Management & I/O Performance | H |
| 7 | Environment & Module Setup | M |
| 8 | Software Installation & Dependencies | M |
| 9 | Visualization & Result Analysis | M |
| 10 | Reproducibility & Experiment Tracking | M |
| 11 | Documentation, Tutorials & Best Practices | M |
| 12 | Collaboration & Sharing | L |
| 13 | Facility / Room / Power Awareness | L |
| 14 | Security, Access & Policy Queries | L |

---

## 2️⃣ Detailed Table Version

| Category | Description | Example Queries | Agent(s) to Fulfill Request |
|-----------|--------------|-----------------|-----------------------------|
| **Job Submission & Workflow Management** | All interactions for running, scheduling, and managing jobs. | “Submit my SLURM job script.”<br>“Show estimated queue wait time for GPU partition.”<br>“Cancel job 10234.” | HPC Job Executor Agent |
| **Resource Discovery & Allocation** | Finding optimal compute nodes and understanding available partitions. | “Which nodes have A100 GPUs?”<br>“How much memory can I request in the `gpu_long` queue?” | RAG Agent + Monitoring Agent |
| **Monitoring & Performance Metrics** | Real-time and historical insights on job/node utilization. | “Show CPU/GPU utilization for job 23456.”<br>“Plot my last week’s node usage.”<br>“Was my job memory-bound?” | ExaSage Monitoring Agent |
| **Debugging & Troubleshooting** | Detecting issues in jobs or applications. | “Why did my MPI job crash?”<br>“Show OOM events for my last job.”<br>“Check stderr of job 44321.” | Monitoring Agent + Log Agent |
| **Profiling & Optimization** | Fine-grained code-level or system-level performance insights. | “Profile my job using nvprof.”<br>“Identify communication bottlenecks in MPI.”<br>“Suggest compiler flags for better vectorization.” | Data Analytics Agent + HPC Executor |
| **Data Management & I/O Performance** | Data staging, parallel file system usage, throughput analysis. | “Copy results from scratch to project folder.”<br>“Check Lustre I/O bandwidth.”<br>“List large files in my /scratch directory.” | HPC Executor + Monitoring Agent |
| **Environment & Module Setup** | Managing software environments and modules. | “Load Python 3.10 with TensorFlow.”<br>“Which modules conflict with OpenMPI?”<br>“Save my conda environment.” | RAG Agent + HPC Executor |
| **Software Installation & Dependencies** | Request or self-manage custom software builds. | “Can I install PyTorch in my home?”<br>“Request installation of GROMACS 2024.” | Admin Agent (for requests) + RAG |
| **Visualization & Result Analysis** | Data visualization, log summaries, post-processing. | “Plot my energy consumption per iteration.”<br>“Generate heatmap of GPU temperature.” | Data Analytics Agent + Monitoring |
| **Reproducibility & Experiment Tracking** | Managing run metadata, seeds, and version control. | “Tag this run as baseline.”<br>“Compare performance of exp_12 vs exp_15.” | Data Analytics Agent + RAG |
| **Documentation, Tutorials & Best Practices** | Learning HPC usage and best practices. | “How to run TensorFlow with SLURM?”<br>“Explain difference between partitions.” | RAG Agent |
| **Collaboration & Sharing** | Team work, shared datasets, shared job scripts. | “Share my job script with user Anna.”<br>“Give read-only access to my logs.” | RAG Agent + Admin Agent |
| **Facility / Room / Power Awareness** | Awareness of physical infrastructure and power metrics. | “What is power usage of my rack?”<br>“Show thermal map of my compute node.” | Facility Agent + ExaSage Monitoring |
| **Security, Access & Policy Queries** | User privileges, quota limits, and authentication issues. | “Why was my SSH access denied?”<br>“How much project storage is left?” | Admin Agent + RAG |

---

## 3️⃣ Permissions & Access Control Notes

| Category | Access Level | Notes |
|-----------|---------------|-------|
| Job Submission, Monitoring, Profiling | **User-level** | Allowed for authenticated HPC users. |
| Resource Discovery | **User-level** | Can expose aggregated, non-sensitive info. |
| Data Management | **User-level** (home/project dirs) | Access limited to owned/group directories. |
| Software Installations | **Elevated** | Admin approval required for cluster-wide packages. |
| Facility / Power Awareness | **Restricted** | Aggregated, anonymized data view only for researchers. |
| Security & Access | **Sensitive** | Must route through secure admin-only agent. |

---

## 4️⃣ Extended Example Questions Corpus (≥25)

1. Can you show me the GPU utilization of my last job?  
2. List all my failed jobs in the past week.  
3. Why did my MPI process rank 0 crash?  
4. Estimate queue time for 4 A100 GPUs.  
5. Plot memory usage over runtime for job 4321.  
6. Which nodes are free right now?  
7. Show historical CPU usage for my account.  
8. Compare runtime of experiment v1 and v2.  
9. Optimize my job for memory bandwidth.  
10. How to use SLURM job arrays for my simulations?  
11. Monitor power consumption of my running job.  
12. Which module should I load for CUDA 12.2?  
13. Install PyTorch Lightning in my conda environment.  
14. Copy data from `/scratch` to `/project`.  
15. Visualize temperature map of GPU nodes.  
16. List top I/O intensive jobs this week.  
17. Why did my job exceed memory limit?  
18. How do I request longer walltime?  
19. Explain the difference between `gpu_short` and `gpu_long` partitions.  
20. Can I share my dataset with user x?  
21. Show last 10 lines of job log 7890.  
22. Generate energy efficiency report for my project.  
23. Tag job 5678 as ‘baseline’ in experiment tracker.  
24. Where is my output file stored?  
25. How do I reproduce job 12345 from my history?

---

## 5️⃣ Priority Tags Summary

| Priority | Meaning | Categories |
|-----------|----------|-------------|
| **H (High)** | Frequent, critical for research workflows | Job Submission, Resource Discovery, Monitoring, Debugging, Profiling, Data Management |
| **M (Medium)** | Periodic needs | Environment Setup, Reproducibility, Documentation, Visualization |
| **L (Low)** | Rare but high-value | Facility Awareness, Security, Collaboration |

---

*Generated using the standard taxonomy prompt for HPC user profiling.*
