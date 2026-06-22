# Network Flow Threat Hunting & Data Exfiltration Detection

An end-to-end Network Flow Threat Hunting project that combines Python-based NetFlow enrichment with Elastic Stack (ELK) dashboards to identify indicators of data exfiltration, malware beaconing, command-and-control (C2) communication, and long-duration suspicious network sessions.

The project enriches raw NetFlow logs by classifying internal/external IP addresses, mapping known public IP ranges to organizations, and visualizing suspicious communication patterns using Kibana dashboards for security investigation.

---

## Project Overview

Modern attackers often avoid triggering signature-based detection by slowly transferring data, maintaining persistent outbound connections, or repeatedly communicating with external infrastructure.

This project demonstrates how enriched NetFlow telemetry can be leveraged to identify these behaviors through data correlation and visualization.

The workflow includes:

- NetFlow log enrichment using Python
- Internal vs External IP classification
- Public IP organization mapping
- Elastic Stack ingestion
- Kibana dashboard creation
- Network threat hunting
- Correlation of multiple behavioral indicators
- Identification of potentially compromised hosts

---

## Objectives

The objectives of this project were to:

- Enrich raw NetFlow records with additional security context
- Identify large outbound data transfers
- Detect excessive outbound connections
- Discover long-duration external sessions
- Correlate multiple network indicators to prioritize investigation
- Visualize suspicious communication patterns using Kibana dashboards

---

## Dataset

The analysis was performed on approximately **42,766 NetFlow records**.

To preserve licensing and academic integrity, the original dataset is **not included** in this repository.

The repository contains:

- Python implementation
- NetFlow enrichment methodology
- Dashboard configurations
- Investigation report
- Findings and conclusions

---

## Methodology

### 1. NetFlow Log Processing

The notebook loads raw NetFlow logs into a Pandas DataFrame for preprocessing and enrichment.

Key preprocessing tasks include:

- JSON parsing
- IP validation
- Data normalization
- Feature generation

---

### 2. Internal vs External IP Classification

Python's `ipaddress` module is used to classify every IP address into internal or external networks.

Private ranges evaluated include:

- 10.0.0.0/8
- 172.16.0.0/12
- 192.168.0.0/16

This additional context allows the analysis to focus specifically on outbound communication leaving the enterprise network.

---

### 3. Company Mapping

Known public IP ranges were mapped to major organizations including:

- Microsoft
- Google
- Amazon
- Facebook

Unknown external destinations are categorized as:

```
None
```

These unknown destinations become primary candidates during threat hunting.

---

### 4. Data Enrichment

Additional fields were generated including:

- src_ip_internal
- des_ip_internal
- des_ip_company

The enriched NetFlow dataset was then exported for Elastic Stack visualization.

---

### 5. Kibana Dashboard Development

Three independent threat hunting dashboards were created to detect different attacker behaviors.

The findings from all dashboards were later correlated to identify the highest-risk systems.

---

# Dashboard Gallery

---

## Large Data Upload Detection

This dashboard identifies internal hosts transferring unusually large amounts of data to unknown external destinations.

Key metric:

- Sum of bytes transferred

Primary use case:

- Data Exfiltration Detection

---

## External Connection Frequency

This dashboard identifies hosts establishing repeated outbound connections to external IP addresses.

Key metric:

- Count of outbound connections

Primary use case:

- Malware Beaconing
- Command-and-Control Detection

---

## Long Duration Connections

This dashboard highlights systems maintaining unusually long communication sessions with external hosts.

Key metric:

- Session Duration (Age)

Primary use case:

- Persistent Backdoors
- Covert Communication Channels

---

## Combined Threat Hunting Dashboard

The final dashboard correlates all three indicators into a single investigation view.

Rather than relying on one metric alone, suspicious hosts are prioritized using:

- Large uploads
- Frequent outbound communication
- Long-duration sessions

This significantly improves investigation accuracy.

---

# Key Findings

The investigation identified multiple internal hosts exhibiting suspicious outbound behavior.

## High-Risk Hosts

### Host: 10.0.1.37

Indicators:

- Large outbound uploads
- Unknown external destination
- Long-duration communication

Risk Level:

🔴 High

---

### Host: 10.0.1.63

Indicators:

- Long-duration connections
- Large outbound transfers

Risk Level:

🔴 High

---

### Host: 10.0.1.64

Indicators:

- Multi-day external session
- Persistent communication

Risk Level:

🟠 Medium-High

---

### Host: 192.168.163.136

Indicators:

- Large number of outbound connections

Risk Level:

🟠 Medium

---

### Host: 10.0.1.126

Indicators:

- High outbound data volume

Risk Level:

🟠 Medium

---

# Threat Hunting Workflow

```
Raw NetFlow Logs
        │
        ▼
Python Data Enrichment
        │
        ▼
Internal / External Classification
        │
        ▼
Public IP Organization Mapping
        │
        ▼
Elastic Stack Ingestion
        │
        ▼
Kibana Dashboards
        │
        ▼
Threat Correlation
        │
        ▼
Compromised Host Identification
```

---

# Technologies Used

- Python
- Pandas
- JSON
- ipaddress
- Elastic Stack (ELK)
- Kibana
- Network Flow Analysis
- NetFlow
- Threat Hunting
- Data Enrichment

---

# Skills Demonstrated

- Network Security Analytics
- Threat Hunting
- Network Flow Analysis
- Data Enrichment
- Data Correlation
- Elastic Stack
- Kibana Dashboard Development
- Python Automation
- Threat Intelligence
- IOC Identification
- Data Exfiltration Detection
- Command-and-Control Detection
- Security Visualization
- Security Investigation

---

# Repository Contents

```
05-network-flow-threat-hunting/

│── network_flow_threat_hunting.ipynb
│── network_flow_threat_hunting_notebook.pdf
│── Network_Flow_Threat_Hunting_Report.pdf
│── README.md
```

---

# Key Takeaways

This project demonstrates how multiple network indicators can be correlated to improve threat detection accuracy.

Rather than relying on a single metric, combining outbound data volume, connection frequency, and session duration enables analysts to identify hosts exhibiting behaviors consistent with data exfiltration, malware beaconing, and persistent command-and-control communication.

The project highlights a practical workflow for transforming raw NetFlow telemetry into actionable security intelligence using Python and the Elastic Stack.

---

## Disclaimer

This repository is intended solely for educational and portfolio purposes.

The original datasets used during the analysis are not included due to licensing, privacy, and academic restrictions. Only the analysis methodology, Python implementation, dashboard design, and summarized findings are provided.

---