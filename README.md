# Enterprise Threat Hunting & Security Analytics Portfolio

![GitHub last commit](https://img.shields.io/github/last-commit/Meghanatha002/Enterprise-Threat-Hunting-and-Security-Analytics?style=for-the-badge)
![GitHub repo size](https://img.shields.io/github/repo-size/Meghanatha002/Enterprise-Threat-Hunting-and-Security-Analytics?style=for-the-badge)
![GitHub language count](https://img.shields.io/github/languages/count/Meghanatha002/Enterprise-Threat-Hunting-and-Security-Analytics?style=for-the-badge)
![GitHub top language](https://img.shields.io/github/languages/top/Meghanatha002/Enterprise-Threat-Hunting-and-Security-Analytics?style=for-the-badge)
![License](https://img.shields.io/github/license/Meghanatha002/Enterprise-Threat-Hunting-and-Security-Analytics?style=for-the-badge)

---

## Overview

Welcome to my **Enterprise Threat Hunting & Security Analytics Portfolio**.

This repository showcases a collection of professional cybersecurity case studies focused on enterprise threat hunting, security analytics, digital investigations, and machine learning-driven threat detection. Each project demonstrates practical blue-team methodologies using Python, the Elastic Stack (ELK), Kibana, Windows event logs, DNS analytics, NetFlow analysis, and supervised machine learning.

Unlike isolated proof-of-concept scripts, these investigations follow structured security analysis workflows similar to those used by Security Operations Centers (SOCs). Each case study includes source code, technical documentation, investigation reports, findings, and supporting evidence to demonstrate both analytical thinking and technical implementation.

The portfolio covers multiple cybersecurity domains, including endpoint security, authentication analysis, DNS threat hunting, network traffic analysis, behavioral analytics, statistical anomaly detection, and phishing website classification using machine learning.

---

# Repository Objectives

This portfolio was created to demonstrate practical cybersecurity skills through real-world inspired investigations and technical analysis.

The primary objectives include:

- Investigating security events using structured threat hunting methodologies.
- Performing endpoint, DNS, and network traffic analysis.
- Developing Python-based security analytics workflows.
- Building interactive dashboards using Kibana.
- Detecting anomalous behavior using statistical analysis and machine learning.
- Producing professional investigation reports suitable for enterprise environments.
- Demonstrating security engineering, analytical reasoning, and documentation skills.

---

# Core Skills Demonstrated

### Threat Hunting

- Windows Endpoint Threat Hunting
- DNS Threat Hunting
- Network Flow Investigation
- Authentication Analysis
- Behavioral Analytics
- IOC Identification
- Threat Correlation
- Security Event Investigation

### Security Analytics

- Log Analysis
- Statistical Analysis
- Frequency Analysis
- Data Enrichment
- Network Traffic Analysis
- Event Correlation
- Security Monitoring
- Dashboard Development

### Machine Learning

- Logistic Regression
- Random Forest
- Multi-Layer Perceptron
- Model Evaluation
- Feature Engineering
- ROC Analysis
- Cross Validation
- Classification Performance Comparison

### Python Development

- Data Processing
- Security Automation
- Data Visualization
- Feature Extraction
- Data Cleaning
- Statistical Computing
- Machine Learning Pipelines

---

# Technologies & Tools

## Programming & Data Science

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Jupyter Notebook

## Security Analytics

- Elastic Stack (ELK)
- Elasticsearch
- Kibana
- Windows Event Logs
- NetFlow
- DNS Logs
- JSON Data Processing

## Cybersecurity

- Threat Hunting
- Security Analytics
- Endpoint Investigation
- Authentication Analysis
- DNS Security
- Network Traffic Analysis
- Machine Learning for Cybersecurity

---

# Investigation Workflow

The investigations throughout this repository follow a structured analytical workflow similar to enterprise Security Operations Centers (SOCs).

```text
                  Raw Security Data
                          │
                          ▼
                 Data Collection & Parsing
                          │
                          ▼
                Python-Based Data Processing
                          │
                          ▼
                Data Cleaning & Enrichment
                          │
                          ▼
             Elasticsearch Data Ingestion
                          │
                          ▼
             Kibana Dashboards & Visualizations
                          │
                          ▼
                 Threat Hunting & Analysis
                          │
                          ▼
              IOC Identification & Correlation
                          │
                          ▼
             Security Investigation Findings
                          │
                          ▼
          Technical Documentation & Reporting
```

---

# Investigation Methodology

Although each case study focuses on a different cybersecurity domain, they all follow a consistent investigative process.

### Phase 1 — Data Collection

Security datasets, Windows event logs, DNS records, NetFlow data, or phishing website features are collected for analysis.

↓

### Phase 2 — Data Preparation

Python is used to clean, preprocess, normalize, and structure the datasets before analysis.

↓

### Phase 3 — Data Analysis

Depending on the investigation, statistical analysis, log analysis, visualization, or supervised machine learning techniques are applied.

↓

### Phase 4 — Threat Hunting

Indicators of compromise (IOCs), anomalies, suspicious behaviors, authentication irregularities, malicious domains, abnormal network activity, or phishing indicators are identified.

↓

### Phase 5 — Documentation

Each investigation concludes with technical findings, supporting evidence, and a professional report summarizing the methodology, analysis, and conclusions.

---


# Repository Structure

This repository is organized as a collection of independent threat hunting and security analytics case studies. Each project demonstrates a different area of cybersecurity analysis while following a consistent investigation methodology.

Every project directory includes:

- Python source notebook (`.ipynb`)
- PDF export of the notebook
- Professional technical investigation report
- Dedicated project README
- Supporting documentation where applicable

```text
Enterprise-Threat-Hunting-and-Security-Analytics
│
├── 01-domain-frequency-analysis
├── 02-insider-access-anomaly-detection
├── 03-windows-endpoint-threat-detection
├── 04-dns-threat-hunting
├── 05-network-flow-threat-hunting
└── 06-machine-learning-phishing-detection
```

---

# Portfolio Case Studies

## 01 — Domain Frequency Analysis for Suspicious Domain Detection

### Objective

Identify suspicious or algorithmically generated domain names using statistical frequency analysis.

### Investigation Summary

This project applies Python-based statistical analysis to evaluate domain labels and identify uncommon naming patterns frequently associated with Domain Generation Algorithms (DGAs). Character frequency scoring is used to distinguish legitimate domains from statistically unusual domain names that may indicate malicious infrastructure.

### Techniques Used

- Domain parsing
- Character frequency analysis
- Statistical scoring
- Python automation
- Threat hunting

### Skills Demonstrated

- Python
- Pandas
- Data analysis
- Threat intelligence
- Statistical anomaly detection

---

## 02 — Insider Access Anomaly Detection

### Objective

Identify suspicious authentication behavior that may indicate insider threats or unauthorized account activity.

### Investigation Summary

Authentication records are analyzed to detect abnormal access behavior by examining user activity, login events, and authentication patterns. The investigation focuses on identifying deviations from expected behavior that may indicate compromised credentials or malicious insider activity.

### Techniques Used

- Authentication log analysis
- Behavioral analytics
- User activity analysis
- Event correlation
- Anomaly detection

### Skills Demonstrated

- Security analytics
- Authentication analysis
- Windows security logs
- Threat hunting
- Python

---

## 03 — Windows Endpoint Threat Detection

### Objective

Investigate Windows event logs to identify endpoint compromise indicators and malicious activity.

### Investigation Summary

This investigation analyzes Windows Event Logs using Elastic Stack and Kibana to identify multiple attack techniques, including external USB device usage, suspicious NTLM authentication associated with Pass-the-Hash attacks, and malicious service installation used for persistence. The investigation correlates multiple Event IDs to reconstruct attacker behavior and identify indicators of compromise.

### Key Event IDs Investigated

- Event ID 6416 – External Device Detection
- Event ID 4624 – Successful Logon Analysis
- Event ID 7045 – Service Installation Events

### Skills Demonstrated

- Windows Event Analysis
- Elastic Stack
- Kibana
- Endpoint threat hunting
- Pass-the-Hash detection
- Persistence detection
- IOC analysis

---

## 04 — DNS Threat Hunting

### Objective

Identify suspicious DNS activity through statistical analysis and domain investigation.

### Investigation Summary

DNS records are analyzed to detect suspicious domain activity, abnormal query behavior, and potentially malicious domains. The investigation demonstrates how DNS telemetry can be leveraged to identify attacker infrastructure, beaconing behavior, and domain-based threats using structured threat hunting methodologies.

### Techniques Used

- DNS analysis
- Domain reputation investigation
- Frequency analysis
- Query correlation
- Threat hunting

### Skills Demonstrated

- DNS Security
- Threat Hunting
- Python
- Security Analytics
- Data Analysis

---

## 05 — Network Flow Threat Hunting

### Objective

Detect suspicious outbound network communications and potential data exfiltration using NetFlow analytics.

### Investigation Summary

This investigation leverages enriched NetFlow data within Elastic Stack to identify suspicious external communications. Kibana dashboards are used to analyze outbound traffic volume, external connection frequency, and long-duration sessions to uncover indicators of data exfiltration and abnormal network behavior.

Three analytical dashboards were developed:

- Large Data Uploads
- External Connection Frequency
- Long-Duration External Connections

### Skills Demonstrated

- NetFlow Analysis
- Elastic Stack
- Kibana Dashboards
- Network Threat Hunting
- Data Exfiltration Detection
- Security Visualization

---

## 06 — Machine Learning-Based Phishing Website Detection

### Objective

Evaluate multiple supervised machine learning algorithms for phishing website classification.

### Investigation Summary

This project compares Logistic Regression, Random Forest, and Multi-Layer Perceptron classifiers using a feature-engineered phishing website dataset. Each model is trained under identical preprocessing conditions to provide an objective comparison of classification performance and identify the most effective approach for automated phishing detection.

### Models Evaluated

- Logistic Regression
- Random Forest
- Multi-Layer Perceptron (Neural Network)

### Skills Demonstrated

- Machine Learning
- Feature Engineering
- Model Evaluation
- Cross Validation
- ROC Analysis
- Python
- Scikit-learn

---

# Cybersecurity Skills Matrix

| Domain               | Technologies & Techniques |
|----------------------|--------------------------|
| Threat Hunting       | IOC Identification, Event Correlation, Behavioral Analytics |
| Windows Security     | Event IDs, Authentication Analysis, Endpoint Investigation |
| Network Security     | NetFlow Analysis, Traffic Investigation, Data Exfiltration Detection |
| DNS Security         | Domain Analysis, Frequency Analysis, Query Investigation |
| SIEM & Visualization | Elastic Stack, Elasticsearch, Kibana Dashboards |
| Security Analytics   | Python, Pandas, Statistical Analysis, Data Enrichment |
| Machine Learning     | Logistic Regression, Random Forest, Neural Networks |
| Programming          | Python, Jupyter Notebook, NumPy, Scikit-learn |
| Investigation        | Log Analysis, Threat Correlation, Incident Investigation |
| Documentation        | Technical Reporting, Security Documentation, Case Study Development |

---
---

# Enterprise Security Analytics Architecture

The projects within this repository follow a layered security analytics architecture that combines Python-based data processing, Elastic Stack visualization, statistical analysis, and machine learning to investigate security events.

```text
                    Security Data Sources
    ┌───────────────────────────────────────────────────────┐
    │                                                       │
    │  Windows Event Logs     DNS Logs      NetFlow Data    │
    │                                                       │
    │  Website Features      Authentication Logs            │
    └───────────────────────────────────────────────────────┘
                           │
                           ▼
                 Python Analytics Pipeline
        Data Cleaning • Parsing • Feature Engineering
                           │
                           ▼
                Statistical & Behavioral Analysis
                           │
                           ▼
                  Elasticsearch Data Storage
                           │
                           ▼
                  Kibana Dashboards & Queries
                           │
                           ▼
          Threat Hunting • IOC Discovery • Investigation
                           │
                           ▼
          Professional Reports & Security Documentation
```

---

---

# Elastic Stack (ELK) Workflow

Several investigations relied on the Elastic Stack for large-scale log analysis and threat hunting.

The general workflow followed:

```text
Security Logs
      │
      ▼
 Elasticsearch
      │
      ▼
 Indexing & Searching
      │
      ▼
 Kibana Discover
      │
      ▼
 Dashboard Creation
      │
      ▼
 Threat Hunting
      │
      ▼
 Investigation Findings
```

Elastic Stack was used for:

- Windows Event Log analysis
- DNS investigations
- NetFlow analysis
- Authentication investigations
- Dashboard creation
- IOC correlation
- Security visualization

---

# Kibana Investigation Techniques

Throughout the investigations, Kibana's search capabilities were used to identify suspicious activity using structured filters and field-based queries.

Common investigation techniques included:

### Windows Event Investigation

- Event ID filtering
- Authentication package analysis
- Logon type analysis
- USB device detection
- Service installation monitoring

---

### DNS Analysis

- Suspicious domain identification
- Frequency-based investigation
- Domain correlation
- DNS traffic analysis

---

### NetFlow Analysis

- External communication analysis
- Long-duration connections
- Data transfer analysis
- Outbound traffic investigation

---

### Dashboard Development

Interactive dashboards were created to simplify large-scale investigations and identify high-risk activity more efficiently.

Examples include:

- Large Data Uploads
- External Connection Frequency
- Long Duration Connections
- Threat Hunting Tables
- Statistical Summaries

---


# Machine Learning Workflow

The phishing detection case study follows a complete supervised machine learning workflow.

```text
Phishing Dataset
        │
        ▼
Data Cleaning
        │
        ▼
Feature Engineering
        │
        ▼
Train/Test Split
        │
        ▼
Feature Scaling
        │
        ▼
Model Training
        │
        ▼
Performance Evaluation
        │
        ▼
Model Comparison
        │
        ▼
Best Model Selection
```

The project evaluates:

- Logistic Regression
- Random Forest
- Multi-Layer Perceptron (Neural Network)

Performance evaluation includes:

- Accuracy
- Precision
- Recall
- F1 Score
- ROC Curve
- ROC-AUC
- Confusion Matrix
- Cross Validation

---

# Dashboard Gallery

Representative dashboard categories developed throughout this repository include:

### Windows Endpoint Threat Hunting

- Windows Event Analysis
- Authentication Investigation
- Service Installation Monitoring
- Endpoint Activity Investigation

---

### DNS Threat Hunting

- Suspicious Domain Investigation
- Domain Frequency Analysis
- Query Correlation

---

### Network Flow Analytics

- Large External Data Transfers
- External Connection Frequency
- Long Duration Sessions
- Network Communication Analysis

---

### Machine Learning

- ROC Curve Comparison
- Confusion Matrices
- Feature Importance
- Model Performance Evaluation

> **Note:** Dashboard screenshots and investigation outputs are included within the individual project folders where applicable.

---
# Repository Statistics

This repository represents a collection of practical cybersecurity investigations developed to demonstrate enterprise threat hunting, security analytics, and machine learning techniques.

### Portfolio Summary

| Category | Details |
|----------|---------|
| Case Studies | **6** |
| Programming Language | Python |
| Security Platform | Elastic Stack (ELK) |
| Visualization Platform | Kibana |
| Machine Learning Models | 3 |
| Professional Technical Reports | 6 |
| Investigation Notebooks | 8+ |
| Dashboard Implementations | Multiple |
| Threat Hunting Methodologies | Windows, DNS, NetFlow |
| Investigation Domains | Endpoint, Network, Authentication, Machine Learning |

---
---

# Key Competencies Demonstrated

### Blue Team Operations

- Threat Hunting
- Security Monitoring
- Behavioral Analytics
- IOC Identification
- Event Correlation
- Incident Investigation

---

### Security Analytics

- Windows Event Analysis
- Authentication Analysis
- DNS Analytics
- Network Flow Analytics
- Statistical Analysis
- Data Enrichment

---

### Data Science for Cybersecurity

- Feature Engineering
- Data Cleaning
- Machine Learning
- Model Evaluation
- Classification Analysis
- Performance Comparison

---

### Python Development

- Pandas
- NumPy
- Scikit-learn
- JSON Processing
- Data Automation
- Jupyter Notebook

---

### SIEM & Visualization

- Elasticsearch
- Kibana
- Dashboard Development
- Security Visualization
- Log Analysis

---

# Future Enhancements

This portfolio will continue to evolve with additional enterprise-focused cybersecurity projects.

Planned areas of expansion include:

- Cloud Security Analytics (AWS & Azure)
- Splunk Enterprise Security
- Microsoft Sentinel
- Sigma Detection Rules
- YARA Rule Development
- MITRE ATT&CK Mapping
- Detection Engineering
- Threat Intelligence Automation
- SOAR Playbooks
- Malware Analysis
- Digital Forensics
- SOC Automation with Python

---

# Repository Disclaimer

This repository has been created for educational and professional portfolio purposes.

Certain datasets, log files, and supporting resources used during the investigations are not included due to licensing restrictions, privacy considerations, or academic policies.

Only the implementation methodology, analytical workflows, technical documentation, investigation reports, and summarized findings are provided.

The projects are intended to demonstrate practical cybersecurity concepts, threat hunting methodologies, and analytical techniques without exposing restricted datasets or proprietary information.

---

# About Me

I am a cybersecurity professional with interests in:

- Security Operations (SOC)
- Threat Hunting
- Network Security
- Security Analytics
- Blue Team Operations
- Incident Response
- Machine Learning for Cybersecurity
- Enterprise Security Architecture

My goal is to build practical, technically accurate, and well-documented security projects that reflect real-world investigative workflows and enterprise cybersecurity practices.

---

# Connect With Me

**GitHub**

https://github.com/Meghanatha002

**LinkedIn**

> *(https://www.linkedin.com/in/meghanatha-reddy-p/)*

---

