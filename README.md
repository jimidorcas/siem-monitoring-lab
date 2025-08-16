
# SIEM Monitoring Lab — Splunk Home Setup for Threat Detection


This project simulates SOC (Security Operations Center) activity using Splunk Cloud to monitor Apache web access logs. It demonstrates my ability to set up a SIEM dashboard, analyze log data for suspicious behavior, and detect potential threats such as reconnaissance, brute-force attempts, and geographic anomalies.

---

##  Goal

To build a home SOC-style SIEM monitoring setup and showcase skills in log ingestion, SPL (Search Processing Language), threat hunting, detection use cases, and dashboarding — using Splunk Cloud.

---

##  Tools Used

| Tool         | Purpose                         |
|--------------|---------------------------------|
| Splunk Cloud | SIEM platform / dashboarding    |
| Apache Logs  | Simulated web log data source   |
| SPL          | Detection queries               |

---

##  Detection Use Cases Implemented

| Use Case                             | SPL Query (Simplified)                           |
|--------------------------------------|--------------------------------------------------|
| **Top Talkers (Most Active IPs)**    | `| stats count by clientip \| sort -count \| head 10` |
| **404 Error Scanners**               | `status=404 \| stats count by clientip \| sort -count \| head 10` |
| **Top Requested URLs**               | `| stats count by uri_path \| sort -count \| head 10` |
| **Traffic Trends Over Time**         | `| timechart count span=1h`                      |
| **Geographic Outlier IPs**           | `| iplocation clientip … \| stats count by Country` |

---

##  Dashboard Panels

Dashboard Name: **Web SOC Monitoring**

Panels included:
- Top 10 Most Active IPs  
- Top 404 Error Generators  
- Top Requested URLs  
- Hourly Traffic Trends (Traffic Over Time)  
- Geographic Outlier IPs *(if available)*

---

##  Screenshots

