# 🔐 Dual VM Penetration Testing Lab – Exploitation & Security Analysis

This repository documents a **controlled internal penetration testing exercise** performed against two intentionally vulnerable virtual machines hosted inside an isolated lab network. The project demonstrates practical skills in **network reconnaissance, vulnerability identification, exploitation analysis, and security assessment documentation**, aligned with real-world penetration testing workflows.

The engagement simulates an internal attacker scenario, where an adversary already has network-level access and attempts to enumerate, exploit, and analyze weaknesses across multiple hosts.

---

## 🎯 Project Objectives

The primary goals of this project were to:

- Perform structured internal network reconnaissance  
- Identify exposed services and attack surfaces  
- Analyze misconfigurations and outdated components  
- Validate exploitation paths in a controlled lab  
- Understand real-world attack chains  
- Document findings in a professional penetration-test format  
- Propose remediation and defensive improvements  

---

## 🧪 Lab Environment Overview

| Component | Description |
|--------|-------------|
| Attacker Machine | Kali Linux |
| Target VM 1 | Windows 7  |
| Target VM 2 | CentOS-based Server  |
| Network Type | Internal / Host-only |
| Assessment Type | Internal Network Penetration Test |

The lab simulates a small enterprise environment where systems communicate on the same subnet.

---

## 🧭 Assessment Scope

### In-Scope Systems
- **192.168.2.100** – Windows 7 system  
- **192.168.2.101** – Linux-based server with web & SMB services  

### Testing Scope Included
- Network enumeration  
- Service discovery  
- Vulnerability identification  
- Misconfiguration analysis  
- Controlled exploitation  
- Post-exploitation validation  
- Documentation & reporting  

---

## 🧰 Tools & Techniques Used

- **Nmap** – service discovery & OS fingerprinting  
- **Metasploit Framework** – exploitation & post-exploitation  
- **Enum4linux** – SMB enumeration  
- **SMBClient** – share interaction  
- **John the Ripper** – password cracking  
- **Hydra** – authentication brute-force testing  
- **Gobuster** – directory enumeration  
- **Nikto** – web misconfiguration scanning  
- **WhatWeb** – web fingerprinting  
- **curl** – manual HTTP interaction  

---

## 🧠 High-Level Attack Flow

| Step | Phase |
|------|------------------------------|
| 1 | Network Reconnaissance |
| 2 | Service Enumeration |
| 3 | Vulnerability Identification |
| 4 | Controlled Exploitation |
| 5 | Post-Exploitation Analysis |
| 6 | Risk Evaluation & Reporting |


---

## 🖥️ Target 1: Windows 7 System (192.168.2.100)

### Key Findings (Summary)

- SMB exposed with legacy configuration  
- MS17-010 (EternalBlue) vulnerable  
- Successful remote SYSTEM-level access  
- NTLM hashes extracted  
- Weak user password cracked  
- SMB message signing disabled  
- Anonymous SMB sessions partially allowed  

### Impact Summary

- Full system compromise possible  
- Credential theft feasible  
- Lateral movement risk  
- Weak authentication enforcement  

---

## 🐧 Target 2: Linux Server (192.168.2.101)

### Key Findings (Summary)

- Outdated Apache, PHP, and Samba services  
- Anonymous SMB share accessible  
- Directory listing enabled  
- Username disclosure via web pages  
- Weak credentials brute-forced  
- Missing security headers  
- TRACE HTTP method enabled  

### Impact Summary

- Unauthorized file access  
- Information disclosure  
- Authentication bypass through weak credentials  
- Increased exposure to web-based attacks  

---

## 🔎 Key Security Weakness Categories Identified

- Outdated and unpatched software  
- Weak authentication mechanisms  
- Insecure SMB configuration  
- Anonymous access exposure  
- Missing security headers  
- Poor credential hygiene  
- Insufficient monitoring and logging  
- Lack of brute-force protections  

---

## 📊 Assessment Outcome Summary

| Category | Result |
|--------|--------|
| Reconnaissance | Successful |
| Service Enumeration | Successful |
| Vulnerability Identification | Successful |
| Exploitation | Successful (lab-controlled) |
| Privilege Escalation | Demonstrated |
| Credential Exposure | Observed |
| Defensive Gaps Identified | Yes |
| Documentation Completed | Yes |

---

## 🧠 Key Learning Outcomes

- Practical understanding of internal network pentesting  
- Real-world exploitation flow from recon → access → impact  
- Importance of patch management  
- Dangers of weak authentication  
- Risks of exposed SMB and web services  
- How attackers chain small misconfigurations  
- Writing professional security documentation  

---


---

## ⚠️ Ethical Notice

This project was performed **strictly in a controlled lab environment** created for educational purposes.

- No real systems were targeted  
- No unauthorized access was performed  
- No external networks were involved  
- All findings are documented for learning and defense  

---

## 📘 Why This Project Matters

This project demonstrates:

- Practical penetration testing methodology  
- Understanding of real-world attack chains  
- Ability to analyze misconfigurations critically  
- Strong documentation and reporting skills  
- Awareness of defensive remediation  
- Readiness for SOC / VAPT / Security Analyst roles  

---

📌 *This repository forms part of my cybersecurity portfolio and documents hands-on experience in internal penetration testing, vulnerability assessment, and security analysis.*


