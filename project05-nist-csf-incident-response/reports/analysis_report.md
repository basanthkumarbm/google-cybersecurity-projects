# NIST CSF Incident Response Analysis Report

---

## 🔎 Summary of the Incident
- All network services stopped responding due to a **distributed denial of service (DDoS) attack** via **ICMP flooding**.  
- The cybersecurity team responded by blocking the attack, stopping non-critical services, and restoring critical services.  
- The attack exploited an **unconfigured firewall**, allowing overwhelming traffic into the network.

---

## 🛡️ Identify
- **Threat actor:** Malicious actor(s) targeting the company’s internal network.  
- **Impact:** Entire internal network affected; critical network resources needed immediate restoration.  
- **Risk assessment:** Identified ICMP flood vulnerability through regular audits and internal network monitoring.

---

## 🔒 Protect
- Implemented a **firewall rule** to limit incoming ICMP packet rates.  
- Deployed an **IDS/IPS system** to filter suspicious ICMP traffic.  
- Policies and procedures updated to reduce vulnerability to future DDoS attacks.

---

## 👀 Detect
- Configured **source IP verification** on the firewall to detect spoofed addresses.  
- Deployed **network monitoring software** to identify abnormal traffic patterns.  
- Continuous monitoring enhances speed and accuracy of incident detection.

---

## ⚡ Respond
- Isolate affected systems to prevent further disruption.  
- Restore critical systems and services impacted by the DDoS attack.  
- Analyze network logs for suspicious activity.  
- Report incidents to upper management and legal authorities as applicable.

---

## 🔄 Recover
- Restore access to network services to normal operational state.  
- Block external ICMP flood attacks at the firewall for future prevention.  
- Stop all non-critical services temporarily to reduce internal network load.  
- Prioritize restoration of critical services first.  
- Bring non-critical systems back online after the threat subsides.

---

## ✅ Conclusion
The DDoS attack via ICMP flooding exposed vulnerabilities in firewall configuration and network monitoring.  

Using the **NIST CSF framework**, the cybersecurity team successfully identified, protected, detected, responded to, and recovered from the incident.  

Future mitigation measures include:
- Continuous monitoring of network traffic  
- Firewall hardening to prevent ICMP floods  
- IDS/IPS configuration updates to detect abnormal patterns early  
