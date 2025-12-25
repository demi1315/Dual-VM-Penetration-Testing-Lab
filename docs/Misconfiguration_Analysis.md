# ⚠️ Misconfiguration Analysis – Dual VM Penetration Test

This document analyzes the security misconfigurations discovered during the assessment and explains **why they are dangerous**, how they arise, and what risks they introduce in real environments.

The goal is to understand systemic weaknesses rather than simply list exploits.

---

## 🔐 Windows Host Misconfigurations (192.168.2.100)

### 1. Outdated Operating System (Windows 7)

The system was running an unsupported version of Windows, making it vulnerable to publicly known exploits.

**Risk:**
- Exposure to critical remote code execution vulnerabilities  
- Lack of vendor security updates  
- High likelihood of compromise  

---

### 2. SMB Service Exposure

Ports related to SMB were openly accessible, allowing enumeration and exploitation.

**Risk:**
- Increased attack surface  
- Exposure to legacy protocol weaknesses  
- Susceptibility to relay and replay attacks  

---

### 3. MS17-010 (EternalBlue) Vulnerability

The system was vulnerable to MS17-010, enabling remote code execution.

**Impact:**
- Full SYSTEM-level compromise  
- No authentication required  
- Complete host takeover  

---

### 4. Credential Extraction Risk

Post-compromise access allowed extraction of NTLM password hashes.

**Impact:**
- Offline password cracking  
- Credential reuse across systems  
- Potential lateral movement  

---

### 5. Weak Password Practices

Recovered credentials were weak and easily crackable using common wordlists.

**Impact:**
- Enables brute-force or credential stuffing attacks  
- Indicates lack of password policy enforcement  

---

## 🐧 Linux Server Misconfigurations (192.168.2.101)

### 1. Outdated Software Stack

The system used outdated versions of Apache, PHP, and Samba.

**Impact:**
- Exposure to known CVEs  
- Increased likelihood of remote exploitation  

---

### 2. Anonymous SMB Access

SMB shares were accessible without authentication.

**Impact:**
- Unauthorized file access  
- Information disclosure  
- Enumeration of internal resources  

---

### 3. Directory Listing Enabled

Web directories were indexable and exposed internal files.

**Impact:**
- Leakage of internal documents  
- Easier reconnaissance for attackers  

---

### 4. Username Disclosure via Web Content

Usernames were visible directly in HTML source.

**Impact:**
- Enables targeted brute-force attacks  
- Reduces attacker guesswork  

---

### 5. Weak Authentication Controls

The web application accepted weak credentials and lacked protections.

**Impact:**
- Susceptible to brute-force attacks  
- No rate limiting or lockout mechanisms  

---

### 6. Missing Security Headers

Critical HTTP headers were absent.

**Impact:**
- Exposure to clickjacking  
- Increased XSS-related risks  
- Poor browser-level protection  

---

## 🧠 Root Cause Analysis

Across both machines, the root causes were consistent:

- Use of outdated operating systems  
- Poor patch management  
- Weak password policies  
- Misconfigured access controls  
- Lack of defense-in-depth  
- Insufficient monitoring  

These issues are common in poorly maintained enterprise environments.

---

## 🔎 Summary

The vulnerabilities observed are not advanced zero-days; they are **fundamental configuration failures**. Their combination enables full compromise with minimal effort, reinforcing why baseline security hygiene is critical.
