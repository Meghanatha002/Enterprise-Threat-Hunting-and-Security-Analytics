# Windows Endpoint Threat Detection and Threat Hunting using ELK

## Professional Summary

This case study demonstrates a Windows endpoint threat hunting investigation performed using the Elastic Stack (ELK). Windows Security Event Logs were analyzed within Kibana to identify indicators of endpoint compromise by correlating multiple Windows Event IDs associated with removable media detection, authentication events, and malicious service installation.

The investigation successfully reconstructed a probable attack sequence involving external device activity, suspicious NTLM authentication consistent with **Pass-the-Hash**, and the deployment of an encoded PowerShell-based persistence mechanism.

---

# Investigation Overview

This investigation follows a structured threat hunting workflow commonly performed within a Security Operations Center (SOC). Rather than relying on a single alert, multiple Windows Security Event Logs were correlated to identify suspicious behavior across enterprise endpoints.

The investigation focused on:

* External USB device detection
* NTLM authentication analysis
* Pass-the-Hash detection
* User and workstation identification
* Malicious Windows service installation
* PowerShell-based persistence

---

# Investigation Workflow

The investigation followed the sequence below:

```text
Windows Security Logs
        │
        ▼
Event ID 6416
(External USB Device)
        │
        ▼
Event ID 4624
(Successful Logon)
        │
        ▼
Exclude Kerberos
        │
        ▼
Identify NTLM Logons
(Logon Type 3)
        │
        ▼
Identify User & Workstation
        │
        ▼
Event ID 7045
(New Service Installation)
        │
        ▼
Encoded PowerShell Execution
        │
        ▼
Evidence of Endpoint Compromise
```

---

# Investigation Findings

## Evidence 1 – External USB Device Detection

Using the filter:

```text
EventID:6416
```

Windows detected a newly connected external USB device.

**Observed Host**

* Hostname: **IT04.YOLP.com**
* Host IP: **10.0.1.14**

**Evidence**

> `screenshots/01-external-usb-device-detection-eventid-6416.png`

---

## Evidence 2 – Suspicious NTLM Authentication

The investigation analyzed successful authentication events using:

```text
EventID:4624
```

To isolate suspicious authentication events, Kerberos logons were excluded:

```text
EventID:4624 AND NOT Message:"*Kerberos*"
```

The remaining events showed:

* Authentication Package: **NtLmSsp**
* Logon Type: **3 (Network Logon)**

These events are commonly associated with **Pass-the-Hash** attacks.

**Evidence**

> `screenshots/02-ntlm-authentication-logon-eventid-4624.png`

---

## Evidence 3 – Source User and Workstation Identification

Further examination of the authentication logs identified the account responsible for the suspicious activity.

**Observed User**

* User: **droseberry**

**Observed Host**

* Hostname: **IT03.YOLP.com**

**Source Workstation**

* **5e9cQ0WHG4RFhNv.YOLP.com**

This information allowed the investigation to identify the endpoint associated with the abnormal authentication events.

**Evidence**

> `screenshots/03-source-workstation-and-user-identification.png`

---

## Evidence 4 – Suspicious Windows Service Installation

The investigation then analyzed Windows service installation events using:

```text
EventID:7045
```

One service immediately stood out due to its randomly generated name.

**Observed Service**

```
flpWsoaatgwnVPnj
```

Unlike legitimate Windows services, this service used an unusual name and executed PowerShell instead of a trusted executable.

**Evidence**

> `screenshots/04-suspicious-service-installation-eventid-7045.png`

---

## Evidence 5 – Encoded PowerShell Payload

Inspection of the service configuration revealed execution of:

```text
powershell.exe -nop -w hidden
```

followed by a large Base64-encoded payload.

Characteristics indicating malicious behavior included:

* Hidden PowerShell execution
* Base64-encoded command
* No PowerShell profile (`-nop`)
* Execution under the **LocalSystem** account
* Random service name

These behaviors are commonly associated with:

* Fileless malware
* PowerShell backdoors
* Persistence mechanisms
* Living-off-the-Land (LotL) techniques

**Evidence**

> `screenshots/05-encoded-powershell-service-payload.png`

---

# Indicators of Compromise (IOCs)

| Indicator              | Value            |
| ---------------------- | ---------------- |
| Event ID               | 6416             |
| Event ID               | 4624             |
| Event ID               | 7045             |
| Authentication Package | NtLmSsp          |
| Logon Type             | 3                |
| Suspicious User        | droseberry       |
| Compromised Host       | IT03.YOLP.com    |
| External Device Host   | IT04.YOLP.com    |
| Service Name           | flpWsoaatgwnVPnj |
| PowerShell Flags       | `-nop -w hidden` |

---

# Skills Demonstrated

* Windows Security Event Log Analysis
* Elastic Stack (ELK)
* Kibana Discover
* Threat Hunting
* Endpoint Detection
* Pass-the-Hash Detection
* Windows Authentication Analysis
* PowerShell Attack Analysis
* Incident Investigation
* Security Analytics

---

# Project Files

| File                                             | Description                                                                                      |
| ------------------------------------------------ | ------------------------------------------------------------------------------------------------ |
| `Windows_Endpoint_Threat_Detection_Report.pdf`   | Technical report documenting the investigation methodology, evidence, findings, and conclusions. |
| `Windows_Endpoint_Threat_Detection_Findings.pdf` | Detailed investigation findings and supporting analysis.                                         |
| `screenshots/`                                   | Kibana evidence collected during the investigation.                                              |

---

# Security Impact

This investigation demonstrates how correlating multiple Windows Security Event Logs can reveal attacker behavior that would otherwise appear unrelated. By combining endpoint telemetry, authentication analysis, and service installation events, the investigation reconstructs a likely attack chain involving unauthorized NTLM authentication and PowerShell-based persistence.

The techniques demonstrated in this case study closely resemble workflows used by enterprise Security Operations Centers (SOCs), Digital Forensics and Incident Response (DFIR) teams, and Threat Hunting analysts.

---

# Conclusion

By systematically correlating Windows Event IDs **6416**, **4624**, and **7045**, the investigation successfully identified multiple indicators of compromise associated with endpoint compromise and attacker persistence. The methodology illustrates a practical, evidence-driven threat hunting workflow for detecting suspicious authentication activity, malicious service installation, and PowerShell-based attacks in enterprise Windows environments.
