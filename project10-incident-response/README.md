# Incident Response: Phishing Alert Playbook

## 📌 Overview
This repository contains an **incident response workflow** designed to handle phishing alerts effectively.  
It demonstrates how to streamline **detection, investigation, and remediation** using playbooks, alert management, and ticketing systems.

---

## 🏢 Scenario
- Role: Level-one SOC analyst at a financial services company  
- Incident: Employee received a **phishing email** with a malicious file attachment  
- Action: File hash confirmed as malicious → followed incident response playbook to investigate & resolve alert  

---

## 📂 Repository Contents
- `reports/analysis_report.md` → Incident response playbook walkthrough & investigation steps
- `alert_ticket.pdf` → Completed alert ticket with investigation details and resolution notes  

---

## ⚠️ Key Workflow Steps
1. **Detection** – Phishing email alert received  
2. **Investigation** – File hash checked against threat intel → confirmed malicious  
3. **Containment** – Isolated affected workstation to stop spread  
4. **Eradication** – Removed malicious file and cleaned system  
5. **Recovery** – Restored system functionality, verified no persistence mechanisms  
6. **Lessons Learned** – Updated ticket with findings & improved phishing detection rules  

---

## 🛡️ Recommendations
- Enforce **email filtering & sandboxing** for attachments  
- Provide **employee phishing awareness training**  
- Automate **hash lookups** in the SIEM for faster triage  
- Maintain detailed **incident response playbooks** for SOC analysts  

---

## 📖 References
- NIST SP 800-61r2 – Computer Security Incident Handling Guide  
- MITRE ATT&CK Framework – Initial Access: Phishing (T1566)  
