# DNS Threat Hunting and Suspicious Domain Analysis

## Professional Summary

This case study demonstrates a DNS threat hunting workflow implemented using Python to identify suspicious domain activity through DNS log enrichment, statistical domain frequency analysis, Top 1 Million domain validation, and naked IP detection. The investigation illustrates how multiple analytical techniques can be combined to prioritize potentially malicious DNS activity for further investigation.

---

# Project Overview

DNS is one of the most valuable data sources available to Security Operations Centers (SOCs) because nearly every network communication begins with a DNS query.

This project analyzes enterprise DNS logs and enriches them with contextual information to identify uncommon domains, suspicious DNS behavior, and potential attacker infrastructure.

---

# Investigation Workflow

```text
Enterprise DNS Logs
        │
        ▼
Root Domain Extraction
        │
        ▼
Frequency Score Calculation
        │
        ▼
Top 1M Domain Validation
        │
        ▼
DNS Log Enrichment
        │
        ▼
IP-to-Domain Mapping
        │
        ▼
Naked IP Detection
        │
        ▼
Suspicious Domain Analysis
```

---

# Key Findings

* Processed **29,368 DNS log records**.
* Extracted root domains from enterprise DNS traffic.
* Compared domains against **891,544** known domains.
* Identified multiple naked IP communications.
* Mapped IP addresses to known domains.
* Evaluated suspicious domains using statistical frequency scoring.
* Produced an enriched DNS dataset for threat hunting.

---

# Skills Demonstrated

* DNS Threat Hunting
* Security Analytics
* DNS Log Enrichment
* Python Programming
* Threat Intelligence
* Data Analysis
* Threat Hunting Methodology

---

# Project Files

| File                              | Description                                                                             |
| --------------------------------- | --------------------------------------------------------------------------------------- |
| `dns_threat_hunting.ipynb`        | Jupyter Notebook containing the complete DNS analysis workflow.                         |
| `dns_threat_hunting_notebook.pdf` | PDF export of the notebook including implementation and outputs.                        |
| `DNS_Threat_Hunting_Report.pdf`   | Technical report documenting the investigation, methodology, findings, and conclusions. |

---

# Dataset Notice

The original DNS log dataset and supporting reference datasets are not included in this repository due to course licensing and data-sharing restrictions.

This repository contains the implementation methodology, documentation, and summarized findings only.

---

# Conclusion

This project demonstrates how DNS telemetry can be transformed into actionable threat hunting intelligence through statistical analysis and enrichment. The techniques presented are directly applicable to enterprise SOC environments for detecting suspicious domains, attacker infrastructure, and anomalous DNS activity.
