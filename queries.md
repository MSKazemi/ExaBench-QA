| #  | Query                                                                                                                                     | User Type                                                                       | QCAT                      | Priority | Difficulty |
| -- | ----------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------- | -------- | ---------- |
| 1  | How much energy is consumed by the nodes, racks, and machine over a given period of time?                                                 | HPC Researchers, Facility Admin, System Admin, System Designers | ENERGY                | High     | Medium     |
| 2  | How much energy is consumed by the cooling system (air and water) over a given period of time?                                            | Facility Admin, System Designers, HPC Researchers                   | FAC / ENERGY          | High     | Medium     |
| 3  | What is the PUE (Power Usage Effectiveness) of a machine or compute room over a given period of time?                                     | Facility Admin, System Designers, HPC Researchers                   | ENERGY                | High     | Medium     |
| 4  | How many jobs are running on a particular node over a given period of time?                                                               | System Admin, Normal HPC User, HPC Researchers                      | JOB                   | High     | Easy       |
| 5  | Provide the distribution over time of the usage of resources (CPUs, GPUs, Memory) before a node fails, over a given period of time.       | HPC Researchers, System Admin                                           | PERF / MON / AIOPS    | High     | Hard       |
| 6  | Give me the node’s resource utilization distribution when the PUE is higher than a given value.                                           | HPC Researchers, System Designers                                       | ENERGY / AIOPS        | High     | Hard       |
| 7  | Give me the node’s resource utilization distribution for a specific JobID whose job PUE is higher than a given value.                     | HPC Researchers, System Admin                                           | ENERGY / PERF / AIOPS | High     | Hard       |
| 8  | Give me the node’s resource utilization distribution for a specific JobID whose job power is higher than a given value.                   | HPC Researchers, System Admin                                           | ENERGY / PERF         | High     | Medium     |
| 9  | Provide the node’s resource utilization (or users) distribution for all jobs whose node’s average job power is higher than a given value. | HPC Researchers, System Admin                                           | ENERGY / PERF / MON   | High     | Hard       |
| 10 | What are the min, max, and average temperatures when a node is in use, over a given period of time?                                       | Facility Admin, System Admin, HPC Researchers                       | MON / ENERGY          | High     | Medium     |
| 11 | What are the min, max, and average of the derivative of temperature when a node is in use, over a given period of time?                   | HPC Researchers, Facility Admin                                         | MON / ENERGY          | High     | Hard       |
| 12 | What is the distribution of the temperature of a node before it fails, over a given period of time (period before failure)?               | HPC Researchers, System Admin, Facility Admin                       | AIOPS / MON           | High     | Hard       |
| 13 | Provide the list of failing nodes over a given period of time.                                                                            | System Admin, Facility Admin, HPC Researchers                       | MON / AIOPS           | High     | Medium     |
| 14 | Give me the Job IDs whose node’s instantaneous (or average over time) power/temperature is higher than a given threshold.                 | System Admin, HPC Researchers                                           | ENERGY / MON / JOB    | High     | Medium     |
| 15 | What is the position of node X?                                                                                                           | Facility Admin, System Admin, System Designers                      | FAC / ARCH            | Medium   | Easy       |
| 16 | How many racks are there in an HPC system X?                                                                                              | System Designers, Facility Admin, System Admin                      | ARCH / FAC            | Medium   | Easy       |
| 17 | Which nodes are part of the rack X?                                                                                                       | System Admin, Facility Admin, System Designers                      | FAC / ARCH            | Medium   | Easy       |
| 18 | How many HPC systems do we have?                                                                                                          | System Designers, System Admin                                          | ARCH / FAC            | Medium   | Easy       |
| 19 | Give me a list of users who submitted jobs in a specified time period.                                                                    | System Admin, HPC Researchers                                           | JOB / USER            | High     | Easy       |
| 20 | Give me a list of jobs submitted by the user X in a specified time period.                                                                | System Admin, HPC Researchers, Normal HPC User                      | JOB                   | High     | Easy       |
| 21 | Give me a list of jobs submitted in a specified time period.                                                                              | System Admin, HPC Researchers, Normal HPC User                      | JOB                   | High     | Easy       |
| 22 | Which user submitted job X?                                                                                                               | System Admin, Normal HPC User                                           | JOB / USER            | High     | Easy       |
| 23 | Give details of job X.                                                                                                                    | System Admin, Normal HPC User                                           | JOB / PERF            | High     | Medium     |
| 24 | How many jobs were running in a specified time period?                                                                                    | System Admin, Normal HPC User                                           | JOB / MON             | High     | Easy       |
| 25 | How many jobs had a time duration above a certain value?                                                                                  | System Admin, HPC Researchers                                           | JOB / PERF            | Medium   | Medium     |
| 26 | Which user submitted jobs during a specified period?                                                                                      | System Admin                                                                | JOB / USER            | Medium   | Easy       |
| 27 | How many jobs did a user U submit on a compute node N in a specified period?                                                              | System Admin, HPC Researchers                                           | JOB / PERF / MON      | Medium   | Medium     |
| 28 | Which users belong to a group G?                                                                                                          | System Admin                                                                | SEC / USER            | Medium   | Easy       |
| 29 | What is the power consumption of the node X in a specified time period?                                                                   | System Admin, HPC Researchers, Facility Admin                       | ENERGY / MON          | High     | Medium     |
| 30 | What is the power consumption of the rack X in a specified time period?                                                                   | System Admin, Facility Admin, System Designers                      | ENERGY / FAC          | High     | Medium     |
| 31 | What is the max/min/avg recorded metric X for compute node N from T1 to T2?                                                               | System Admin, HPC Researchers, Facility Admin                       | MON / PERF            | High     | Medium     |
| 32 | What is the max/min/avg recorded metric X for rack R today?                                                                               | System Admin, Facility Admin                                            | MON / ENERGY          | High     | Medium     |
| 33 | What is the max/min/avg recorded metric X for Job J?                                                                                      | System Admin, HPC Researchers, Normal HPC User                      | MON / PERF            | High     | Medium     |
| 34 | Can you tell me the list of compute nodes that had temperatures higher than normal in a specified time period?                            | Facility Admin, System Admin, HPC Researchers                       | MON / ENERGY / AIOPS  | High     | Medium     |
| 35 | Please provide me the compute node N average temperature during May 2025.                                                                 | Facility Admin, System Admin                                            | MON / ENERGY          | Medium   | Easy       |
| 1  | What is the current total CPU utilization across all nodes?              | System Admin, HPC Researchers                      | PERF / MON      | High     | Easy       |
| 2  | Which nodes have the highest average CPU usage over the past 24 hours?   | System Admin, HPC Researchers                      | PERF / MON      | High     | Medium     |
| 3  | How much GPU memory is currently in use per GPU device?                  | System Admin, Normal HPC User, HPC Researchers | PERF / MON      | High     | Easy       |
| 4  | What is the GPU utilization trend for the top 10 busiest GPUs this week? | System Admin, HPC Researchers                      | PERF / MON      | Medium   | Medium     |
| 5  | How much RAM is allocated versus available in the cluster right now?     | System Admin                                           | PERF / MON      | High     | Easy       |
| 6  | Which nodes are running low on free memory or swap?                      | System Admin, HPC Researchers                      | MON / PERF      | High     | Medium     |
| 7  | What is the total disk usage and free space per partition across nodes?  | System Admin, Facility Admin                       | DATA / MON      | High     | Medium     |
| 8  | What is the network traffic in/out per rack over the last hour?          | System Admin, Facility Admin                       | MON / NET / FAC | Medium   | Medium     |
| 9  | Which nodes have the highest I/O wait percentage?                        | System Admin, HPC Researchers                      | PERF / MON      | Medium   | Hard       |
| 10 | What are the top processes or jobs consuming the most CPU resources?     | System Admin, HPC Researchers, Normal HPC User | JOB / PERF      | High     | Medium     |
| 11 | What is the total power consumption of the entire cluster from IPMI sensors? | System Admin, Facility Admin, HPC Researchers | ENERGY / MON | High | Medium |
| 12 | How much power is used by CPUs versus GPUs in each node? | HPC Researchers, System Designers | ENERGY / PERF | High | Hard |
| 13 | Which racks have the highest power draw? | Facility Admin, System Admin, System Designers | ENERGY / FAC | High | Medium |
| 14 | What is the data center’s total IT power consumption (Logics plugin)? | Facility Admin, System Designers | ENERGY / FAC | High | Medium |
| 15 | What is the total power used by CRACs, chillers, and pumps (Logics)? | Facility Admin | FAC / ENERGY | High | Medium |
| 16 | What is the Power Usage Effectiveness (PUE) trend for the past week? | Facility Admin, System Designers, HPC Researchers | ENERGY / FAC | High | Medium |
| 17 | Which nodes show abnormal increases in power usage compared to average? | System Admin, HPC Researchers | AIOPS / ENERGY / MON | High | Hard |
| 18 | How much energy (kWh) was consumed by the IT equipment in the last 24 hours? | Facility Admin, System Admin, HPC Researchers | ENERGY | Medium | Medium |
| 19 | What is the correlation between node power consumption and CPU load? | HPC Researchers, System Admin | PERF / ENERGY / AIOPS | High | Hard |
| 20 | Are there any nodes exceeding their configured power limits? | System Admin, Facility Admin | ENERGY / MON | High | Medium |
| 21 | What are the inlet (ambient) temperatures per node from IPMI? | Facility Admin, System Admin | MON / ENERGY | High | Easy |
| 22 | Which nodes show high GPU or DIMM temperatures? | System Admin, HPC Researchers, Facility Admin | MON / ENERGY | High | Medium |
| 23 | How does node temperature correlate with power consumption? | HPC Researchers, System Admin | AIOPS / ENERGY / PERF | High | Hard |
| 24 | What is the current return and supply air temperature from Vertiv units? | Facility Admin | FAC / MON | Medium | Easy |
| 25 | Which CRAC units are operating at maximum compressor utilization? | Facility Admin | FAC / COOL / MON | High | Medium |
| 26 | What is the temperature delta between supply and return air across all units? | Facility Admin, System Designers | FAC / MON / ENERGY | Medium | Medium |
| 27 | What is the liquid cooling flow rate in each Schneider RDHx circuit? | Facility Admin | FAC / MON | Medium | Hard |
| 28 | Which pumps or valves in the cooling system report alarms or faults? | Facility Admin | FAC / ALARM / MON | High | Medium |
| 29 | How balanced are the temperatures between different cooling zones? | Facility Admin, System Designers | FAC / ENERGY / MON | Medium | Medium |
| 30 | What are the outdoor weather temperature and humidity, and how do they affect inlet temperatures? | Facility Admin, HPC Researchers | FAC / ENV / ENERGY | Medium | Medium |
| 31 | How many jobs are currently running, pending, or failed in SLURM? | System Admin, Normal HPC User, HPC Researchers | JOB / MON | High | Easy |
| 32 | Which partitions have the highest average waiting time for jobs? | System Admin, HPC Researchers | JOB / PERF | Medium | Medium |
| 33 | What is the 95th percentile of job waiting time across all QoS classes? | System Admin, HPC Researchers | JOB / PERF | Medium | Hard |
| 34 | Which users or groups consume the most resources (CPU/GPU hours)? | System Admin, HPC Researchers | JOB / PERF / USER | High | Medium |
| 35 | What is the overall cluster CPU/GPU allocation efficiency? | System Admin, HPC Researchers | PERF / AIOPS / JOB | High | Hard |
| 36 | Which jobs consumed the most energy per run? | HPC Researchers, System Admin | ENERGY / JOB | Medium | Medium |
| 37 | What is the distribution of job durations by QoS and partition? | System Admin, HPC Researchers | JOB / PERF | Medium | Medium |
| 38 | How many nodes are currently idle or down? | System Admin | MON / JOB | High | Easy |
| 39 | What is the average node utilization across the past week? | System Admin, HPC Researchers | MON / PERF | Medium | Medium |
| 40 | Which jobs frequently fail or exit with non-zero codes? | System Admin, HPC Researchers | JOB / DEBUG / PERF | High | Medium |
| 41 | Which nodes have active Nagios alarms? | System Admin, Facility Admin | MON / ALARM | High | Easy |
| 42 | What are the most common critical service alerts from Nagios this month? | System Admin | ALARM / MON | Medium | Medium |
| 43 | Are there any BMC or GPU memory ECC errors reported recently? | System Admin, HPC Researchers | MON / AIOPS | High | Medium |
| 44 | Which nodes experienced XID GPU errors or thermal violations? | System Admin, HPC Researchers | MON / PERF / AIOPS | High | Hard |
| 45 | What percentage of nodes are in maintenance or drained state? | System Admin | MON / NODE / JOB | High | Easy |
| 46 | Which cooling pumps or valves triggered alarms in Schneider PLC logs? | Facility Admin | FAC / MON / ALARM | Medium | Medium |
| 47 | What is the number of communication failures (Comlost) in Logics data? | Facility Admin | FAC / MON | Medium | Medium |
| 48 | Are all network switches and storage systems reported healthy by Nagios? | System Admin, Facility Admin | MON / NET / STOR | High | Medium |
| 49 | Which nodes have rebooted within the last 24 hours? | System Admin, Facility Admin | MON / NODE | High | Easy |
| 50 | What is the overall cluster availability and health status summary? | System Admin, System Designers | MON / AIOPS | High | Medium |
| 51 | Detect nodes showing abnormal correlation between power and temperature. | HPC Researchers, System Admin | AIOPS / ENERGY / MON | High | Hard |
| 52 | Identify GPUs whose utilization dropped below 10 % for more than 6 hours. | HPC Researchers, System Admin | AIOPS / PERF / MON | Medium | Hard |
| 53 | Find nodes where CPU temperature increased faster than 10 °C in 5 minutes. | HPC Researchers, Facility Admin | AIOPS / MON / ENERGY | High | Hard |
| 54 | Detect outliers in power consumption versus average node group trend. | HPC Researchers, System Admin | AIOPS / ENERGY / MON | High | Hard |
| 55 | Which GPUs reported repeated ECC errors in the past week? | System Admin, HPC Researchers | AIOPS / MON | Medium | Hard |
| 56 | List nodes with more than 5 unexpected reboots this month. | System Admin, Facility Admin | AIOPS / MON | Medium | Medium |
| 57 | Highlight cooling units whose compressor utilization deviates > 20 % from peers. | Facility Admin, System Designers | AIOPS / FAC / COOL | Medium | Hard |
| 58 | Predict next 24 hours power consumption using last 7 days trend. | HPC Researchers, System Designers | AIOPS / ENERGY | High | Hard |
| 59 | Which nodes show an unusual pattern of memory errors correlated with ambient temperature? | HPC Researchers, System Admin | AIOPS / MON / ENERGY | High | Hard |
| 60 | Detect pumps or valves in Schneider data that oscillate abnormally (PID instability). | Facility Admin | AIOPS / FAC / MON | Medium | Hard |
| 61 | What is the average CPU utilization trend over the last 30 days per partition? | System Admin, System Designers | PERF / ARCH / MON | Medium | Medium |
| 62 | How much GPU capacity remains unused per QoS class? | System Admin, HPC Researchers | PERF / JOB | Medium | Medium |
| 63 | Forecast when current storage utilization will reach 90 % capacity. | System Admin, HPC Researchers, System Designers | AIOPS / DATA / PERF | High | Hard |
| 64 | Which racks consistently operate near power limit thresholds? | Facility Admin, System Designers | ENERGY / FAC | Medium | Medium |
| 65 | What is the trend of job submission rate per user group? | System Admin, HPC Researchers | JOB / PERF | Medium | Medium |
| 66 | Which partitions experience the longest cumulative queue times? | System Admin, HPC Researchers | JOB / PERF | Medium | Medium |
| 67 | What is the ratio of idle vs allocated nodes across the past month? | System Admin | MON / JOB / PERF | Medium | Medium |
| 68 | How many GPUs are typically idle during off-peak hours? | System Admin, HPC Researchers | PERF / AIOPS | Medium | Medium |
| 69 | How balanced is job distribution across nodes and racks? | System Admin, HPC Researchers, System Designers | JOB / PERF / FAC | Medium | Hard |
| 70 | What fraction of nodes remain powered on but unused for more than 12 hours daily? | System Admin, Facility Admin | ENERGY / AIOPS / MON | Medium | Hard |
| 71 | Compute PUE every 15 minutes and detect degradation periods. | Facility Admin, System Designers | ENERGY / AIOPS | High | Medium |
| 72 | Correlate ambient outdoor temperature with total cooling power consumption. | HPC Researchers, Facility Admin | ENERGY / AIOPS / FAC | Medium | Hard |
| 73 | Identify CRAC units with the poorest temperature regulation stability. | Facility Admin | FAC / AIOPS / COOL | Medium | Hard |
| 74 | What is the efficiency difference between air-cooled and liquid-cooled racks? | System Designers, Facility Admin | ENERGY / FAC / PERF | Medium | Medium |
| 75 | Compute average energy per job and identify energy-intensive workloads. | HPC Researchers, System Admin | ENERGY / JOB / PERF | High | Medium |
| 76 | Estimate potential energy savings from consolidating low-load nodes. | System Admin, System Designers | ENERGY / AIOPS / PERF | Medium | Hard |
| 77 | Compare total IT energy (Logics) with IPMI-reported node energy to find discrepancies. | HPC Researchers, System Admin | ENERGY / AIOPS / MON | Medium | Hard |
| 78 | Identify nodes frequently exceeding 85 % of their power limit. | System Admin, HPC Researchers | ENERGY / MON / AIOPS | High | Medium |
| 79 | Compute cooling energy per °C of inlet temperature reduction. | Facility Admin, System Designers | ENERGY / FAC / PERF | Medium | Hard |
| 80 | Estimate CO₂ emissions based on total energy and regional carbon intensity. | HPC Researchers, Facility Admin, System Designers | ENERGY / SUSTAIN | Medium | Hard |
| 81 | Which fans in IPMI data show decreased RPM trends over time? | System Admin, Facility Admin | MON / AIOPS / HEALTH | Medium | Hard |
| 82 | List all nodes with “CRITICAL” state in Nagios for more than 1 hour. | System Admin | MON / ALARM | High | Medium |
| 83 | Detect jobs that failed repeatedly due to hardware or thermal issues. | System Admin, HPC Researchers | AIOPS / JOB / MON | High | Hard |
| 84 | Which nodes have persistent “down” or “drained” state in SLURM? | System Admin | MON / JOB / NODE | High | Medium |
| 85 | Identify power supplies showing unstable voltage or current readings. | Facility Admin, System Admin | FAC / MON / AIOPS | Medium | Hard |
| 86 | What percentage of cooling alarms were unresolved within 30 minutes? | Facility Admin | FAC / ALARM / MON | Medium | Medium |
| 87 | List devices with missing data (Comlost = 1) in Logics telemetry. | Facility Admin | FAC / MON / DATA | Medium | Easy |
| 88 | Which network switches reported hardware faults most often? | System Admin, Facility Admin | NET / MON / AIOPS | Medium | Medium |
| 89 | How many ECC errors per GPU occurred before a job crash? | HPC Researchers, System Admin | AIOPS / MON / PERF | Medium | Hard |
| 90 | Which nodes exhibit recurring BMC or BIOS sensor failures? | System Admin, Facility Admin | AIOPS / MON / NODE | Medium | Medium |
| 91 | How does outdoor humidity affect data center inlet temperature? | Facility Admin, HPC Researchers | FAC / ENV / ENERGY | Medium | Medium |
| 92 | Identify days when strong wind correlated with lower inlet temperature. | Facility Admin, HPC Researchers | FAC / ENV / ENERGY | Low | Medium |
| 93 | Compare weather pressure trends with CRAC static pressure values. | Facility Admin, System Designers | FAC / ENV / MON | Low | Medium |
| 94 | Compute daily dew-point average and correlate with humidity alarms. | Facility Admin, HPC Researchers | FAC / MON / ENERGY | Medium | Medium |
| 95 | Determine if weather temperature anomalies affect power usage efficiency. | Facility Admin, HPC Researchers, System Designers | FAC / ENERGY / AIOPS | Medium | Hard |
| 96 | Rank top 10 users by energy cost per job. | System Admin, HPC Researchers | ENERGY / JOB / PERF | High | Medium |
| 97 | Identify jobs that consumed most GPU time but least CPU utilization. | HPC Researchers, System Admin | PERF / JOB / AIOPS | Medium | Hard |
| 1  | Compute average waiting-time penalty per partition vs. resource availability.        | System Admin, HPC Researchers                      | JOB / PERF          | Medium   | Medium     |
| 2  | Show trend of maintenance alarms per subsystem over the past quarter.                | Facility Admin, System Admin                       | FAC / ALARM / MON   | Medium   | Medium     |
| 3  | Generate summary of total uptime percentage for compute, cooling, and power systems. | System Admin, Facility Admin, System Designers | MON / FAC / AIOPS   | High     | Medium     |
| 4  | What jobs are currently running under my user ID?                                    | Normal HPC User, System Admin                      | JOB / MON           | High     | Easy       |
| 5  | Show me all my pending jobs and their waiting times.                                 | Normal HPC User, System Admin                      | JOB / QUEUE         | High     | Easy       |
| 6  | How long did job 458932 take to complete?                                            | Normal HPC User, HPC Researchers                   | JOB / PERF          | High     | Easy       |
| 7  | What is the status of job 458932?                                                    | Normal HPC User, System Admin                      | JOB                 | High     | Easy       |
| 8  | Which partition did my job 458932 run on?                                            | Normal HPC User, System Admin                      | JOB / QUEUE / PERF  | Medium   | Easy       |
| 9  | How many nodes were allocated to job 458932?                                         | Normal HPC User, System Admin                      | JOB / MON / RES     | Medium   | Easy       |
| 10 | What is the average waiting time in the queue today?                                 | Normal HPC User, System Admin                      | JOB / QUEUE         | Medium   | Easy       |
| 11 | Which queue has the shortest average waiting time?                                   | Normal HPC User, System Admin                      | JOB / QUEUE         | High     | Easy       |
| 12 | How many jobs failed in the last 24 hours?                                           | System Admin, Normal HPC User                      | JOB / MON / DEBUG   | High     | Easy       |
| 13 | What are the top users by number of submitted jobs this week?                        | System Admin, HPC Researchers                      | JOB / USER / PERF   | Medium   | Medium     |
| 14 | Show CPU utilization for my last five jobs.                                          | Normal HPC User, HPC Researchers                   | PERF / MON / JOB    | Medium   | Medium     |
| 15 | What was the GPU utilization for job 458932?                                         | Normal HPC User, HPC Researchers                   | PERF / MON / JOB    | Medium   | Medium     |
| 16 | Plot memory usage over time for job 458932.                                          | Normal HPC User, HPC Researchers                   | PERF / MON          | Medium   | Medium     |
| 17 | What was the peak GPU temperature during my job?                                     | Normal HPC User, HPC Researchers                   | ENERGY / MON / PERF | Medium   | Medium     |
| 18 | Show CPU idle percentage across all my allocated nodes.                              | Normal HPC User, System Admin                      | MON / PERF          | Medium   | Medium     |
| 19 | What is the average CPU speed (MHz) for my current job nodes?                        | Normal HPC User, HPC Researchers                   | PERF / MON          | Medium   | Medium     |
| 20 | How many GPUs were active during my last run?                                        | Normal HPC User, HPC Researchers                   | PERF / MON / JOB    | Medium   | Medium     |
| 21 | Did any of my jobs exceed the memory limit?                                          | Normal HPC User, System Admin                      | JOB / PERF / DEBUG  | High     | Easy       |
| 22 | Which nodes showed the highest load during my simulation?                            | Normal HPC User, HPC Researchers                   | PERF / MON / JOB    | Medium   | Medium     |
| 23 | What is the total GPU energy consumption per job?                                    | Normal HPC User, HPC Researchers                   | ENERGY / JOB / PERF | Medium   | Medium     |
| 24 | How much storage space am I currently using?                                         | Normal HPC User, System Admin                      | DATA / STOR / MON   | High     | Easy       |
| 25 | List my largest files in the scratch directory.                                      | Normal HPC User                                        | DATA / STOR         | High     | Easy       |
| 26 | What percentage of my project quota is used?                                         | Normal HPC User, System Admin                      | DATA / STOR / SEC   | Medium   | Easy       |
| 27 | Which directory has the highest disk usage?                                          | Normal HPC User                                        | DATA / STOR / MON   | Medium   | Medium     |
| 28 | Show total free disk space on my allocated nodes.                                    | Normal HPC User, System Admin                      | DATA / STOR / MON   | Medium   | Easy       |
| 29 | Has my job ever failed due to insufficient disk space?                               | Normal HPC User, System Admin                      | DATA / DEBUG / JOB  | Medium   | Easy       |
| 30 | Compare disk usage between home and project directories.                             | Normal HPC User, System Admin                      | DATA / STOR         | Medium   | Medium     |
| 31 | When was my quota last exceeded?                                                     | Normal HPC User, System Admin                      | DATA / STOR / SEC   | Medium   | Medium     |
| 32 | How many files were modified in my scratch directory this week?                      | Normal HPC User                                        | DATA / STOR / MON   | Low      | Easy       |
| 33 | List files older than 30 days to clean up.                                           | Normal HPC User                                        | DATA / STOR / AUTO  | Medium   | Easy       |
| 34 | Which modules are currently loaded in my session?                                    | Normal HPC User                                        | SOFT / MON          | High     | Easy       |
| 35 | What version of Python is available on the system?                                   | Normal HPC User, System Admin                      | SOFT / DOCS         | Medium   | Easy       |
| 36 | Load TensorFlow with CUDA support.                                                   | Normal HPC User                                        | SOFT / GPU / ENV    | High     | Easy       |
| 37 | Is CUDA 12 available on this cluster?                                                | Normal HPC User, System Admin                      | SOFT / GPU / DOCS   | Medium   | Easy       |
| 38 | Show all installed scientific libraries related to MPI.                              | Normal HPC User, System Admin                      | SOFT / DOCS / PERF  | Medium   | Easy       |
| 39 | Check if my environment has OpenBLAS enabled.                                        | Normal HPC User, System Admin                      | SOFT / PERF         | Medium   | Medium     |
| 40 | Which compiler version is recommended for my code?                                   | Normal HPC User, System Admin, HPC Researchers | SOFT / DOCS / PERF  | Medium   | Medium     |
| 41 | How can I load GROMACS with GPU acceleration?                                        | Normal HPC User                                        | SOFT / GPU / DOCS   | Medium   | Easy       |
| 42 | Display all available software modules related to machine learning.                  | Normal HPC User                                        | SOFT / DOCS         | Medium   | Easy       |
| 43 | What MPI implementations are currently supported?                                    | Normal HPC User, System Admin                      | SOFT / DOCS / PERF  | Medium   | Easy       |
| 44 | Why did my last job fail?                                                            | Normal HPC User, System Admin                      | JOB / DEBUG / LOGS  | High     | Easy       |
| 45 | Show me the error log for job 458932.                                                | Normal HPC User, System Admin                      | JOB / DEBUG / LOGS  | High     | Easy       |
| 46 | Which node caused my job failure?                                                    | Normal HPC User, System Admin                      | JOB / DEBUG / MON   | High     | Medium     |
| 47 | Did my job exceed the time limit?                                                    | Normal HPC User, System Admin                      | JOB / DEBUG / PERF  | High     | Easy       |
| 48 | What was the reason my job was requeued?                                             | Normal HPC User, System Admin                      | JOB / DEBUG / QUEUE | Medium   | Easy       |
| 49 | Were there any thermal alerts on nodes used by my job?                               | Normal HPC User, System Admin, HPC Researchers | ENERGY / MON / JOB  | Medium   | Medium     |
| 50 | Did the scheduler report resource contention for my job?                             | Normal HPC User, System Admin, HPC Researchers | JOB / PERF / DEBUG  | Medium   | Medium     |
| 51 | Show exit code and state reason for failed jobs.                                     | Normal HPC User, System Admin                      | JOB / DEBUG / LOGS  | High     | Easy       |
| 52 | What percentage of my jobs finished successfully this month?                         | Normal HPC User, System Admin                      | JOB / PERF / MON    | Medium   | Easy       |
| 1  | Suggest possible causes for MPI rank errors.                                 | Normal HPC User, HPC Researchers, System Admin    | DEBUG / JOB / PERF | High     | Medium     |
| 2  | Show current CPU utilization across the cluster.                             | System Admin, HPC Researchers                     | MON / PERF         | High     | Easy       |
| 3  | What is the average GPU utilization in my partition?                         | System Admin, HPC Researchers                     | MON / PERF         | High     | Medium     |
| 4  | Display node temperature trends for my active jobs.                          | Normal HPC User, System Admin                     | MON / ENERGY       | High     | Medium     |
| 5  | Plot CPU and memory usage trends during my simulation.                       | Normal HPC User, HPC Researchers                  | MON / PERF         | High     | Medium     |
| 6  | Which nodes are reporting high ambient temperature?                          | System Admin, Facility Admin                      | MON / FAC / ENERGY | High     | Medium     |
| 7  | Show total energy usage for my jobs today.                                   | Normal HPC User, HPC Researchers                  | ENERGY / JOB       | Medium   | Easy       |
| 8  | How many running processes are currently active per node?                    | System Admin                                      | MON / PERF         | Medium   | Medium     |
| 9  | What was the network throughput for my job 458932?                           | Normal HPC User, HPC Researchers                  | MON / PERF         | Medium   | Medium     |
| 10 | Display swap memory usage on my allocated nodes.                             | Normal HPC User, System Admin                     | MON / PERF         | Medium   | Easy       |
| 11 | How many jobs are running on nodes with fan speed alerts?                    | System Admin                                      | MON / ALARM / JOB  | High     | Medium     |
| 12 | Show GPU power consumption over time for my last job.                        | Normal HPC User, HPC Researchers                  | ENERGY / MON / JOB | Medium   | Medium     |
| 13 | What was the maximum GPU temperature reached today?                          | System Admin, Normal HPC User                     | MON / ENERGY       | Medium   | Easy       |
| 14 | Display GPU ECC error counts in my allocated nodes.                          | Normal HPC User, System Admin                     | MON / AIOPS        | Medium   | Medium     |
| 15 | Are there any GPUs with low utilization?                                     | System Admin, HPC Researchers                     | MON / PERF         | Medium   | Easy       |
| 16 | Compare GPU clock speeds across nodes used by my job.                        | Normal HPC User, HPC Researchers                  | MON / PERF         | Medium   | Medium     |
| 17 | What is the average GPU memory usage across my active jobs?                  | Normal HPC User, HPC Researchers                  | MON / PERF         | Medium   | Easy       |
| 18 | Did any GPU exceed its power management limit?                               | System Admin, HPC Researchers                     | ENERGY / MON       | High     | Medium     |
| 19 | Show NVLink error counts on my job nodes.                                    | System Admin, HPC Researchers                     | MON / PERF         | Medium   | Medium     |
| 20 | How much total GPU memory is available in my partition?                      | System Admin                                      | PERF / RES / MON   | Medium   | Easy       |
| 21 | Show GPU thermal violation events for my jobs.                               | Normal HPC User, System Admin                     | MON / ENERGY / JOB | High     | Medium     |
| 22 | What is the current PUE of the cluster?                                      | Facility Admin, System Designers, HPC Researchers | ENERGY / FAC       | High     | Easy       |
| 23 | How much total IT power is consumed right now?                               | Facility Admin, System Admin                      | ENERGY / FAC       | High     | Easy       |
| 24 | Show energy usage breakdown between compute and cooling.                     | Facility Admin, System Designers                  | ENERGY / FAC       | High     | Medium     |
| 25 | What was the average inlet temperature during my job?                        | Normal HPC User, HPC Researchers                  | MON / ENERGY       | Medium   | Easy       |
| 26 | Display total power consumption per rack.                                    | Facility Admin, System Admin                      | ENERGY / FAC       | High     | Medium     |
| 27 | How has cluster energy usage changed over the past week?                     | System Admin, HPC Researchers, Facility Admin     | ENERGY / MON       | Medium   | Medium     |
| 28 | Which CRAC units have the highest compressor utilization?                    | Facility Admin                                    | FAC / MON          | High     | Medium     |
| 29 | Show return air temperature trends for the cooling units.                    | Facility Admin                                    | FAC / MON          | Medium   | Medium     |
| 30 | Display humidity levels in the machine room.                                 | Facility Admin                                    | FAC / MON          | Medium   | Easy       |
| 31 | What is the difference between supply and return flow temperatures?          | Facility Admin                                    | FAC / MON          | Medium   | Medium     |
| 32 | What is the current outdoor temperature near the facility?                   | Facility Admin                                    | FAC / MON          | Low      | Easy       |
| 33 | How does outside humidity affect cooling energy use?                         | Facility Admin, HPC Researchers                   | FAC / ENERGY       | Medium   | Medium     |
| 34 | Show wind speed during the last peak cooling period.                         | Facility Admin                                    | FAC / MON          | Low      | Easy       |
| 35 | Was there any correlation between external temperature and job failure rate? | HPC Researchers, System Admin                     | AIOPS / MON / JOB  | Medium   | Hard       |
| 36 | How does external pressure vary during high compute load hours?              | Facility Admin, HPC Researchers                   | FAC / MON          | Low      | Medium     |
| 37 | Show top 10 jobs by total runtime this month.                                | System Admin, HPC Researchers                     | JOB / PERF         | Medium   | Easy       |
| 38 | Which job had the highest energy consumption?                                | System Admin, HPC Researchers                     | ENERGY / JOB       | Medium   | Medium     |
| 39 | What are the average CPU and GPU utilization per user?                       | System Admin, HPC Researchers                     | JOB / PERF / MON   | Medium   | Medium     |
| 40 | Compare job runtime and waiting time for my recent jobs.                     | Normal HPC User, HPC Researchers                  | JOB / PERF         | High     | Easy       |
| 41 | Generate performance summary for all my completed jobs.                      | Normal HPC User, HPC Researchers                  | JOB / PERF / DOCS  | Medium   | Medium     |
| 42 | Schedule a daily report of my job statistics.                                | Normal HPC User                                   | AUTO / JOB / DOCS  | Medium   | Easy       |
| 43 | Notify me when a job exceeds its time limit.                                 | Normal HPC User                                   | AUTO / JOB         | High     | Easy       |
| 44 | Automatically delete temporary files after job completion.                   | Normal HPC User                                   | AUTO / DATA        | Medium   | Easy       |
| 45 | Generate a weekly performance summary of my workloads.                       | Normal HPC User, HPC Researchers                  | AUTO / JOB / PERF  | Medium   | Easy       |
| 46 | Alert me if GPU utilization drops below 20%.                                 | Normal HPC User, System Admin                     | AUTO / MON / PERF  | High     | Easy       |
| 47 | Share my project directory with user “alice”.                                | Normal HPC User, System Admin                     | SEC / DATA         | Medium   | Easy       |
| 48 | Check permissions for the folder `/project/shared`.                          | Normal HPC User, System Admin                     | SEC / DATA         | Medium   | Easy       |
| 49 | Add SSH key to enable remote job submission.                                 | Normal HPC User, System Admin                     | SEC / DOCS         | High     | Easy       |
| 50 | Who has access to my project folder?                                         | Normal HPC User, System Admin                     | SEC / DATA         | Medium   | Easy       |
| 51 | List collaborators with active jobs in the same partition.                   | Normal HPC User, System Admin                     | JOB / USER / MON   | Medium   | Easy       |
| 1   | Show the temperature map for each datacenter zone.              | Facility Admin / Technicians                                                 | FAC / MON             | High     | Medium     |
| 2   | Which racks exceed 28 °C inlet temperature?                     | Facility Admin / Technicians, System Admin                                   | FAC / MON / ENERGY    | High     | Easy       |
| 3   | List humidity readings for all rooms.                           | Facility Admin / Technicians                                                 | FAC / MON             | Medium   | Easy       |
| 4   | What is the average airflow rate per rack?                      | Facility Admin / Technicians                                                 | FAC / MON             | Medium   | Medium     |
| 5   | Compare inlet vs outlet temperature across zones.               | Facility Admin / Technicians, System Designers / Architects                  | FAC / MON / ENERGY    | Medium   | Medium     |
| 6   | Show temperature difference between supply and return air.      | Facility Admin / Technicians                                                 | FAC / MON             | Medium   | Easy       |
| 7   | Detect racks with unstable thermal gradients.                   | Facility Admin / Technicians, HPC Researchers                                | AIOPS / FAC / MON     | High     | Hard       |
| 8   | Report average ambient temperature for the past 24 h.           | Facility Admin / Technicians                                                 | FAC / MON             | Medium   | Easy       |
| 9   | Which areas have humidity below 35 %?                           | Facility Admin / Technicians                                                 | FAC / MON             | Medium   | Easy       |
| 10  | Identify hotspots detected by IPMI sensors today.               | Facility Admin / Technicians, System Admin                                   | MON / ENERGY / FAC    | High     | Medium     |
| 11  | Compare CRAC unit efficiency (Vertiv metrics) by power usage.   | Facility Admin / Technicians, System Designers / Architects                  | ENERGY / FAC          | High     | Medium     |
| 12  | Show compressor utilization trend for all CRACs.                | Facility Admin / Technicians                                                 | FAC / MON             | Medium   | Medium     |
| 13  | Which CRAC units have Free-Cooling mode active?                 | Facility Admin / Technicians                                                 | FAC / MON             | Medium   | Easy       |
| 14  | Report supply and return air temperatures per CRAC.             | Facility Admin / Technicians                                                 | FAC / MON             | Medium   | Easy       |
| 15  | Correlate fan speed with return air temperature.                | Facility Admin / Technicians, HPC Researchers                                | AIOPS / FAC / MON     | Medium   | Medium     |
| 16  | Detect pressure drop anomalies in filter sensors.               | Facility Admin / Technicians                                                 | AIOPS / FAC / MON     | High     | Hard       |
| 17  | Which CRAC units have humidity control enabled?                 | Facility Admin / Technicians                                                 | FAC / MON             | Medium   | Easy       |
| 18  | Compute average Free-Cooling fluid temperature.                 | Facility Admin / Technicians                                                 | FAC / MON             | Medium   | Easy       |
| 19  | Identify underperforming CRACs with low cooling delta.          | Facility Admin / Technicians                                                 | AIOPS / FAC / MON     | High     | Hard       |
| 20  | Compare supply temperature set-points vs actual readings.       | Facility Admin / Technicians                                                 | FAC / MON             | Medium   | Medium     |
| 21  | Show total energy consumption per room.                         | Facility Admin / Technicians                                                 | ENERGY / FAC          | High     | Medium     |
| 22  | Plot PUE trend for the last 7 days.                             | Facility Admin / Technicians, System Designers / Architects, HPC Researchers | ENERGY                | High     | Medium     |
| 23  | Compute total CRAC power (Logics: Tot_cdz).                     | Facility Admin / Technicians                                                 | ENERGY / FAC          | High     | Medium     |
| 24  | Compare ICT vs auxiliary power consumption.                     | Facility Admin / Technicians, System Designers / Architects                  | ENERGY / FAC          | High     | Medium     |
| 25  | Show voltage and current imbalance across phases.               | Facility Admin / Technicians                                                 | FAC / MON             | High     | Medium     |
| 26  | Which electrical panels report abnormal current draw?           | Facility Admin / Technicians                                                 | AIOPS / FAC / MON     | High     | Medium     |
| 27  | Display power factor (Fattore di potenza) trend.                | Facility Admin / Technicians                                                 | ENERGY / FAC          | Medium   | Medium     |
| 28  | Report total power per rack group.                              | Facility Admin / Technicians, System Admin                                   | ENERGY / FAC          | Medium   | Medium     |
| 29  | Estimate daily energy cost of the cooling system.               | Facility Admin / Technicians, System Designers / Architects                  | ENERGY                | Medium   | Medium     |
| 30  | Compare chiller and liquid cooling (Tot_chiller vs Tot_qpompe). | Facility Admin / Technicians, System Designers / Architects                  | ENERGY / FAC          | Medium   | Medium     |
| 31  | Which nodes report high CPU temperature (> 85 °C)?              | System Admin, Facility Admin / Technicians                                   | MON / ENERGY          | High     | Medium     |
| 32  | Show average fan speed trend per node.                          | System Admin                                                                 | MON                   | Medium   | Medium     |
| 33  | Identify nodes with failed or stalled fans.                     | System Admin, Facility Admin / Technicians                                   | AIOPS / MON           | High     | Medium     |
| 34  | Correlate DIMM temperature with inlet ambient.                  | HPC Researchers, System Admin                                                | AIOPS / MON / ENERGY  | Medium   | Hard       |
| 35  | List GPU temperature extremes per rack.                         | System Admin, HPC Researchers                                                | MON / ENERGY / FAC    | Medium   | Medium     |
| 36  | Detect power-supply voltage fluctuations in nodes.              | System Admin                                                                 | AIOPS / MON           | High     | Hard       |
| 37  | Which servers have persistent power anomalies?                  | System Admin                                                                 | AIOPS / MON / ENERGY  | High     | Hard       |
| 38  | Report nodes exceeding thermal violation thresholds.            | System Admin, Facility Admin / Technicians                                   | MON / ENERGY          | High     | Medium     |
| 39  | Compare node inlet vs exhaust temperature.                      | System Admin, Facility Admin / Technicians                                   | MON / ENERGY          | Medium   | Medium     |
| 40  | Detect correlation between GPU power usage and temperature.     | HPC Researchers                                                              | AIOPS / ENERGY / PERF | Medium   | Hard       |
| 41  | List all active alarms from Schneider PLC panels.               | Facility Admin / Technicians                                                 | FAC / MON             | High     | Easy       |
| 42  | Which pumps triggered fault alarms in the last hour?            | Facility Admin / Technicians                                                 | FAC / MON             | High     | Medium     |
| 43  | Display CRAC units with “Alarm On” status.                      | Facility Admin / Technicians                                                 | FAC / MON             | High     | Easy       |
| 44  | Which devices lost communication (Comlost flag)?                | Facility Admin / Technicians                                                 | FAC / MON / DATA      | High     | Easy       |
| 45  | Report critical Nagios facility alerts for today.               | System Admin, Facility Admin / Technicians                                   | MON                   | High     | Easy       |
| 46  | Identify repeated alarm patterns per device.                    | Facility Admin / Technicians, HPC Researchers                                | AIOPS / FAC / MON     | Medium   | Hard       |
| 47  | Correlate inverter alarms with pump failures.                   | Facility Admin / Technicians, HPC Researchers                                | AIOPS / FAC           | Medium   | Hard       |
| 48  | Show valve alarms and affected circuits.                        | Facility Admin / Technicians                                                 | FAC / MON             | Medium   | Medium     |
| 49  | Which PLC panels have “Allarme presente = 1”?                   | Facility Admin / Technicians                                                 | FAC / MON             | High     | Easy       |
| 50  | Summarize environmental anomalies detected overnight.           | Facility Admin / Technicians                                                 | AIOPS / FAC / MON     | High     | Medium     |
| 51  | Why did Zone B overheat yesterday?                              | Facility Admin / Technicians                                                 | AIOPS / FAC / MON     | High     | Hard       |
| 52  | Correlate UPS alert timestamps with thermal spikes.             | Facility Admin / Technicians                                                 | AIOPS / FAC           | High     | Hard       |
| 53  | Identify whether pump P102 failure caused CRAC 5 overload.      | Facility Admin / Technicians                                                 | AIOPS / FAC           | High     | Hard       |
| 54  | Was high humidity related to free-cooling malfunction?          | Facility Admin / Technicians                                                 | AIOPS / FAC           | Medium   | Hard       |
| 55  | Compare weather temperature vs inlet air over time.             | Facility Admin / Technicians, HPC Researchers                                | FAC / MON / ENERGY    | Medium   | Medium     |
| 56  | Determine root cause of low airflow in Room F.                  | Facility Admin / Technicians                                                 | AIOPS / FAC           | High     | Hard       |
| 57  | Analyze if power dips preceded cooling alarm events.            | Facility Admin / Technicians, System Admin                                   | AIOPS / FAC / ENERGY  | High     | Hard       |
| 58  | Correlate PUE degradation with chiller inefficiency.            | Facility Admin / Technicians, System Designers / Architects                  | AIOPS / ENERGY / FAC  | High     | Hard       |
| 59  | Examine voltage drop events and device downtime.                | Facility Admin / Technicians                                                 | FAC / MON             | Medium   | Medium     |
| 60  | Reconstruct timeline of alarms leading to outage #23.           | Facility Admin / Technicians                                                 | AIOPS / FAC / MON     | High     | Hard       |
| 61  | What maintenance is planned for this week?                      | Facility Admin / Technicians                                                 | FAC / DOCS            | Medium   | Easy       |
| 62  | Which pumps are due for preventive maintenance?                 | Facility Admin / Technicians                                                 | FAC / DOCS            | Medium   | Medium     |
| 63  | Show cumulative running hours for pump P103.                    | Facility Admin / Technicians                                                 | FAC / MON             | Medium   | Easy       |
| 64  | When was the last valve TY141 serviced?                         | Facility Admin / Technicians                                                 | FAC / DOCS            | Medium   | Easy       |
| 65  | Record a note for CRAC 4 filter replacement.                    | Facility Admin / Technicians                                                 | DOCS / FAC            | Medium   | Easy       |
| 66  | List equipment exceeding 5 000 h operation.                     | Facility Admin / Technicians                                                 | FAC / MON             | Medium   | Easy       |
| 67  | Track mean time between failures for pumps.                     | Facility Admin / Technicians                                                 | AIOPS / FAC           | Medium   | Medium     |
| 68  | Show next calibration date for temperature sensors.             | Facility Admin / Technicians                                                 | FAC / DOCS            | Low      | Easy       |
| 69  | Generate maintenance report for all cooling panels.             | Facility Admin / Technicians                                                 | DOCS / FAC            | Medium   | Medium     |
| 70  | List all interventions logged this month.                       | Facility Admin / Technicians                                                 | DOCS / FAC            | Medium   | Easy       |
| 71  | Show monthly CO₂ footprint for the facility.                    | Facility Admin / Technicians, System Designers / Architects                  | ENERGY                | Medium   | Medium     |
| 72  | Estimate annual energy savings from eco-mode.                   | Facility Admin / Technicians, System Designers / Architects                  | ENERGY / AIOPS        | Medium   | Medium     |
| 73  | Compute average PUE before and after optimization.              | Facility Admin / Technicians, System Designers / Architects                  | ENERGY                | Medium   | Medium     |
| 74  | Track water vs air cooling contribution to efficiency.          | Facility Admin / Technicians, System Designers / Architects                  | ENERGY / FAC          | Medium   | Medium     |
| 75  | Forecast CO₂ reduction from new chiller schedule.               | Facility Admin / Technicians, System Designers / Architects                  | AIOPS / ENERGY        | Medium   | Hard       |
| 76  | Compare energy cost per rack before/after airflow tuning.       | Facility Admin / Technicians, System Admin                                   | ENERGY / FAC          | Medium   | Medium     |
| 77  | Evaluate cooling energy recovery efficiency.                    | Facility Admin / Technicians, System Designers / Architects                  | ENERGY / FAC          | Medium   | Hard       |
| 78  | Report daily renewable power ratio (if available).              | Facility Admin / Technicians, System Designers / Architects                  | ENERGY                | Low      | Medium     |
| 79  | Show trend of energy efficiency KPIs (PUE, DCiE).               | Facility Admin / Technicians, System Designers / Architects                  | ENERGY                | Medium   | Medium     |
| 80  | Identify top 5 racks contributing to excess energy use.         | Facility Admin / Technicians, System Admin                                   | AIOPS / ENERGY / FAC  | High     | Medium     |
| 81  | List all CRAC and chiller devices in the facility.              | Facility Admin / Technicians                                                 | FAC / DOCS            | Low      | Easy       |
| 82  | Where is panel Q101 physically located?                         | Facility Admin / Technicians                                                 | FAC / ARCH            | Low      | Easy       |
| 83  | Which nodes belong to Rack-R07?                                 | System Admin, Facility Admin / Technicians                                   | ARCH / FAC            | Medium   | Easy       |
| 84  | List all sensors under maintenance status.                      | Facility Admin / Technicians                                                 | FAC / DOCS            | Medium   | Easy       |
| 85  | Retrieve mapping between pumps and valves in RDHX loop.         | Facility Admin / Technicians                                                 | FAC / DOCS / ARCH     | Medium   | Medium     |
| 86  | Identify devices currently offline or disconnected.             | Facility Admin / Technicians                                                 | FAC / MON             | High     | Easy       |
| 87  | Show inventory of all PDUs and UPS units.                       | Facility Admin / Technicians                                                 | FAC / DOCS            | Medium   | Easy       |
| 88  | List equipment added in the last 6 months.                      | Facility Admin / Technicians                                                 | FAC / DOCS            | Low      | Easy       |
| 89  | Which assets are redundant (primary/backup pairs)?              | Facility Admin / Technicians                                                 | FAC / ARCH / DOCS     | Medium   | Medium     |
| 90  | Map rack positions and associated power meters.                 | Facility Admin / Technicians, System Designers / Architects                  | FAC / ARCH            | Medium   | Medium     |
| 91  | Plot 1-year trend of room temperature averages.                 | Facility Admin / Technicians                                                 | FAC / MON             | Medium   | Medium     |
| 92  | Predict failure probability for pump P101.                      | Facility Admin / Technicians, HPC Researchers                                | AIOPS / FAC           | Medium   | Hard       |
| 93  | Forecast next thermal anomaly using past data.                  | HPC Researchers, Facility Admin / Technicians                                | AIOPS / FAC / MON     | High     | Hard       |
| 94  | Show 6-month power factor trend per panel.                      | Facility Admin / Technicians                                                 | ENERGY / FAC          | Medium   | Medium     |
| 95  | Analyze compressor utilization trend vs season.                 | Facility Admin / Technicians, HPC Researchers                                | AIOPS / FAC / MON     | Medium   | Medium     |
| 96  | Predict humidity deviation risk for the next 24 h.              | HPC Researchers, Facility Admin / Technicians                                | AIOPS / FAC           | Medium   | Hard       |
| 97  | Visualize historical PUE and correlate with weather.            | Facility Admin / Technicians, HPC Researchers                                | ENERGY / FAC          | Medium   | Medium     |
| 98  | Estimate component degradation rate from runtime hours.         | HPC Researchers, Facility Admin / Technicians                                | AIOPS / FAC           | Medium   | Hard       |
| 99  | Detect repeating weekly patterns in power usage.                | HPC Researchers, Facility Admin / Technicians                                | AIOPS / ENERGY        | Medium   | Medium     |
| 100 | Predict which CRAC may require servicing soon.                  | HPC Researchers, Facility Admin / Technicians                                | AIOPS / FAC           | High     | Hard       |
| 1   | List all jobs that exceeded their walltime limits in 2024.           | System Admin, HPC Researchers                     | JOB / DEBUG          | Medium   | Easy       |
| 2   | Which jobs had the longest queue waiting times this month?           | System Admin, HPC Researchers                     | JOB / PERF           | Medium   | Easy       |
| 3   | Show the average GPU utilization per job for my last 20 submissions. | Normal HPC User, HPC Researchers                  | MON / PERF / JOB     | High     | Medium     |
| 4   | Correlate job runtime with allocated nodes across all users.         | HPC Researchers, System Admin                     | JOB / PERF / MON     | High     | Medium     |
| 5   | Identify failed jobs with non-zero exit codes.                       | System Admin, Normal HPC User                     | JOB / DEBUG          | High     | Easy       |
| 6   | Compare performance of two job scripts using identical input data.   | Normal HPC User, HPC Researchers                  | PERF / JOB           | Medium   | Medium     |
| 7   | Show distribution of job durations for the past year.                | System Admin, HPC Researchers                     | JOB / PERF           | Medium   | Easy       |
| 8   | Detect jobs that underutilized allocated GPUs.                       | System Admin, HPC Researchers                     | PERF / MON / JOB     | High     | Medium     |
| 9   | Estimate average power consumption per job partition.                | HPC Researchers, System Admin                     | ENERGY / JOB         | Medium   | Medium     |
| 10  | Find jobs that ran on overheated nodes.                              | System Admin, HPC Researchers                     | ENERGY / MON / JOB   | High     | Medium     |
| 11  | Profile CPU vs GPU utilization trends over the last week.            | HPC Researchers, System Admin                     | MON / PERF           | High     | Medium     |
| 12  | Identify CPU-bound versus memory-bound jobs.                         | HPC Researchers, Normal HPC User                  | PERF / MON           | High     | Medium     |
| 13  | Compute job-level I/O bottlenecks from Lustre metrics.               | System Admin, HPC Researchers                     | DATA / PERF          | High     | Hard       |
| 14  | Plot correlation between GPU temperature and utilization.            | HPC Researchers                                   | ENERGY / PERF / MON  | Medium   | Medium     |
| 15  | Analyze scaling efficiency for MPI jobs with more than 128 nodes.    | HPC Researchers, System Admin                     | PERF / JOB           | Medium   | Hard       |
| 16  | Compare runtime variability between partitions.                      | HPC Researchers, System Admin                     | JOB / PERF           | Medium   | Medium     |
| 17  | Identify top 10 nodes with highest average load.                     | System Admin                                      | MON / PERF           | High     | Easy       |
| 18  | Detect network congestion events in interconnect metrics.            | System Admin, HPC Researchers                     | MON / PERF           | High     | Hard       |
| 19  | Show average SM clock frequency deviation for GPUs.                  | System Admin, HPC Researchers                     | MON / PERF           | Medium   | Medium     |
| 20  | Quantify performance drift across software updates.                  | HPC Researchers, System Admin                     | PERF / DOCS / MON    | Medium   | Hard       |
| 21  | Show CPU, memory, and GPU utilization per node for last 48 hours.    | System Admin, HPC Researchers                     | MON / PERF           | High     | Medium     |
| 22  | Detect anomalies in node power usage using IPMI data.                | System Admin, HPC Researchers                     | AIOPS / ENERGY / MON | High     | Hard       |
| 23  | Compare ambient vs internal rack temperatures.                       | Facility Admin, System Admin                      | FAC / MON / ENERGY   | Medium   | Medium     |
| 24  | Correlate memory errors (ECC) with system reboots.                   | System Admin, HPC Researchers                     | MON / AIOPS          | High     | Hard       |
| 25  | Visualize thermal violation frequency per GPU.                       | System Admin, HPC Researchers                     | MON / ENERGY         | Medium   | Medium     |
| 26  | Track NVLink CRC error rates over time.                              | System Admin, HPC Researchers                     | MON / PERF           | Medium   | Medium     |
| 27  | Show time series of fan speeds and temperatures for rack F2.         | Facility Admin, System Admin                      | FAC / MON            | Medium   | Medium     |
| 28  | Identify periods of excessive GPU throttling.                        | System Admin, HPC Researchers                     | MON / PERF / ENERGY  | High     | Medium     |
| 29  | Compute average node uptime from Ganglia and Nagios.                 | System Admin                                      | MON                  | Medium   | Easy       |
| 30  | Detect long-term drift in cluster utilization.                       | HPC Researchers, System Admin                     | AIOPS / MON / PERF   | High     | Hard       |
| 31  | Estimate total IT energy consumption per month.                      | Facility Admin, System Admin                      | ENERGY               | Medium   | Medium     |
| 32  | Compute PUE trend of the facility for 2023–2024.                     | Facility Admin, System Designers, HPC Researchers | ENERGY / FAC         | High     | Medium     |
| 33  | Correlate compute load with cooling energy usage.                    | HPC Researchers, Facility Admin                   | ENERGY / FAC / AIOPS | High     | Hard       |
| 34  | Identify jobs contributing most to cluster energy peaks.             | HPC Researchers, System Admin                     | ENERGY / JOB         | Medium   | Medium     |
| 35  | Calculate energy-per-job normalized by runtime.                      | HPC Researchers, System Admin                     | ENERGY / JOB / PERF  | Medium   | Medium     |
| 36  | Generate energy efficiency ranking per partition.                    | HPC Researchers, System Admin                     | ENERGY / PERF        | Medium   | Medium     |
| 37  | Estimate power cost of my last 10 SLURM jobs.                        | Normal HPC User, HPC Researchers                  | ENERGY / JOB         | Medium   | Easy       |
| 38  | Detect energy inefficiencies during low utilization periods.         | HPC Researchers, Facility Admin                   | ENERGY / AIOPS       | Medium   | Hard       |
| 39  | Correlate CPU and GPU power with ambient temperature.                | HPC Researchers, System Admin                     | ENERGY / MON / AIOPS | Medium   | Hard       |
| 40  | Identify nodes with persistently high power draw.                    | System Admin, Facility Admin                      | ENERGY / MON         | High     | Medium     |
| 41  | Show temperature difference between supply and return air.           | Facility Admin                                    | FAC / MON            | Medium   | Easy       |
| 42  | Correlate CRAC fan speed with room humidity.                         | Facility Admin                                    | FAC / MON            | Medium   | Medium     |
| 43  | Compute chiller power load distribution over 24 hours.               | Facility Admin                                    | ENERGY / FAC         | Medium   | Medium     |
| 44  | Detect abnormal flow rate readings in Schneider PLC data.            | Facility Admin                                    | AIOPS / FAC / MON    | High     | Hard       |
| 45  | Compare liquid vs air cooling energy efficiency.                     | System Designers, Facility Admin                  | ENERGY / FAC         | Medium   | Medium     |
| 46  | Identify pumps with excessive runtime hours.                         | Facility Admin                                    | FAC / MON            | Medium   | Easy       |
| 47  | Find temperature outliers in RDHx panels.                            | Facility Admin                                    | FAC / MON            | Medium   | Medium     |
| 48  | Estimate cooling system energy per compute watt.                     | Facility Admin, HPC Researchers                   | ENERGY / FAC         | Medium   | Hard       |
| 49  | Track panel alarms and inverter fault occurrences.                   | Facility Admin                                    | FAC / MON            | Medium   | Medium     |
| 50  | Detect synchronization errors between redundant cooling panels.      | Facility Admin                                    | AIOPS / FAC          | High     | Hard       |
| 51  | Compute I/O throughput trends during high-load periods.              | System Admin, HPC Researchers                     | DATA / PERF          | High     | Medium     |
| 52  | Detect file systems nearing full capacity.                           | System Admin                                      | DATA / MON           | High     | Easy       |
| 53  | Correlate job I/O patterns with Lustre bandwidth.                    | HPC Researchers, System Admin                     | DATA / PERF / JOB    | Medium   | Medium     |
| 54  | Identify peak data transfer times across nodes.                      | System Admin                                      | DATA / MON           | Medium   | Medium     |
| 55  | Compare read vs write ratios for project datasets.                   | HPC Researchers, System Admin                     | DATA / PERF          | Medium   | Medium     |
| 56  | Estimate average file size in scratch directories.                   | System Admin, Normal HPC User                     | DATA / MON           | Low      | Easy       |
| 57  | Detect repeated metadata operation failures.                         | System Admin                                      | DATA / MON / AIOPS   | Medium   | Medium     |
| 58  | Show disk usage growth rate per user.                                | System Admin                                      | DATA / MON           | Medium   | Easy       |
| 59  | Measure checkpointing frequency of large jobs.                       | HPC Researchers, System Admin                     | JOB / DATA / PERF    | Medium   | Medium     |
| 60  | Identify I/O-heavy jobs impacting shared storage.                    | System Admin, HPC Researchers                     | DATA / PERF / JOB    | High     | Medium     |
| 61  | Train anomaly detection model on multi-year temperature data.        | HPC Researchers                                   | AIOPS / FAC / MON    | Medium   | Hard       |
| 62  | Detect cooling system anomalies using sensor fusion.                 | HPC Researchers, Facility Admin                   | AIOPS / FAC          | High     | Hard       |
| 63  | Predict GPU thermal violations for next week.                        | HPC Researchers, System Admin                     | AIOPS / ENERGY / MON | Medium   | Hard       |
| 64  | Identify early-warning signals of fan failures.                      | HPC Researchers, System Admin                     | AIOPS / MON          | High     | Hard       |
| 65  | Detect power instability patterns across racks.                      | HPC Researchers, Facility Admin                   | AIOPS / ENERGY / FAC | High     | Hard       |
| 66  | Predict next occurrence of critical Nagios alerts.                   | HPC Researchers, System Admin                     | AIOPS / MON          | Medium   | Hard       |
| 67  | Forecast high-load periods based on historical job traces.           | HPC Researchers, System Admin                     | AIOPS / JOB / PERF   | Medium   | Hard       |
| 68  | Detect node-level thermal lag anomalies.                             | HPC Researchers, System Admin                     | AIOPS / ENERGY / MON | Medium   | Hard       |
| 69  | Generate dataset for supervised anomaly detection.                   | HPC Researchers                                   | DATA / AIOPS         | Medium   | Medium     |
| 70  | Correlate anomalies with weather and facility data.                  | HPC Researchers, Facility Admin                   | AIOPS / FAC / ENERGY | Medium   | Hard       |
| 71  | Correlate weather humidity with datacenter cooling load.             | HPC Researchers, Facility Admin                   | FAC / ENERGY         | Medium   | Medium     |
| 72  | Compare outdoor temperature with CRAC return air temperature.        | Facility Admin, HPC Researchers                   | FAC / MON            | Medium   | Medium     |
| 73  | Compute correlation matrix between CPU load, power, and PUE.         | HPC Researchers                                   | ENERGY / PERF / MON  | Medium   | Medium     |
| 74  | Analyze coupling between compute and cooling zones.                  | HPC Researchers, System Designers                 | FAC / ENERGY / PERF  | Medium   | Hard       |
| 75  | Detect misalignment between IT and facility energy peaks.            | HPC Researchers, Facility Admin                   | AIOPS / ENERGY / FAC | High     | Hard       |
| 76  | Identify correlation between user job mix and cluster efficiency.    | HPC Researchers, System Admin                     | JOB / PERF           | Medium   | Medium     |
| 77  | Compare daytime vs nighttime energy usage.                           | Facility Admin, HPC Researchers                   | ENERGY / MON         | Medium   | Easy       |
| 78  | Study impact of GPU firmware updates on power metrics.               | HPC Researchers, System Admin                     | ENERGY / PERF        | Medium   | Medium     |
| 79  | Correlate system downtimes with facility alarms.                     | System Admin, Facility Admin                      | MON / FAC / AIOPS    | High     | Medium     |
| 80  | Evaluate lag between cooling reaction and compute spikes.            | HPC Researchers, Facility Admin                   | AIOPS / FAC / ENERGY | Medium   | Hard       |
| 81  | Cluster jobs based on CPU, GPU, and memory profiles.                 | HPC Researchers                                   | AIOPS / JOB / PERF   | Medium   | Hard       |
| 82  | Identify dominant job classes by resource consumption.               | HPC Researchers, System Admin                     | JOB / PERF           | Medium   | Medium     |
| 83  | Compute mean runtime per job category.                               | HPC Researchers, System Admin                     | JOB / PERF           | Medium   | Easy       |
| 84  | Analyze workload balance between CPU-only and GPU nodes.             | HPC Researchers, System Admin                     | PERF / MON           | Medium   | Medium     |
| 85  | Detect seasonal variation in job submission behavior.                | HPC Researchers, System Admin                     | AIOPS / JOB          | Low      | Medium     |
| 86  | Characterize users with most energy-efficient jobs.                  | HPC Researchers, System Admin                     | ENERGY / JOB         | Medium   | Medium     |
| 87  | Estimate carbon intensity per workload type.                         | HPC Researchers, System Designers                 | ENERGY               | Medium   | Hard       |
| 88  | Compare workload profiles before and after scheduler update.         | HPC Researchers, System Admin                     | JOB / PERF           | Medium   | Medium     |
| 89  | Visualize workload distribution across partitions.                   | System Admin, HPC Researchers                     | JOB / MON            | Medium   | Easy       |
| 90  | Detect underutilized partitions.                                     | System Admin, HPC Researchers                     | JOB / PERF / MON     | High     | Medium     |
| 91  | Recommend energy-aware scheduling strategies.                        | HPC Researchers, System Admin                     | AIOPS / ENERGY / JOB | High     | Hard       |
| 92  | Generate auto-labeled dataset for predictive maintenance.            | HPC Researchers                                   | DATA / AIOPS         | Medium   | Hard       |
| 93  | Train regression model for power prediction from job metadata.       | HPC Researchers                                   | AIOPS / ENERGY / JOB | Medium   | Hard       |
| 94  | Detect cooling inefficiencies via ML clustering.                     | HPC Researchers, Facility Admin                   | AIOPS / FAC / ENERGY | Medium   | Hard       |
| 95  | Forecast node failures using historical telemetry.                   | HPC Researchers, System Admin                     | AIOPS / MON          | High     | Hard       |
| 96  | Auto-generate reports of anomalies detected in Prometheus data.      | System Admin, HPC Researchers                     | AIOPS / DOCS / MON   | Medium   | Medium     |
| 97  | Suggest job rescheduling based on current energy price.              | HPC Researchers, System Admin                     | AIOPS / ENERGY / JOB | Medium   | Medium     |
| 98  | Compare performance of ML-based anomaly detection models.            | HPC Researchers                                   | AIOPS / PERF         | Medium   | Hard       |
| 99  | Detect abnormal job runtime using unsupervised learning.             | HPC Researchers                                   | AIOPS / JOB / PERF   | Medium   | Hard       |
| 100 | Generate explainable summary of detected anomalies.                  | HPC Researchers, System Admin                     | AIOPS / DOCS         | High     | Medium     |
| 1   | Show current CPU, GPU, and memory utilization across all partitions.                   | System Admin, HPC Researchers                     | MON / PERF            | High     | Easy       |
| 2   | What is the average GPU power usage per node over the last 24 hours?                   | System Admin, HPC Researchers                     | ENERGY / MON / PERF   | High     | Medium     |
| 3   | Compare cooling energy vs IT power for the past month.                                 | Facility Admin, System Designers                  | ENERGY / FAC / AIOPS  | High     | Medium     |
| 4   | Show nodes with the highest ambient temperature variability.                           | Facility Admin, HPC Researchers                   | MON / ENERGY / AIOPS  | Medium   | Hard       |
| 5   | Which racks have the highest power density?                                            | Facility Admin, System Designers                  | ENERGY / FAC          | High     | Medium     |
| 6   | Plot PUE trend over the past six months.                                               | Facility Admin, HPC Researchers                   | ENERGY / FAC          | High     | Medium     |
| 7   | Estimate energy efficiency (kW per TFLOPS) across system generations.                  | System Designers, HPC Researchers                 | ENERGY / PERF / ARCH  | Medium   | Hard       |
| 8   | Identify nodes with recurring ECC memory errors.                                       | System Admin, HPC Researchers                     | MON / AIOPS           | High     | Medium     |
| 9   | Correlate GPU temperature with job power consumption.                                  | HPC Researchers                                   | ENERGY / JOB / MON    | High     | Medium     |
| 10  | Compare NVLink bandwidth utilization across GPU nodes.                                 | HPC Researchers, System Admin                     | PERF / MON            | Medium   | Medium     |
| 11  | Show fan speed distributions across compute racks.                                     | System Admin, Facility Admin                      | MON / ENERGY / FAC    | Medium   | Medium     |
| 12  | Calculate average CPU thermal efficiency (Watt per °C).                                | HPC Researchers, System Designers                 | ENERGY / PERF         | Medium   | Medium     |
| 13  | Plot load averages vs system boottime trends.                                          | System Admin                                      | MON / PERF            | Medium   | Medium     |
| 14  | Identify cooling zones with abnormal return air temperature.                           | Facility Admin                                    | FAC / MON             | High     | Medium     |
| 15  | Map rack-level power usage vs chiller consumption.                                     | Facility Admin, System Designers                  | ENERGY / FAC          | Medium   | Medium     |
| 16  | Show time series of total power consumption per device from Logics.                    | Facility Admin                                    | ENERGY / FAC / MON    | Medium   | Medium     |
| 17  | Which panels report abnormal voltage fluctuations?                                     | Facility Admin                                    | FAC / MON / AIOPS     | High     | Hard       |
| 18  | Estimate total IT energy consumption for the week.                                     | Facility Admin, System Admin                      | ENERGY                | Medium   | Easy       |
| 19  | Compare power factor across all electrical panels.                                     | Facility Admin                                    | ENERGY / FAC          | Medium   | Medium     |
| 20  | Detect anomalies in CRAC compressor utilization.                                       | Facility Admin                                    | AIOPS / FAC / MON     | High     | Hard       |
| 21  | What is the efficiency difference between free cooling and mechanical cooling periods? | Facility Admin, System Designers                  | ENERGY / FAC          | Medium   | Medium     |
| 22  | Analyze correlation between outside temperature and PUE.                               | HPC Researchers, Facility Admin                   | ENERGY / FAC / AIOPS  | Medium   | Hard       |
| 23  | Show network throughput and packet error rate per switch.                              | System Admin                                      | MON / NET / PERF      | High     | Medium     |
| 24  | Which InfiniBand ports have the highest CRC error counts?                              | System Admin                                      | MON / NET             | High     | Medium     |
| 25  | Summarize total node uptime across the cluster.                                        | System Admin                                      | MON                   | Medium   | Easy       |
| 26  | Identify nodes that failed due to GPU power limit violations.                          | System Admin, HPC Researchers                     | ENERGY / MON / AIOPS  | High     | Medium     |
| 27  | Estimate average energy per completed job.                                             | HPC Researchers, System Admin                     | ENERGY / JOB          | Medium   | Easy       |
| 28  | Compare compute energy cost for GPU vs CPU workloads.                                  | HPC Researchers, System Designers                 | ENERGY / JOB / PERF   | Medium   | Medium     |
| 29  | Predict rack overheating risk using last 30 days of data.                              | HPC Researchers, Facility Admin                   | AIOPS / ENERGY / FAC  | High     | Hard       |
| 30  | Calculate total power used by RDHX pumps and valves.                                   | Facility Admin                                    | ENERGY / FAC          | Medium   | Medium     |
| 31  | Which valves or pumps show abnormal duty cycles?                                       | Facility Admin                                    | AIOPS / FAC / MON     | Medium   | Hard       |
| 32  | Show daily average supply and return water temperatures.                               | Facility Admin                                    | FAC / MON             | Medium   | Easy       |
| 33  | Correlate humidity levels with equipment reliability events.                           | Facility Admin, HPC Researchers                   | FAC / AIOPS / ENERGY  | Medium   | Medium     |
| 34  | Identify underperforming chillers based on energy usage.                               | Facility Admin                                    | ENERGY / FAC / AIOPS  | High     | Hard       |
| 35  | Estimate heat recovery potential from exhaust air.                                     | System Designers, Facility Admin                  | ENERGY / FAC          | Medium   | Medium     |
| 36  | What is the total downtime caused by cooling subsystem alarms?                         | Facility Admin                                    | FAC / MON / ALARM     | High     | Medium     |
| 37  | Compare thermal performance between CRAC units.                                        | Facility Admin                                    | FAC / MON             | Medium   | Medium     |
| 38  | Estimate network latency trends during high system load.                               | System Admin                                      | NET / PERF / MON      | Medium   | Medium     |
| 39  | Show power and temperature correlation per rack.                                       | Facility Admin, HPC Researchers                   | ENERGY / FAC / MON    | Medium   | Medium     |
| 40  | Compare efficiency across partitions with different QoS classes.                       | HPC Researchers, System Admin                     | JOB / PERF            | Medium   | Medium     |
| 41  | Evaluate GPU energy efficiency across workload types.                                  | HPC Researchers, System Admin                     | ENERGY / JOB / PERF   | Medium   | Medium     |
| 42  | Identify nodes with persistent CPU throttling.                                         | System Admin, HPC Researchers                     | MON / PERF / ENERGY   | High     | Medium     |
| 43  | Calculate thermal violation duration across all GPUs.                                  | HPC Researchers, System Admin                     | ENERGY / MON          | Medium   | Medium     |
| 44  | What is the CPU utilization distribution across nodes?                                 | System Admin                                      | MON / PERF            | High     | Easy       |
| 45  | Show the total energy consumption trend for each cluster generation.                   | System Designers, Facility Admin                  | ENERGY / MON          | Medium   | Medium     |
| 46  | Estimate TCO impact of cooling upgrades.                                               | System Designers, Facility Admin                  | ENERGY / FAC / ARCH   | Medium   | Hard       |
| 47  | Compare rack inlet and outlet temperature deltas.                                      | Facility Admin                                    | FAC / MON             | Medium   | Medium     |
| 48  | Identify imbalanced cooling airflow zones.                                             | Facility Admin                                    | FAC / MON / AIOPS     | Medium   | Hard       |
| 49  | Rank nodes by total GPU energy consumption.                                            | HPC Researchers, System Admin                     | ENERGY / MON / JOB    | Medium   | Medium     |
| 50  | Compare energy intensity between AI and CFD workloads.                                 | HPC Researchers                                   | ENERGY / JOB / PERF   | Medium   | Medium     |
| 51  | Plot total energy cost per rack over one year.                                         | Facility Admin, System Designers                  | ENERGY / FAC          | Medium   | Medium     |
| 52  | Simulate performance-per-watt curve for different load ratios.                         | HPC Researchers, System Designers                 | ENERGY / PERF / ARCH  | Medium   | Hard       |
| 53  | Which nodes experience the highest reliability violations?                             | System Admin, HPC Researchers                     | MON / AIOPS           | High     | Hard       |
| 54  | Estimate system mean time between failures (MTBF).                                     | System Admin, Facility Admin                      | AIOPS / MON           | Medium   | Hard       |
| 55  | Detect patterns of thermal runaway events.                                             | HPC Researchers, Facility Admin                   | AIOPS / ENERGY / MON  | High     | Hard       |
| 56  | Compare node fan duty cycle against inlet temperature.                                 | System Admin, HPC Researchers                     | MON / PERF / ENERGY   | Medium   | Medium     |
| 57  | Evaluate performance impact of memory temperature rise.                                | HPC Researchers                                   | PERF / MON            | Medium   | Medium     |
| 58  | Correlate CPU speed fluctuations with job performance.                                 | HPC Researchers                                   | PERF / JOB / MON      | Medium   | Medium     |
| 59  | Predict which nodes will exceed power capacity next week.                              | HPC Researchers, Facility Admin                   | AIOPS / ENERGY / MON  | High     | Hard       |
| 60  | Generate node topology map with thermal overlays.                                      | System Designers, System Admin                    | ARCH / MON / ENERGY   | Medium   | Medium     |
| 61  | Visualize energy breakdown between IT, CRAC, and pumps.                                | Facility Admin, System Designers                  | ENERGY / FAC          | Medium   | Medium     |
| 62  | Identify panels responsible for most reactive power losses.                            | Facility Admin                                    | ENERGY / FAC          | Medium   | Hard       |
| 63  | Compute daily cooling-to-compute energy ratio.                                         | Facility Admin, HPC Researchers                   | ENERGY / FAC          | Medium   | Medium     |
| 64  | Rank components by share of total data center energy use.                              | Facility Admin, System Designers                  | ENERGY / FAC          | Medium   | Medium     |
| 65  | Correlate job waiting time with energy consumption trend.                              | HPC Researchers                                   | JOB / ENERGY / PERF   | Medium   | Medium     |
| 66  | What fraction of total cluster power is consumed by GPUs?                              | HPC Researchers, System Admin                     | ENERGY / MON / JOB    | Medium   | Medium     |
| 67  | Estimate network energy footprint per job.                                             | HPC Researchers                                   | ENERGY / JOB / NET    | Medium   | Medium     |
| 68  | Compare storage power draw per TB between Lustre and Ceph.                             | System Admin, HPC Researchers                     | ENERGY / DATA / MON   | Medium   | Medium     |
| 69  | Determine optimal node mix for performance-per-watt.                                   | System Designers, HPC Researchers                 | ENERGY / ARCH / PERF  | High     | Hard       |
| 70  | Analyze voltage stability across all power panels.                                     | Facility Admin                                    | FAC / MON / ENERGY    | Medium   | Hard       |
| 71  | Estimate effect of outside humidity on cooling system load.                            | Facility Admin, HPC Researchers                   | FAC / ENERGY / AIOPS  | Medium   | Medium     |
| 72  | Calculate aggregate job throughput vs energy draw.                                     | HPC Researchers, System Admin                     | ENERGY / JOB / PERF   | Medium   | Medium     |
| 73  | Compare thermal gradient across racks over 24 hours.                                   | Facility Admin                                    | FAC / MON             | Medium   | Medium     |
| 74  | Identify outlier sensors with unrealistic readings.                                    | Facility Admin, System Admin                      | AIOPS / FAC / MON     | High     | Hard       |
| 75  | Generate efficiency dashboard for different cooling strategies.                        | Facility Admin, System Designers                  | ENERGY / FAC / DOCS   | Medium   | Medium     |
| 76  | Estimate PUE if chilled water temperature is raised by 2°C.                            | Facility Admin, System Designers                  | ENERGY / FAC          | Medium   | Medium     |
| 77  | Correlate failures with inlet temperature thresholds.                                  | HPC Researchers, Facility Admin                   | AIOPS / MON / ENERGY  | High     | Hard       |
| 78  | Assess redundancy level of current power distribution topology.                        | Facility Admin, System Designers                  | FAC / ARCH / ENERGY   | Medium   | Hard       |
| 79  | Compare utilization efficiency across compute partitions.                              | System Admin, HPC Researchers                     | JOB / PERF / MON      | Medium   | Medium     |
| 80  | Evaluate cost per watt for GPU vs CPU nodes.                                           | HPC Researchers, System Designers                 | ENERGY / PERF / JOB   | Medium   | Medium     |
| 81  | Show trends in inlet airflow pressure drop.                                            | Facility Admin                                    | FAC / MON             | Medium   | Medium     |
| 82  | Rank rooms by cooling energy efficiency.                                               | Facility Admin                                    | ENERGY / FAC          | Medium   | Medium     |
| 83  | Identify peak load hours for power and cooling systems.                                | Facility Admin                                    | ENERGY / FAC / MON    | Medium   | Easy       |
| 84  | Predict future power demand based on job trends.                                       | HPC Researchers, System Designers                 | AIOPS / ENERGY / JOB  | High     | Hard       |
| 85  | Estimate carbon footprint of data center operation.                                    | Facility Admin, System Designers, HPC Researchers | ENERGY / SUSTAIN      | Medium   | Medium     |
| 86  | Compute ratio of IT power to total facility power.                                     | Facility Admin, HPC Researchers                   | ENERGY / FAC          | Medium   | Easy       |
| 87  | Show seasonal variation in PUE.                                                        | Facility Admin, HPC Researchers                   | ENERGY / FAC / MON    | Medium   | Medium     |
| 88  | Compare average inlet temperatures across node types.                                  | Facility Admin, System Designers                  | MON / ENERGY          | Medium   | Medium     |
| 89  | Identify underused racks by average CPU utilization.                                   | System Admin, Facility Admin                      | MON / PERF            | Medium   | Easy       |
| 90  | Rank jobs by their energy intensity (kWh/job).                                         | HPC Researchers, System Admin                     | ENERGY / JOB / PERF   | Medium   | Medium     |
| 91  | Detect abnormal network behavior using Nagios metrics.                                 | System Admin                                      | NET / AIOPS / MON     | High     | Medium     |
| 92  | Simulate performance under hypothetical power constraints.                             | HPC Researchers, System Designers                 | ENERGY / PERF / ARCH  | Medium   | Hard       |
| 93  | Estimate cost savings from replacing air cooling with liquid cooling.                  | System Designers, Facility Admin                  | ENERGY / FAC / ARCH   | Medium   | Hard       |
| 94  | Generate topology-aware performance heatmap.                                           | System Designers, HPC Researchers                 | ARCH / PERF / MON     | Medium   | Hard       |
| 95  | Show node-level total_energy_consumption trend since deployment.                       | System Admin, HPC Researchers                     | ENERGY / MON          | Medium   | Medium     |
| 96  | Detect fan anomalies correlated with temperature spikes.                               | System Admin, HPC Researchers                     | AIOPS / MON / ENERGY  | Medium   | Hard       |
| 97  | Identify deviations from expected PID valve behavior.                                  | Facility Admin                                    | AIOPS / FAC           | High     | Hard       |
| 98  | Predict system aging impact on energy efficiency.                                      | HPC Researchers, System Designers                 | AIOPS / ENERGY / ARCH | Medium   | Hard       |
| 99  | Summarize hardware obsolescence risks based on sensor data.                            | System Designers, Facility Admin                  | AIOPS / ARCH / MON    | Medium   | Hard       |
| 100 | Generate design validation report integrating performance, thermal, and energy KPIs.   | System Designers, HPC Researchers                 | ARCH / DOCS / ENERGY  | High     | Hard       |
