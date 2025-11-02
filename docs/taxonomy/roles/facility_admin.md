# 🧠 HPC Facility Admin / Technicians

## **Primary Mission**
- Ensure reliable, safe, and energy-efficient operation of HPC datacenter infrastructure including power, cooling, and environmental systems.

## **Core Tasks & Responsibilities**
- Monitor environmental metrics (temperature, humidity, airflow) across racks and zones.  
- Manage and optimize cooling systems (CRAC, RDHX, chiller loops).  
- Track facility-level and rack-level power and energy consumption.  
- Detect and respond to hardware or facility alarms.  
- Schedule and document maintenance interventions.  
- Oversee equipment inventory and physical layout.  
- Ensure safety compliance and facility regulations are followed.  
- Support automation and sustainability initiatives (PUE, CO₂ metrics).

## **Key Studies / Knowledge Areas**
- Data center operations, energy management, and sustainability.  
- Building Management Systems (BMS), DCIM, and Redfish/IPMI protocols.  
- Thermal dynamics and airflow management.  
- Power distribution, UPS systems, and electrical safety standards.  
- Predictive maintenance and root-cause analysis using monitoring data.  
- Incident response and fault detection.  
- RBAC and compliance auditing for control operations.

## **Data Sources They Analyze**
- BMS/DCIM telemetry (temperature, humidity, airflow).  
- IPMI and sensor logs from nodes and racks.  
- Power and energy meters (PDU, UPS, CRAC).  
- Facility maintenance records and logs.  
- Safety and compliance documentation.  
- Network switch environmental metrics.  
- Historical energy efficiency reports (PUE, CO₂ footprint).

## **Tools & Frameworks**
- ExaSage Monitoring and Facility Agents.  
- Data Analytics and AIOps dashboards.  
- Prometheus/Grafana for telemetry visualization.  
- BMS/DCIM systems with Redfish and SNMP interfaces.  
- Python scripts for facility automation and control.  
- Energy analytics and forecasting platforms.  
- RAG-based documentation access for SOPs and safety guides.

## **Research Themes / Study Topics**
- Energy optimization and sustainability analytics (PUE, CO₂).  
- Cooling efficiency benchmarking and airflow optimization.  
- Predictive maintenance for CRAC, UPS, and sensors.  
- Facility-level anomaly detection and correlation analysis.  
- Integration of facility telemetry with HPC monitoring.  
- Root-cause analysis for thermal or power anomalies.  
- Automation and eco-mode control strategies.  
- Compliance verification and incident auditing.

---

## **Example Queries for Multi-Agentic Chat System**

| # | Code | Category | Description | Example Queries | Priority |
|---|------|-----------|--------------|-----------------|-----------|
| 1 | **MON** | **Environmental Monitoring** | Observe and track environmental metrics across racks, zones, and rooms. | “Show temperature map of Zone B.”<br>“Which racks exceed 28°C?” | **H** |
| 2 | **COOL** | **Cooling System Operations** | Manage and analyze CRAC, RDHX, and cooling system efficiency. | “Compare CRAC-3 vs CRAC-5 efficiency.”<br>“Switch CRAC-4 to standby.” | **H** |
| 3 | **ENERGY** | **Power & Energy Management** | Measure energy draw, compute PUE, and monitor power usage. | “Current PUE for datacenter A.”<br>“Energy breakdown per rack.” | **H** |
| 4 | **HEALTH** | **Rack & Node Health** | Monitor node-level thermal and hardware metrics. | “Which nodes report high CPU temperature?”<br>“Fan RPM history for node CN-25.” | **H** |
| 5 | **ALARM** | **Alarms & Anomaly Detection** | Identify and handle environmental or system alarms. | “List all active critical alarms.”<br>“Was there a power spike yesterday?” | **H** |
| 6 | **IRCA** | **Incident Response & Root-Cause Analysis** | Diagnose causes of environmental or power anomalies. | “Why did Room B overheat on Oct 15?”<br>“Correlate UPS alerts with thermal spikes.” | **H** |
| 7 | **MAINT** | **Maintenance Scheduling & Logs** | Plan, track, and document facility interventions. | “What maintenance is scheduled this week?”<br>“Add note for UPS-3 service.” | **M** |
| 8 | **SUSTAIN** | **Sustainability & Efficiency Analytics** | Evaluate CO₂ footprint and energy-saving improvements. | “Show monthly CO₂ footprint.”<br>“Energy saved after airflow optimization.” | **M** |
| 9 | **ASSET** | **Asset & Inventory Management** | Track equipment, racks, and node locations. | “List all servers in Rack-7.”<br>“Where is node CN123 physically located?” | **M** |
| 10 | **NET** | **Networking Infrastructure** | Monitor switches, PDUs, and network-related telemetry. | “Switch S-3 power draw.”<br>“Port errors on S-4.” | **M** |
| 11 | **DOCS** | **Documentation & Learning Support** | Retrieve standard procedures and calibration guides. | “How to calibrate humidity sensors?”<br>“Reset PDU alarm guide.” | **M** |
| 12 | **TREND** | **Historical Trend & Predictive Analysis** | Visualize trends and forecast failures using telemetry data. | “Show 1-year energy trend per rack.”<br>“Predict CRAC-1 failure probability.” | **M** |
| 13 | **INT** | **Facility System Integration** | Query integrated BMS/DCIM systems or Redfish APIs. | “Fetch latest BMS telemetry for Room B.”<br>“UPS battery health via BMS.” | **L** |
| 14 | **SAFE** | **Safety, Compliance & Regulations** | Access safety rules and operational policies. | “Show fire suppression rules.”<br>“Electrical safety SOP.” | **L** |
| 15 | **CTRL** | **Control & Automation Requests** | Execute authorized actuation commands within safety limits. | “Restart CRAC-2.”<br>“Activate eco cooling mode.” | **L** |

---

## **Priority Tags Summary**

| Priority | Meaning | Categories |
|----------|----------|------------|
| **H (High)** | Frequent, critical for datacenter stability and safety. | MON, COOL, ENERGY, HEALTH, ALARM, IRCA |
| **M (Medium)** | Periodic or planning-related operations. | MAINT, SUSTAIN, ASSET, NET, DOCS, TREND |
| **L (Low)** | Restricted or admin-only actions. | INT, SAFE, CTRL |
