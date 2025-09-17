# OS Hardening Incident Analysis Report

---

## 🔎 Section 1: Network Protocol Involved
- The protocol involved in the incident is **HTTP** (Hypertext Transfer Protocol).  
- Accessing the website `yummyrecipesforme.com` used HTTP traffic as confirmed by `tcpdump` logs.  
- The malicious file was delivered to users’ computers over **HTTP at the application layer**.

---

## ⚠️ Section 2: Incident Documentation
- Several users reported that visiting the website prompted a download of a file claiming to provide access to new recipes.  
- Users’ computers slowed down after executing the file.  
- The website owner was **locked out** of their admin account.  

**Investigation steps:**
1. Analyst used a **sandbox environment** to access the website safely.  
2. Ran **tcpdump** to capture network traffic.  
3. Observed:
   - Initial HTTP requests to `yummyrecipesforme.com`.  
   - Prompt to download a malicious file.
   - Redirects to a new domain: `greatrecipesforme.com`.  
4. Analysis of the source code and downloaded file revealed:
   - The website was **compromised** to prompt malicious downloads.  
   - The admin account was likely accessed using a **brute force attack**.

**Captured traffic highlights:**
```text
14:18:36.786501 IP your.machine.36086 > yummyrecipesforme.com.http: Flags [S], ...
14:20:32.192571 IP your.machine.52444 > dns.google.domain: 21899+ A? greatrecipesforme.com.
14:25:29.576493 IP your.machine.56378 > greatrecipesforme.com.http: Flags [S], ...
```
Traffic logs show HTTP requests and redirects to malicious domains.

## 🛡️ Section 3: Remediation for Brute Force Attacks

- **Disallow reuse of previous passwords**  
  Prevents attackers from using default or old passwords.

- **Require frequent password updates**  
  Limits exposure if credentials are leaked.

- **Implement Multi-Factor Authentication (MFA)**  
  - Requires a password + one-time passcode (OTP) for authentication.  
  - Prevents unauthorized access even if the password is compromised.

---

## 🔧 Section 4: OS Hardening Tools and Methods

- **Multi-Factor Authentication (MFA)** – Adds an extra layer of authentication.  
- **Strong Password Policies** – Enforce complex passwords, limit failed login attempts, and require frequent changes.  
- **Firewall Maintenance** – Regular updates to block suspicious traffic, prevent DoS/DDoS attacks, and control inbound/outbound traffic.

---

## 📖 Section 5: Recommendations

- MFA and strong passwords make brute force attacks more difficult.  
- Regular firewall checks help prevent unauthorized access and network attacks.  
- Continuous monitoring of HTTP traffic can detect malicious file downloads or redirection to phishing websites.

---

## ✅ Conclusion

The incident demonstrates how **compromised websites** can deliver malicious files via **HTTP**, and how attackers can gain admin access using brute force attacks.  

Applying **OS hardening techniques** such as MFA, strong password policies, and firewall maintenance reduces vulnerabilities and strengthens overall system security.
