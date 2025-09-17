# Incident Response Analysis Report

---

## 📌 Summary
A phishing alert was triggered after an employee downloaded a suspicious file.  
Upon investigation, the file’s hash was verified as **malicious**.  
The SOC analyst followed the organization’s **incident response playbook** to contain and resolve the incident.

---

## 🔎 Investigation Steps
1. **Alert received** → Phishing email reported in SIEM  
2. **File hash lookup** → Verified malicious using threat intelligence feeds  
3. **User interview** → Employee confirmed opening the email attachment  
4. **Scope check** → Ensured no other endpoints downloaded the same file  

---

## 🛡️ Response Actions
- **Containment:** Isolated the employee’s computer from the network  
- **Eradication:** Deleted the malicious file & terminated related processes  
- **Recovery:** Restored clean system state and reconnected device to network  
- **Ticket update:** Documented investigation details, response actions, and outcome  

---

## ⚠️ Recommendations
- Enhance **email gateway filtering** and **attachment sandboxing**  
- Conduct **ongoing phishing awareness training** for employees  
- Automate **hash validation** in SOC workflows to reduce response time  
- Regularly **update playbooks** to reflect new phishing tactics  

---

## ✅ Conclusion
The phishing attempt was successfully contained and remediated without further compromise.  
Using a structured **incident response playbook** ensured rapid action and minimized risk to the organization.  
