# HPC User Query Taxonomy — Facility Admin / Technicians

You are an expert HPC architect and HPC user-experience designer.

---

## 1️⃣ Category List (High-Level Overview)

| Category | Priority | Description |
|-----------|-----------|-------------|
| 1. Facility Infrastructure Status | H | Monitor power, cooling, and environmental telemetry across racks, rooms, and zones. |
| 2. Rack-Level & Node Environmental Monitoring | H | Inspect rack temperature, humidity, airflow, IPMI readings, and fan speeds. |
| 3. Power Usage & Energy Efficiency | H | Analyze PUE, energy cost breakdown, and per-node/pod energy consumption. |
| 4. Alerts & Anomaly Detection | H | Receive and query alerts related to thermal, power, or equipment failures. |
| 5. Maintenance Scheduling & Logs | M | Track, log, and plan maintenance operations and equipment replacements. |
| 6. Hardware Asset Management | M | Manage inventory of racks, nodes, PDUs, UPS, sensors, and network switches. |
| 7. Facility Map & Spatial Visualization | L | Query and visualize spatial rack layouts, cable routes, and airflows. |
| 8. Sensor Calibration & Validation | L | Perform checks and calibrations on IPMI sensors and environmental probes. |
| 9. System Availability & Downtime Reports | H | Retrieve uptime/downtime metrics for racks, PDUs, cooling units, and UPS. |
| 10. Facility Control & Actuation | M | Trigger or schedule fan-speed adjustments, power cycling, or cooling-zone activation. |
| 11. Integration with Building Management Systems (BMS) | M | Interact with BMS APIs and query HVAC, CRAC, or UPS subsystems. |
| 12. Documentation & SOP Support | M | Access documentation for maintenance SOPs, safety guides, and escalation protocols. |
| 13. Incident Root-Cause Analysis | H | Request historical correlation across telemetry and maintenance records. |
| 14. Communication & Ticketing Integration | M | Interact with issue-tracking or helpdesk systems (e.g., ServiceNow). |
| 15. Data Retention & Compliance | L | Review logs retention, compliance constraints, and facility access control. |

---

## 2️⃣ Detailed Table Version

| Category | Description | Example Queries | Agent(s) to Fulfill Request |
|-----------|-------------|-----------------|-----------------------------|
| **Facility Infrastructure Status** | Check operational status of power, cooling, and environmental systems. | - “What is the current PUE of the HPC facility?”<br> - “Show CRAC units status in Room A.”<br> - “Are any power circuits overloaded?” | ExaSage Monitoring Agent, Facility Agent |
| **Rack-Level & Node Environmental Monitoring** | Inspect rack temperature, airflow, and IPMI metrics. | - “Show top 10 racks by temperature.”<br> - “What’s the humidity in rack R05?”<br> - “List nodes reporting thermal throttling.” | ExaSage Monitoring Agent |
| **Power Usage & Energy Efficiency** | Analyze per-rack and per-node power draw and energy consumption. | - “Compare node power usage trends over last 24h.”<br> - “Which racks consume the most energy per job?”<br> - “Generate energy efficiency report.” | Data Analytics Agent, ExaSage Monitoring Agent |
| **Alerts & Anomaly Detection** | Detect and diagnose facility-level anomalies. | - “List all active thermal anomalies.”<br> - “Was there a power spike yesterday?”<br> - “Correlate fan failure alerts with high temperatures.” | ExaSage Monitoring Agent, Data Analytics Agent |
| **Maintenance Scheduling & Logs** | Manage maintenance schedules and logs. | - “What maintenance is scheduled this week?”<br> - “Add maintenance note for CRAC unit 2.”<br> - “Show last calibration report.” | Facility Agent, Admin capabilities |
| **Hardware Asset Management** | Manage and track physical infrastructure assets. | - “List all active sensors and their firmware versions.”<br> - “Which PDUs are near end-of-life?” | Facility Agent, RAG Agent |
| **Facility Map & Spatial Visualization** | Visualize racks, sensors, and airflow patterns. | - “Show spatial layout of Room B.”<br> - “Highlight racks with abnormal temperature.” | Facility Agent, RAG Agent |
| **Sensor Calibration & Validation** | Ensure reliability of IPMI and BMC data. | - “When was the last IPMI calibration?”<br> - “Compare temperature sensors with reference probe.” | Facility Agent, ExaSage Monitoring Agent |
| **System Availability & Downtime Reports** | Track downtime and service interruptions. | - “Which cooling units were offline last week?”<br> - “Generate uptime report for the facility.” | Data Analytics Agent |
| **Facility Control & Actuation** | Control or trigger physical operations. | - “Power-cycle rack R10.”<br> - “Set fan speed in Zone C to auto mode.” | Facility Agent, Admin capabilities |
| **Integration with BMS** | Bridge facility telemetry with building systems. | - “Query BMS for HVAC status.”<br> - “Get UPS battery health from BMS feed.” | Facility Agent |
| **Documentation & SOP Support** | Provide procedural guidance. | - “How to safely replace a failed PSU?”<br> - “Show the SOP for CRAC maintenance.” | RAG Agent |
| **Incident Root-Cause Analysis** | Analyze past incidents with data correlation. | - “Why did Room B overheat on Oct 15?”<br> - “Show anomalies before UPS failure.” | Data Analytics Agent, ExaSage Monitoring Agent |
| **Communication & Ticketing Integration** | Manage facility support workflow. | - “Open a new maintenance ticket for UPS alert.”<br> - “Update ServiceNow with latest fan failure details.” | Facility Agent, RAG Agent |
| **Data Retention & Compliance** | Review security and data governance policies. | - “How long are sensor logs stored?”<br> - “Who has access to room-level telemetry?” | RAG Agent, Admin capabilities |

---

## 3️⃣ Permissions & Access Control Notes

| Access Level | Category | Notes |
|---------------|-----------|-------|
| **Public/User-Level** | Documentation, Reports, SOPs | Safe for all users; read-only. |
| **Technician Privilege** | Monitoring, Maintenance Logs, Sensor Readings | Requires facility role or read privileges on telemetry APIs. |
| **Admin Privilege** | Facility Control, Power Operations, Data Retention | Includes actuation rights; must be authenticated and audited. |
| **Sensitive Data** | Energy Cost, Access Logs | Should be protected via role-based access control (RBAC). |

Security recommendation:  
> Use fine-grained RBAC and audit trails for any command triggering **physical actuation or configuration changes**. Logging via ExaSage and Facility Agent must be mandatory.

---

## 4️⃣ Extended Example Questions Corpus (≥25)

1. “What is the power draw of Rack 12 right now?”
2. “List all sensors reporting abnormal temperature.”
3. “Show the humidity trend in Room B for the past 48 hours.”
4. “Which CRAC units are currently in maintenance mode?”
5. “When was the last UPS battery replacement?”
6. “Generate a PUE report for this month.”
7. “Are there any power distribution alarms active?”
8. “Compare energy consumption across zones.”
9. “Show racks sorted by cooling efficiency.”
10. “What caused the temperature spike yesterday evening?”
11. “Can you correlate thermal anomalies with node workloads?”
12. “Schedule maintenance for cooling unit 3 tomorrow.”
13. “Open a ticket for fan replacement in rack R07.”
14. “Retrieve airflow map for Data Room C.”
15. “Has the IPMI sensor calibration drifted recently?”
16. “Export downtime statistics for the last quarter.”
17. “List all devices nearing end of service life.”
18. “Which rack has the highest failure rate?”
19. “Display spatial layout with active alerts overlay.”
20. “Send notification to maintenance team for CRAC issue.”
21. “What’s the average energy cost per compute node?”
22. “Update the calibration log for temperature probe T-22.”
23. “Pull SOP for emergency cooling failure procedure.”
24. “Check access control violations in Room A.”
25. “Compare fan speeds vs ambient temperature trends.”

---

✅ **Summary for Intent Classification**
- Total categories: 15  
- Priorities: H (6), M (6), L (3)  
- Dominant agents: **ExaSage Monitoring**, **Facility**, **Data Analytics**, **RAG (Docs/SOPs)**  
- Access control: Mixed (Technician/Admin-heavy)

---

