# NIST CSF Incident Response: DDoS Attack Analysis

## 📌 Overview
This repository documents the application of the **NIST Cybersecurity Framework (CSF)** to structure and execute an effective incident response process for a DDoS attack at a multimedia company.  

The CSF provides a scalable approach to identifying, protecting, detecting, responding, and recovering from cybersecurity incidents.

---

## 🔎 Incident Summary
- The company experienced a **DDoS attack** through a flood of incoming **ICMP packets**, causing network services to stop responding for **two hours**.  
- Internal network traffic was disrupted and critical network services were affected.  
- The cybersecurity team responded by blocking incoming ICMP packets, isolating affected systems, and restoring critical network services.  

---

## 🛡️ Remediation Measures Implemented
- New **firewall rules** to limit the rate of incoming ICMP packets.  
- **Source IP verification** on the firewall to detect spoofed IP addresses.  
- Deployment of **network monitoring software** to detect abnormal traffic patterns.  
- Implementation of an **IDS/IPS system** to filter suspicious ICMP traffic.  

---

## 📂 Repository Contents
- `analysis_report.md` → Detailed incident report and NIST CSF analysis.  

---

## 📖 References
- NIST Cybersecurity Framework (CSF)  
- DDoS Attack Mitigation Techniques  
- Network Monitoring and Incident Response Best Practices  
