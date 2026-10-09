# SECURECORP — Cybersecurity Assessment Capstone

**Junior Cybersecurity Consultant | Controlled Training Laboratory**

## 📌 Project Overview

This project assesses a controlled cybersecurity training environment from both offensive and defensive security perspectives. It documents laboratory setup, network discovery, application security assessment, security monitoring, risk analysis, and remediation recommendations.

## 🎯 Objectives

* Build a controlled cybersecurity lab environment.
* Discover exposed network services using Nmap.
* Verify access to the Damn Vulnerable Web Application (DVWA).
* Configure Wazuh Cloud security monitoring.
* Analyze cybersecurity risks and potential vulnerabilities.
* Document findings and recommend security improvements.

## 🏗️ Lab Architecture

| Component              | Description         |
| ---------------------- | ------------------- |
| Attacker / Analyst     | Ubuntu 26.04 on WSL |
| Target Machine         | Metasploitable2     |
| Vulnerable Application | DVWA                |
| Security Monitoring    | Wazuh Cloud         |
| Monitoring Agent       | SecureCorp-WSL      |
| Network Discovery Tool | Nmap                |

## 🛠️ Technologies Used

* Ubuntu Linux and Windows Subsystem for Linux (WSL)
* Metasploitable2
* DVWA (Damn Vulnerable Web Application)
* Nmap
* Wazuh Cloud
* Networking and vulnerability assessment concepts

## 🔍 Assessment Activities

### 1. Laboratory Setup

Established a controlled environment with Ubuntu WSL, Metasploitable2, and DVWA.

### 2. Network Discovery

Used Nmap to identify exposed services and understand the target's network attack surface.

Services identified included:

* FTP — Port 21
* SSH — Port 22
* Telnet — Port 23
* SMTP — Port 25
* DNS — Port 53
* HTTP — Port 80
* Samba — Ports 139/445
* NFS — Port 2049
* MySQL — Port 3306
* PostgreSQL — Port 5432
* VNC — Port 5900
* X11 — Port 6000

### 3. Application Security Assessment

Verified DVWA availability and assessed the planned testing areas:

* Brute-force testing
* SQL injection
* Cross-site scripting (XSS)
* Command injection
* FTP and SSH credential testing

**Evidence status:** Successful exploitation of these testing activities was not sufficiently verified in the submitted evidence.

### 4. Security Monitoring

Configured Wazuh Cloud and enrolled the Ubuntu WSL agent.

* Agent name: `SecureCorp-WSL`
* Agent status: Active
* Local agent connection: Connected
* Target-side Wazuh monitoring: Not verified

### 5. Risk Assessment

The assessment prioritized the following risks:

* Command injection in vulnerable web applications
* Exposed legacy network services
* Exposed database services
* Insecure remote administration services
* Insufficient target-side security monitoring

## 🛡️ Security Recommendations

1. Restrict unnecessary inbound network services.
2. Disable or isolate Telnet, VNC, X11, and unused FTP, RPC, and NFS services.
3. Patch obsolete operating systems and software.
4. Enforce strong authentication and multi-factor authentication (MFA).
5. Validate and sanitize web application inputs.
6. Configure target-side Wazuh monitoring and log collection.
7. Improve security detection rules and alert investigation procedures.
8. Maintain and test backups regularly.
9. Provide cybersecurity awareness training.

## 📊 Project Outcome

The assessment established the laboratory environment, verified DVWA availability, documented exposed network services, and demonstrated an active Wazuh agent on Ubuntu WSL.

No confirmed compromise is claimed. Activities without sufficient practical evidence are marked **Not Verified**.

## 📁 Suggested Project Structure

```text
SecureCorp-Cybersecurity-Capstone/
│
├── README.md
├── SecureCorp_Final_Submission_Report.docx
├── screenshots/
│   ├── wazuh-environment.png
│   ├── agent-deployment.png
│   ├── agent-installation.png
│   ├── active-agent.png
│   ├── wazuh-overview.png
│   └── target-network-evidence.png
│
└── presentation/
    └── SecureCorp-Presentation.pptx
```

*Note: The folder structure above is a suggested organization. Add only files and screenshots that you actually have.*

## ⚖️ Rules of Engagement

All assessment activities must remain within the authorized, controlled training laboratory. Password testing is restricted to self-created lab accounts. Findings must be supported by practical evidence.

## 📝 Conclusion

This capstone demonstrates foundational cybersecurity assessment skills, including network discovery, application security review, security monitoring, risk assessment, and remediation planning. Future work should establish target-side telemetry and repeat unverified activities with timestamps, source and target IP addresses, supporting evidence, and Wazuh rule references.

---

**Project:** SecureCorp Cybersecurity Assessment Capstone
**Role:** Junior Cybersecurity Consultant
**Environment:** Controlled Training Laboratory
**Status:** Final Submission Report Prepared
