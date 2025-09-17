# Network Attack Incident Report

## 📌 Overview
Incident report documenting a **network attack**, including traffic analysis, indicators of compromise (IoCs), impact assessment, and mitigation measures.  
This case study demonstrates how abnormal network traffic can disrupt business operations and highlights defensive measures taken during the incident.

---

## 📝 Scenario
You work as a security analyst for a **travel agency** that advertises sales and promotions on the company’s website.  
Employees regularly access the sales webpage to search for vacation packages for customers.  

One afternoon, you receive an automated alert from the monitoring system about a problem with the **web server**.  
When you attempt to access the company’s website, you receive a **connection timeout error**.  

---

## 🔎 Investigation
- A **packet sniffer** was used to capture traffic to and from the web server.  
- Observations:
  - A large number of **TCP SYN requests** were detected.  
  - Requests were coming from an **unfamiliar IP address**.  
  - The **web server was overwhelmed** and unable to respond to the excessive SYN requests.  
- This behavior is consistent with a **SYN flood attack**, a type of **Denial of Service (DoS)** attack.  

---

## ⚠️ Indicators of Compromise (IoCs)
- Unusually high volume of **TCP SYN packets** from a single IP address.  
- **Web server unresponsiveness** (connection timeout for legitimate users).  
- Automated alert triggered by the **monitoring system**.  

---

## 📉 Impact Assessment
- The company’s **web server was unable to respond** to legitimate requests.  
- Employees could not access the sales webpage, affecting **business operations**.  
- Customer-facing website downtime reduced accessibility to promotions and vacation packages.  

---

## 🛡️ Mitigation Measures
- Temporarily took the **server offline** to allow recovery.  
- Configured the **firewall** to block the attacking IP address.  
- Recognized that IP blocking alone is **not a long-term solution**, since attackers can **spoof IP addresses**.  
- Escalated the incident to management to discuss stronger countermeasures.  

---

## 📂 Repository Contents
- `reports/analysis_report.md` → Detailed incident analysis  

---

## 📖 Next Steps
- Inform management of the discovered **SYN flood attack**.  
- Explore **advanced defenses** such as:
  - SYN cookies  
  - Rate limiting  
  - Intrusion Prevention Systems (IPS)  
  - Cloud-based DDoS protection services  

---
