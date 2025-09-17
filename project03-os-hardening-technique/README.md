# Applying OS Hardening Techniques: Security Incident Analysis

## 📌 Overview
This repository documents the application of **OS hardening techniques** to strengthen system security, reduce vulnerabilities, and enforce best practices.  

It includes an analysis of a **malicious file download incident** via the HTTP protocol and recommendations for preventing brute force attacks.

---

## 🔎 Summary of Incident
- The website `yummyrecipesforme.com` prompted users to download a malicious file disguised as a recipe browser update.  
- Users’ computers were compromised, and the website owner’s admin account was locked out.  
- Packet captures (`tcpdump`) confirmed the use of **HTTP protocol** to transport malicious files and subsequent redirection to `greatrecipesforme.com`.  

---

## 🛡️ OS Hardening & Mitigation
- Implemented **Multi-Factor Authentication (MFA)** to prevent unauthorized access.  
- Enforced **strong password policies** and frequent updates to prevent brute force attacks.  
- Performed **firewall maintenance** to block suspicious traffic and reduce exposure to network attacks.  

---

## 📂 Repository Contents
- `reports/analysis_report.md` → Detailed incident analysis, traffic logs interpretation, and remediation steps.  
- `tcpdump_logs.png` → Captured network traffic logs showing HTTP requests and malicious file downloads.  

---

## 📖 References
- TCP/IP and HTTP Protocol Analysis  
- OS Hardening Best Practices  
- Brute Force Attack Mitigation Techniques  
