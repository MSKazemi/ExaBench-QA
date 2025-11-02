 - How much energy is consumed by the nodes, racks, and machine over a given period of time?
 - How much energy is consumed by the cooling system (air and water) over a given period of time?
 - What is the PUE (Power Usage Effectiveness) of a machine or compute room over a given period of time?
 - How many jobs are running on a particular node over a given period of time?
 - Provide the distribution over time of the usage of resources (CPUs, GPUs, Memory) before a node fails, over a given period of time.
 - Give me the node’s resource utilization distribution when the PUE is higher than a given value.
 - Give me the node’s resource utilization distribution for a specific JobID whose job PUE is higher than a given value.
 - Give me the node’s resource utilization distribution for a specific JobID whose job power is higher than a given value.
 - Provide the node’s resource utilization (or users) distribution for all jobs whose node’s average job power is higher than a given value.
 - What are the min, max, and average temperatures when a node is in use, over a given period of time?
 - What are the min, max, and average of the derivative of temperature when a node is in use, over a given period of time?
 - What is the distribution of the temperature of a node before it fails, over a given period of time (period before failure)?
 - Provide the list of failing nodes over a given period of time.
 - Give me the Job IDs whose node’s instantaneous (or average over time) power/temperature is higher than a given threshold.
 - What is the position of node X?
 - How many racks are there in an HPC system X?
 - Which nodes are part of the rack X?
 - How many HPC systems do we have?
 - Give me a list of users who submitted jobs in a specified time period.
 - Give me a list of jobs submitted by the user X in a specified time period.
 - Give me a list of jobs submitted in a specified time period.
 - Which user submitted job X?
 - Give details of job X.
 - How many jobs were running in a specified time period?
 - How many jobs had a time duration above a certain value?
 - Which user submitted jobs during a specified period?
 - How many jobs did a user U submit on a compute node N in a specified period?
 - Which users belong to a group G?
 - What is the power consumption of the node X in a specified time period?
 - What is the power consumption of the rack X in a specified time period?
 - What is the max/min/avg recorded metric X for compute node N from T1 to T2?
 - What is the max/min/avg recorded metric X for rack R today?
 - What is the max/min/avg recorded metric X for Job J?
 - Can you tell me the list of compute nodes that had temperatures higher than normal in a specified time period?
 - Please provide me the compute node N average temperature during May 2025.



## System Administrator Queries

### 🧩 Cluster-wide Performance & Utilization

1. What is the current total CPU utilization across all nodes?
2. Which nodes have the highest average CPU usage over the past 24 hours?
3. How much GPU memory is currently in use per GPU device?
4. What is the GPU utilization trend for the top 10 busiest GPUs this week?
5. How much RAM is allocated versus available in the cluster right now?
6. Which nodes are running low on free memory or swap?
7. What is the total disk usage and free space per partition across nodes?
8. What is the network traffic in/out per rack over the last hour?
9. Which nodes have the highest I/O wait percentage?
10. What are the top processes or jobs consuming the most CPU resources?


### ⚡ Power & Energy Efficiency

11. What is the total power consumption of the entire cluster from IPMI sensors?
12. How much power is used by CPUs versus GPUs in each node?
13. Which racks have the highest power draw?
14. What is the data center’s total IT power consumption (Logics plugin)?
15. What is the total power used by CRACs, chillers, and pumps (Logics)?
16. What is the Power Usage Effectiveness (PUE) trend for the past week?
17. Which nodes show abnormal increases in power usage compared to average?
18. How much energy (kWh) was consumed by the IT equipment in the last 24 hours?
19. What is the correlation between node power consumption and CPU load?
20. Are there any nodes exceeding their configured power limits?


### 🌡️ Thermal & Cooling Analysis

21. What are the inlet (ambient) temperatures per node from IPMI?
22. Which nodes show high GPU or DIMM temperatures?
23. How does node temperature correlate with power consumption?
24. What is the current return and supply air temperature from Vertiv units?
25. Which CRAC units are operating at maximum compressor utilization?
26. What is the temperature delta between supply and return air across all units?
27. What is the liquid cooling flow rate in each Schneider RDHx circuit?
28. Which pumps or valves in the cooling system report alarms or faults?
29. How balanced are the temperatures between different cooling zones?
30. What are the outdoor weather temperature and humidity, and how do they affect inlet temperatures?


### 🧠 Job Scheduling & Resource Efficiency

31. How many jobs are currently running, pending, or failed in SLURM?
32. Which partitions have the highest average waiting time for jobs?
33. What is the 95th percentile of job waiting time across all QoS classes?
34. Which users or groups consume the most resources (CPU/GPU hours)?
35. What is the overall cluster CPU/GPU allocation efficiency?
36. Which jobs consumed the most energy per run?
37. What is the distribution of job durations by QoS and partition?
38. How many nodes are currently idle or down?
39. What is the average node utilization across the past week?
40. Which jobs frequently fail or exit with non-zero codes?


### 🧱 Reliability, Alarms & System Health

41. Which nodes have active Nagios alarms?
42. What are the most common critical service alerts from Nagios this month?
43. Are there any BMC or GPU memory ECC errors reported recently?
44. Which nodes experienced XID GPU errors or thermal violations?
45. What percentage of nodes are in maintenance or drained state?
46. Which cooling pumps or valves triggered alarms in Schneider PLC logs?
47. What is the number of communication failures (Comlost) in Logics data?
48. Are all network switches and storage systems reported healthy by Nagios?
49. Which nodes have rebooted within the last 24 hours?
50. What is the overall cluster availability and health status summary?


### 🧠 Predictive & Anomaly-Driven Queries

1. Detect nodes showing abnormal correlation between power and temperature.
2. Identify GPUs whose utilization dropped below 10 % for more than 6 hours.
3. Find nodes where CPU temperature increased faster than 10 °C in 5 minutes.
4. Detect outliers in power consumption versus average node group trend.
5. Which GPUs reported repeated ECC errors in the past week?
6. List nodes with more than 5 unexpected reboots this month.
7. Highlight cooling units whose compressor utilization deviates > 20 % from peers.
8. Predict next 24 hours power consumption using last 7 days trend.
9. Which nodes show an unusual pattern of memory errors correlated with ambient temperature?
10. Detect pumps or valves in Schneider data that oscillate abnormally (PID instability).


### ⚙️ Capacity & Resource Planning

11. What is the average CPU utilization trend over the last 30 days per partition?
12. How much GPU capacity remains unused per QoS class?
13. Forecast when current storage utilization will reach 90 % capacity.
14. Which racks consistently operate near power limit thresholds?
15. What is the trend of job submission rate per user group?
16. Which partitions experience the longest cumulative queue times?
17. What is the ratio of idle vs. allocated nodes across the past month?
18. How many GPUs are typically idle during off-peak hours?
19. How balanced is job distribution across nodes and racks?
20. What fraction of nodes remain powered on but unused for more than 12 hours daily?


### 🌡️ Energy & Thermal Optimization

21. Compute PUE every 15 minutes and detect degradation periods.
22. Correlate ambient outdoor temperature with total cooling power consumption.
23. Identify CRAC units with the poorest temperature regulation stability.
24. What is the efficiency difference between air-cooled and liquid-cooled racks?
25. Compute average energy per job and identify energy-intensive workloads.
26. Estimate potential energy savings from consolidating low-load nodes.
27. Compare total IT energy (Logics) with IPMI-reported node energy to find discrepancies.
28. Identify nodes frequently exceeding 85 % of their power limit.
29. Compute cooling energy per degree of inlet temperature reduction.
30. Estimate CO₂ emissions based on total energy and regional carbon intensity.


### 📊 System Reliability & Health Diagnostics

31. Which fans in IPMI data show decreased RPM trends over time?
32. List all nodes with “CRITICAL” state in Nagios for more than 1 hour.
33. Detect jobs that failed repeatedly due to hardware or thermal issues.
34. Which nodes have persistent “down” or “drained” state in SLURM?
35. Identify power supplies (psX) showing unstable voltage or current readings.
36. What percentage of cooling alarms were unresolved within 30 minutes?
37. List devices with missing data (Comlost = 1) in Logics telemetry.
38. Which network switches reported hardware faults most often?
39. How many ECC errors per GPU occurred before a job crash?
40. Which nodes exhibit recurring BMC or BIOS sensor failures?


### 🌦️ Environmental Awareness & Correlation

41. How does outdoor humidity affect data center inlet temperature?
42. Identify days when strong wind correlated with lower inlet temperature.
43. Compare weather pressure trends with CRAC static pressure values.
44. Compute daily dew-point average and correlate with humidity alarms.
45. Determine if weather temperature anomalies affect power usage efficiency.


### 📈 Operational Efficiency & Insights

46. Rank top 10 users by energy cost per job.
47. Identify jobs that consumed most GPU time but least CPU utilization.
48. Compute average waiting-time penalty per partition vs. resource availability.
49. Show trend of maintenance alarms per subsystem over the past quarter.
50. Generate summary of total uptime percentage for compute, cooling, and power systems.




## Normal HPC User Queries

### 🧩 Job & Queue Management

1. What jobs are currently running under my user ID?
2. Show me all my pending jobs and their waiting times.
3. How long did job 458932 take to complete?
4. What is the status of job 458932?
5. Which partition did my job 458932 run on?
6. How many nodes were allocated to job 458932?
7. What is the average waiting time in the queue today?
8. Which queue has the shortest average waiting time?
9. How many jobs failed in the last 24 hours?
10. What are the top users by number of submitted jobs this week?

---

### ⚙️ Performance & Resource Utilization

11. Show CPU utilization for my last five jobs.
12. What was the GPU utilization for job 458932?
13. Plot memory usage over time for job 458932.
14. What was the peak GPU temperature during my job?
15. Show CPU idle percentage across all my allocated nodes.
16. What is the average CPU speed (MHz) for my current job nodes?
17. How many GPUs were active during my last run?
18. Did any of my jobs exceed the memory limit?
19. Which nodes showed the highest load during my simulation?
20. What is the total GPU energy consumption per job?

---

### 💾 Data & Storage

21. How much storage space am I currently using?
22. List my largest files in the scratch directory.
23. What percentage of my project quota is used?
24. Which directory has the highest disk usage?
25. Show total free disk space on my allocated nodes.
26. Has my job ever failed due to insufficient disk space?
27. Compare disk usage between home and project directories.
28. When was my quota last exceeded?
29. How many files were modified in my scratch directory this week?
30. List files older than 30 days to clean up.

---

### 🧮 Software & Environment

31. Which modules are currently loaded in my session?
32. What version of Python is available on the system?
33. Load TensorFlow with CUDA support.
34. Is CUDA 12 available on this cluster?
35. Show all installed scientific libraries related to MPI.
36. Check if my environment has OpenBLAS enabled.
37. Which compiler version is recommended for my code?
38. How can I load GROMACS with GPU acceleration?
39. Display all available software modules related to machine learning.
40. What MPI implementations are currently supported?

---

### 🧠 Debugging & Troubleshooting

41. Why did my last job fail?
42. Show me the error log for job 458932.
43. Which node caused my job failure?
44. Did my job exceed the time limit?
45. What was the reason my job was requeued?
46. Were there any thermal alerts on nodes used by my job?
47. Did the scheduler report resource contention for my job?
48. Show exit code and state reason for failed jobs.
49. What percentage of my jobs finished successfully this month?
50. Suggest possible causes for MPI rank errors.

---

### 🧰 Monitoring & Runtime Metrics

51. Show current CPU utilization across the cluster.
52. What is the average GPU utilization in my partition?
53. Display node temperature trends for my active jobs.
54. Plot CPU and memory usage trends during my simulation.
55. Which nodes are reporting high ambient temperature?
56. Show total energy usage for my jobs today.
57. How many running processes are currently active per node?
58. What was the network throughput for my job 458932?
59. Display swap memory usage on my allocated nodes.
60. How many jobs are running on nodes with fan speed alerts?

---

### ⚡ GPU & Accelerator Insights

61. Show GPU power consumption over time for my last job.
62. What was the maximum GPU temperature reached today?
63. Display GPU ECC error counts in my allocated nodes.
64. Are there any GPUs with low utilization?
65. Compare GPU clock speeds across nodes used by my job.
66. What is the average GPU memory usage across my active jobs?
67. Did any GPU exceed its power management limit?
68. Show NVLink error counts on my job nodes.
69. How much total GPU memory is available in my partition?
70. Show GPU thermal violation events for my jobs.

---

### 🌡️ Environment & Energy Awareness

71. What is the current PUE of the cluster?
72. How much total IT power is consumed right now?
73. Show energy usage breakdown between compute and cooling.
74. What was the average inlet temperature during my job?
75. Display total power consumption per rack.
76. How has cluster energy usage changed over the past week?
77. Which CRAC units have the highest compressor utilization?
78. Show return air temperature trends for the cooling units.
79. Display humidity levels in the machine room.
80. What is the difference between supply and return flow temperatures?

---

### ☁️ Weather & Facility Context

81. What is the current outdoor temperature near the facility?
82. How does outside humidity affect cooling energy use?
83. Show wind speed during the last peak cooling period.
84. Was there any correlation between external temperature and job failure rate?
85. How does external pressure vary during high compute load hours?

---

### 🧩 Job Profiling & Analysis

86. Show top 10 jobs by total runtime this month.
87. Which job had the highest energy consumption?
88. What are the average CPU and GPU utilization per user?
89. Compare job runtime and waiting time for my recent jobs.
90. Generate performance summary for all my completed jobs.

---

### 🤖 Automation & Assistance

91. Schedule a daily report of my job statistics.
92. Notify me when a job exceeds its time limit.
93. Automatically delete temporary files after job completion.
94. Generate a weekly performance summary of my workloads.
95. Alert me if GPU utilization drops below 20%.

---

### 🔐 Access, Sharing, and Collaboration

96. Share my project directory with user “alice”.
97. Check permissions for the folder `/project/shared`.
98. Add SSH key to enable remote job submission.
99. Who has access to my project folder?
100. List collaborators with active jobs in the same partition.

---


    
## Facility Admin / Technician

### 🔹 Environmental Monitoring (MON)

1. Show the temperature map for each datacenter zone.
2. Which racks exceed 28 °C inlet temperature?
3. List humidity readings for all rooms.
4. What is the average airflow rate per rack?
5. Compare inlet vs outlet temperature across zones.
6. Show temperature difference between supply and return air.
7. Detect racks with unstable thermal gradients.
8. Report average ambient temperature for the past 24 h.
9. Which areas have humidity below 35 %?
10. Identify hotspots detected by IPMI sensors today.


### 🔹 Cooling System Operations (COOL)

11. Compare CRAC unit efficiency (Vertiv metrics) by power usage.
12. Show compressor utilization trend for all CRACs.
13. Which CRAC units have Free-Cooling mode active?
14. Report supply and return air temperatures per CRAC.
15. Correlate fan speed with return air temperature.
16. Detect pressure drop anomalies in filter sensors.
17. Which CRAC units have humidity control enabled?
18. Compute average Free-Cooling fluid temperature.
19. Identify underperforming CRACs with low cooling delta.
20. Compare supply temperature set-points vs actual readings.


### 🔹 Power & Energy Management (ENERGY)

21. Show total energy consumption per room.
22. Plot PUE trend for the last 7 days.
23. Compute total CRAC power (Logics: Tot_cdz).
24. Compare ICT vs auxiliary power consumption.
25. Show voltage and current imbalance across phases.
26. Which electrical panels report abnormal current draw?
27. Display power factor (Fattore di potenza) trend.
28. Report total power per rack group.
29. Estimate daily energy cost of the cooling system.
30. Compare chiller and liquid cooling (Tot_chiller vs Tot_qpompe).


### 🔹 Rack & Node Health (HEALTH)

31. Which nodes report high CPU temperature (> 85 °C)?
32. Show average fan speed trend per node.
33. Identify nodes with failed or stalled fans.
34. Correlate DIMM temperature with inlet ambient.
35. List GPU temperature extremes per rack.
36. Detect power-supply voltage fluctuations in nodes.
37. Which servers have persistent power anomalies?
38. Report nodes exceeding thermal violation thresholds.
39. Compare node inlet vs exhaust temperature.
40. Detect correlation between GPU power usage and temperature.


### 🔹 Alarms & Anomaly Detection (ALARM)

41. List all active alarms from Schneider PLC panels.
42. Which pumps triggered fault alarms in the last hour?
43. Display CRAC units with “Alarm On” status.
44. Which devices lost communication (Comlost flag)?
45. Report critical Nagios facility alerts for today.
46. Identify repeated alarm patterns per device.
47. Correlate inverter alarms with pump failures.
48. Show valve alarms and affected circuits.
49. Which PLC panels have “Allarme presente = 1”?
50. Summarize environmental anomalies detected overnight.


### 🔹 Incident Response & Root-Cause Analysis (IRCA)

51. Why did Zone B overheat yesterday?
52. Correlate UPS alert timestamps with thermal spikes.
53. Identify whether pump P102 failure caused CRAC 5 overload.
54. Was high humidity related to free-cooling malfunction?
55. Compare weather temperature vs inlet air over time.
56. Determine root cause of low airflow in Room F.
57. Analyze if power dips preceded cooling alarm events.
58. Correlate PUE degradation with chiller inefficiency.
59. Examine voltage drop events and device downtime.
60. Reconstruct timeline of alarms leading to outage #23.


### 🔹 Maintenance Scheduling & Logs (MAINT)

61. What maintenance is planned for this week?
62. Which pumps are due for preventive maintenance?
63. Show cumulative running hours for pump P103.
64. When was the last valve TY141 serviced?
65. Record a note for CRAC 4 filter replacement.
66. List equipment exceeding 5 000 h operation.
67. Track mean time between failures for pumps.
68. Show next calibration date for temperature sensors.
69. Generate maintenance report for all cooling panels.
70. List all interventions logged this month.


### 🔹 Sustainability & Efficiency Analytics (SUSTAIN)

71. Show monthly CO₂ footprint for the facility.
72. Estimate annual energy savings from eco-mode.
73. Compute average PUE before and after optimization.
74. Track water vs air cooling contribution to efficiency.
75. Forecast CO₂ reduction from new chiller schedule.
76. Compare energy cost per rack before/after airflow tuning.
77. Evaluate cooling energy recovery efficiency.
78. Report daily renewable power ratio (if available).
79. Show trend of energy efficiency KPIs (PUE, DCiE).
80. Identify top 5 racks contributing to excess energy use.


### 🔹 Asset & Inventory Management (ASSET)

81. List all CRAC and chiller devices in the facility.
82. Where is panel Q101 physically located?
83. Which nodes belong to Rack-R07?
84. List all sensors under maintenance status.
85. Retrieve mapping between pumps and valves in RDHX loop.
86. Identify devices currently offline or disconnected.
87. Show inventory of all PDUs and UPS units.
88. List equipment added in the last 6 months.
89. Which assets are redundant (primary/backup pairs)?
90. Map rack positions and associated power meters.


### 🔹 Historical Trend & Predictive Analysis (TREND)

91. Plot 1-year trend of room temperature averages.
92. Predict failure probability for pump P101.
93. Forecast next thermal anomaly using past data.
94. Show 6-month power factor trend per panel.
95. Analyze compressor utilization trend vs season.
96. Predict humidity deviation risk for the next 24 h.
97. Visualize historical PUE and correlate with weather.
98. Estimate component degradation rate from runtime hours.
99. Detect repeating weekly patterns in power usage.
100. Predict which CRAC may require servicing soon.

---


## HPC Researcher Queries

### 🔹 Job & Workflow Analysis

1. List all jobs that exceeded their walltime limits in 2024.
2. Which jobs had the longest queue waiting times this month?
3. Show the average GPU utilization per job for my last 20 submissions.
4. Correlate job runtime with allocated nodes across all users.
5. Identify failed jobs with non-zero exit codes.
6. Compare performance of two job scripts using identical input data.
7. Show distribution of job durations for the past year.
8. Detect jobs that underutilized allocated GPUs.
9. Estimate average power consumption per job partition.
10. Find jobs that ran on overheated nodes.


### 🔹 Performance & Optimization

11. Profile CPU vs GPU utilization trends over the last week.
12. Identify CPU-bound versus memory-bound jobs.
13. Compute job-level I/O bottlenecks from Lustre metrics.
14. Plot correlation between GPU temperature and utilization.
15. Analyze scaling efficiency for MPI jobs with more than 128 nodes.
16. Compare runtime variability between partitions.
17. Identify top 10 nodes with highest average load.
18. Detect network congestion events in interconnect metrics.
19. Show average SM clock frequency deviation for GPUs.
20. Quantify performance drift across software updates.


### 🔹 Monitoring & Observability

21. Show CPU, memory, and GPU utilization per node for last 48 hours.
22. Detect anomalies in node power usage using IPMI data.
23. Compare ambient vs internal rack temperatures.
24. Correlate memory errors (ECC) with system reboots.
25. Visualize thermal violation frequency per GPU.
26. Track NVLink CRC error rates over time.
27. Show time series of fan speeds and temperatures for rack F2.
28. Identify periods of excessive GPU throttling.
29. Compute average node uptime from Ganglia and Nagios.
30. Detect long-term drift in cluster utilization.


### 🔹 Energy & Sustainability

31. Estimate total IT energy consumption per month.
32. Compute PUE trend of the facility for 2023–2024.
33. Correlate compute load with cooling energy usage.
34. Identify jobs contributing most to cluster energy peaks.
35. Calculate energy-per-job normalized by runtime.
36. Generate energy efficiency ranking per partition.
37. Estimate power cost of my last 10 SLURM jobs.
38. Detect energy inefficiencies during low utilization periods.
39. Correlate CPU and GPU power with ambient temperature.
40. Identify nodes with persistently high power draw.


### 🔹 Facility & Cooling Systems

41. Show temperature difference between supply and return air.
42. Correlate CRAC fan speed with room humidity.
43. Compute chiller power load distribution over 24 hours.
44. Detect abnormal flow rate readings in Schneider PLC data.
45. Compare liquid vs air cooling energy efficiency.
46. Identify pumps with excessive runtime hours.
47. Find temperature outliers in RDHx panels.
48. Estimate cooling system energy per compute watt.
49. Track panel alarms and inverter fault occurrences.
50. Detect synchronization errors between redundant cooling panels.


### 🔹 Data & Storage Management

51. Compute I/O throughput trends during high-load periods.
52. Detect file systems nearing full capacity.
53. Correlate job I/O patterns with Lustre bandwidth.
54. Identify peak data transfer times across nodes.
55. Compare read vs write ratios for project datasets.
56. Estimate average file size in scratch directories.
57. Detect repeated metadata operation failures.
58. Show disk usage growth rate per user.
59. Measure checkpointing frequency of large jobs.
60. Identify I/O-heavy jobs impacting shared storage.


### 🔹 Anomaly Detection & Predictive Modeling

61. Train anomaly detection model on multi-year temperature data.
62. Detect cooling system anomalies using sensor fusion.
63. Predict GPU thermal violations for next week.
64. Identify early-warning signals of fan failures.
65. Detect power instability patterns across racks.
66. Predict next occurrence of critical Nagios alerts.
67. Forecast high-load periods based on historical job traces.
68. Detect node-level thermal lag anomalies.
69. Generate dataset for supervised anomaly detection.
70. Correlate anomalies with weather and facility data.


### 🔹 Cross-Domain Correlation Studies

71. Correlate weather humidity with datacenter cooling load.
72. Compare outdoor temperature with CRAC return air temperature.
73. Compute correlation matrix between CPU load, power, and PUE.
74. Analyze coupling between compute and cooling zones.
75. Detect misalignment between IT and facility energy peaks.
76. Identify correlation between user job mix and cluster efficiency.
77. Compare daytime vs nighttime energy usage.
78. Study impact of GPU firmware updates on power metrics.
79. Correlate system downtimes with facility alarms.
80. Evaluate lag between cooling reaction and compute spikes.


### 🔹 HPC Workload Characterization

81. Cluster jobs based on CPU, GPU, and memory profiles.
82. Identify dominant job classes by resource consumption.
83. Compute mean runtime per job category.
84. Analyze workload balance between CPU-only and GPU nodes.
85. Detect seasonal variation in job submission behavior.
86. Characterize users with most energy-efficient jobs.
87. Estimate carbon intensity per workload type.
88. Compare workload profiles before and after scheduler update.
89. Visualize workload distribution across partitions.
90. Detect underutilized partitions.


### 🔹 Automation & AIOps

91. Recommend energy-aware scheduling strategies.
92. Generate auto-labeled dataset for predictive maintenance.
93. Train regression model for power prediction from job metadata.
94. Detect cooling inefficiencies via ML clustering.
95. Forecast node failures using historical telemetry.
96. Auto-generate reports of anomalies detected in Prometheus data.
97. Suggest job rescheduling based on current energy price.
98. Compare performance of ML-based anomaly detection models.
99. Detect abnormal job runtime using unsupervised learning.
100. Generate explainable summary of detected anomalies.

---

## HPC System Designer / Architect Queries

1. Show current CPU, GPU, and memory utilization across all partitions.
2. What is the average GPU power usage per node over the last 24 hours?
3. Compare cooling energy vs IT power for the past month.
4. Show nodes with the highest ambient temperature variability.
5. Which racks have the highest power density?
6. Plot PUE trend over the past six months.
7. Estimate energy efficiency (kW per TFLOPS) across system generations.
8. Identify nodes with recurring ECC memory errors.
9. Correlate GPU temperature with job power consumption.
10. Compare NVLink bandwidth utilization across GPU nodes.
11. Show fan speed distributions across compute racks.
12. Calculate average CPU thermal efficiency (Watt per °C).
13. Plot load averages vs system boottime trends.
14. Identify cooling zones with abnormal return air temperature.
15. Map rack-level power usage vs chiller consumption.
16. Show time series of total power consumption per device from Logics.
17. Which panels report abnormal voltage fluctuations?
18. Estimate total IT energy consumption for the week.
19. Compare power factor across all electrical panels.
20. Detect anomalies in CRAC compressor utilization.
21. What is the efficiency difference between free cooling and mechanical cooling periods?
22. Analyze correlation between outside temperature and PUE.
23. Show network throughput and packet error rate per switch.
24. Which InfiniBand ports have the highest CRC error counts?
25. Summarize total node uptime across the cluster.
26. Identify nodes that failed due to GPU power limit violations.
27. Estimate average energy per completed job.
28. Compare compute energy cost for GPU vs CPU workloads.
29. Predict rack overheating risk using last 30 days of data.
30. Calculate total power used by RDHX pumps and valves.
31. Which valves or pumps show abnormal duty cycles?
32. Show daily average supply and return water temperatures.
33. Correlate humidity levels with equipment reliability events.
34. Identify underperforming chillers based on energy usage.
35. Estimate heat recovery potential from exhaust air.
36. What is the total downtime caused by cooling subsystem alarms?
37. Compare thermal performance between CRAC units.
38. Estimate network latency trends during high system load.
39. Show power and temperature correlation per rack.
40. Compare efficiency across partitions with different QoS classes.
41. Evaluate GPU energy efficiency across workload types.
42. Identify nodes with persistent CPU throttling.
43. Calculate thermal violation duration across all GPUs.
44. What is the CPU utilization distribution across nodes?
45. Show the total energy consumption trend for each cluster generation.
46. Estimate TCO impact of cooling upgrades.
47. Compare rack inlet and outlet temperature deltas.
48. Identify imbalanced cooling airflow zones.
49. Rank nodes by total GPU energy consumption.
50. Compare energy intensity between AI and CFD workloads.
51. Plot total energy cost per rack over one year.
52. Simulate performance-per-watt curve for different load ratios.
53. Which nodes experience the highest reliability violations?
54. Estimate system mean time between failures (MTBF).
55. Detect patterns of thermal runaway events.
56. Compare node fan duty cycle against inlet temperature.
57. Evaluate performance impact of memory temperature rise.
58. Correlate CPU speed fluctuations with job performance.
59. Predict which nodes will exceed power capacity next week.
60. Generate node topology map with thermal overlays.
61. Visualize energy breakdown between IT, CRAC, and pumps.
62. Identify panels responsible for most reactive power losses.
63. Compute daily cooling-to-compute energy ratio.
64. Rank components by share of total data center energy use.
65. Correlate job waiting time with energy consumption trend.
66. What fraction of total cluster power is consumed by GPUs?
67. Estimate network energy footprint per job.
68. Compare storage power draw per TB between Lustre and Ceph.
69. Determine optimal node mix for performance-per-watt.
70. Analyze voltage stability across all power panels.
71. Estimate effect of outside humidity on cooling system load.
72. Calculate aggregate job throughput vs energy draw.
73. Compare thermal gradient across racks over 24 hours.
74. Identify outlier sensors with unrealistic readings.
75. Generate efficiency dashboard for different cooling strategies.
76. Estimate PUE if chilled water temperature is raised by 2°C.
77. Correlate failures with inlet temperature thresholds.
78. Assess redundancy level of current power distribution topology.
79. Compare utilization efficiency across compute partitions.
80. Evaluate cost per watt for GPU vs CPU nodes.
81. Show trends in inlet airflow pressure drop.
82. Rank rooms by cooling energy efficiency.
83. Identify peak load hours for power and cooling systems.
84. Predict future power demand based on job trends.
85. Estimate carbon footprint of data center operation.
86. Compute ratio of IT power to total facility power.
87. Show seasonal variation in PUE.
88. Compare average inlet temperatures across node types.
89. Identify underused racks by average CPU utilization.
90. Rank jobs by their energy intensity (kWh/job).
91. Detect abnormal network behavior using Nagios metrics.
92. Simulate performance under hypothetical power constraints.
93. Estimate cost savings from replacing air cooling with liquid cooling.
94. Generate topology-aware performance heatmap.
95. Show node-level total_energy_consumption trend since deployment.
96. Detect fan anomalies correlated with temperature spikes.
97. Identify deviations from expected PID valve behavior.
98. Predict system aging impact on energy efficiency.
99. Summarize hardware obsolescence risks based on sensor data.
100. Generate design validation report integrating performance, thermal, and energy KPIs.

---
    
