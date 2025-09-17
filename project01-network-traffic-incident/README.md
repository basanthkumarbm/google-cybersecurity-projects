# Network Traffic Incident Report

## 📌 Overview
Incident report analyzing **network traffic anomalies**, highlighting a **blocked port** and identifying the **root cause**.  
The investigation focuses on **DNS** and **ICMP traffic** using data captured with a network protocol analyzer tool (`tcpdump`).  

---

## 📝 Scenario
As a cybersecurity analyst at an IT services company, you received reports from multiple customers that they could not access the client’s website: www.yummyrecipesforme.com

Error: "Destination port unreachable"

Attempted to access the site yourself and encountered the same issue.

---

## 🔎 Investigation
- Used `tcpdump` to analyze network traffic during the failed webpage load.  
- Browser behavior:
  1. Sent a **DNS query** (UDP/53) to resolve the domain name.  
  2. Received **ICMP error messages** stating:  
     ```
     udp port 53 unreachable
     ```
  3. Since DNS resolution failed, the **HTTPS request** to the web server could not proceed.  

---

## 📡 Protocol Analysis
- **DNS (UDP/53):** Used to resolve the domain name into an IP address.  
- **ICMP:** Returned the error message indicating the DNS port was blocked/unreachable.  
- **IP (Internet Layer, TCP/IP Model):** Formatted the packets into datagrams, providing insight into traffic anomalies.  

---

## ✅ Root Cause
The affected protocol was **DNS over UDP (Port 53)**.  
Because the DNS server’s port was blocked or unreachable, the browser could not resolve the domain name, resulting in failure to access the website.  

---

## 🛡️ Key Takeaways
- Monitoring DNS and ICMP traffic is essential for diagnosing connectivity issues.  
- ICMP error messages help identify the exact reason for failed communication.  
- Misconfigured or blocked ports can cause widespread service disruptions.  

---

## 📂 Repository Contents
- `analysis_report.md` → Detailed incident analysis  
- `traffic_screenshot.png` → Screenshot of captured network traffic  

---

## 👀 How to View This Repo
1. **Start with [README.md]** (this file) for a quick summary.  
2. Open `analysis_report.md` for the **full detailed report**.  
3. Review `traffic_screenshot.png` to **visualize captured traffic flow**.  
4. Explore `tcpdump_logs.txt` if you want to see the **raw packet captures**.  

---

## 📖 References
- TCP/IP Model – Internet Layer  
- DNS Protocol (UDP/53)  
- ICMP Error Messaging  
