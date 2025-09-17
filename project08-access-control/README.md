# Access Control: Incident Analysis and Mitigation

## 📌 Overview
This repository demonstrates how **access control mechanisms** can be designed and implemented to manage user permissions and protect sensitive resources.  

Access controls reduce security risks by ensuring only authorized users can access critical systems. They combine:
- **Authentication** → Verifies identity  
- **Authorization** → Defines permissions and limits  

---

## 🏢 Scenario
A growing business experienced an incident where an unauthorized deposit was attempted to an unknown bank account.  

The investigation revealed:
- An administrator account belonging to a **former contractor** was still active.  
- The account was used years after the contract ended to access payroll systems.  

---

## 📂 Repository Contents
- `reports/analysis_report.md` → Incident analysis, issues found, and recommendations  
- `event_accounting.pdf` → Event accounting log with details of the incident  

---

## 🛡️ Key Recommendations
- Expire **inactive accounts** within 30 days  
- Apply **least privilege access** for contractors and temporary staff  
- Enable **multi-factor authentication (MFA)** for all sensitive systems  

---

## 📖 References
- NIST SP 800-53: Access Control (AC)  
- CIS Controls v8: Access Control Management  
