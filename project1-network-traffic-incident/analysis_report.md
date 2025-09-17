# Cybersecurity Incident Report: Network Traffic Analysis

---

## 📝 Part 1: Summary of the Problem
During packet analysis using `tcpdump`, the following observations were made:

- As part of the **DNS protocol**, the browser used **UDP** to contact the DNS server in order to retrieve the IP address for the domain `yummyrecipesforme.com`.  
- The DNS server responded with **ICMP error messages** indicating issues contacting the server.  
- In the logs:
  - The **UDP messages** from the browser to the DNS server are shown in the first two lines of each log entry.  
  - The **ICMP error messages** are displayed in the third and fourth lines of each log entry, containing:  
    ```
    udp port 53 unreachable
    ```
- Since **port 53** is associated with DNS protocol traffic, this indicates an issue with the DNS server.  
- Additional evidence from the logs:
  - The **plus sign (+)** after the query identification number `35084` highlights flagged conditions with the UDP message.  
  - The **“A?”** symbol indicates flags related to DNS protocol operations.  
- Together, these observations strongly suggest that the DNS server is not responding to queries.  

---

## 🔎 Part 2: Analysis and Likely Cause
- **Incident time:** Today at **1:24 p.m.**  
- **Customer impact:** Users attempting to access `yummyrecipesforme.com` reported the error: destination port unreachable

- **Investigation steps:**
1. Customers’ issue was reproduced internally.  
2. Packet sniffing was conducted using `tcpdump`.  
3. The log confirmed that **DNS port 53 was unreachable**.  

- **Possible causes:**
1. **DNS server outage** – The server may have been taken offline due to a misconfiguration or failure.  
2. **Firewall blocking** – Traffic to port 53 may be blocked by a firewall rule, preventing DNS queries from succeeding.  
3. **Denial of Service (DoS) attack** – The DNS server may have been targeted, making it unresponsive to legitimate requests.  

---

## ✅ Conclusion
The root of the issue lies in **DNS resolution failure** caused by UDP port 53 being unreachable. Without a functioning DNS service, customers cannot resolve the domain name `yummyrecipesforme.com` and therefore cannot access the website.  

The next steps include:  
- Verifying the **status of the DNS server**.  
- Reviewing **firewall rules** to confirm if port 53 traffic is blocked.  
- Checking for **signs of a DoS attack** or other malicious activity.  

---
