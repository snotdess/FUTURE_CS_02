# Security Monitoring and Incident Response with Splunk

## 📌 Overview  
This project simulates the role of a SOC (Security Operations Center) analyst using **Splunk** as a SIEM tool. The focus was on monitoring security events, detecting suspicious activities, classifying incidents, and simulating incident response workflows.  

## ⚡ Activities Performed  
-  **Splunk Setup & Exploration**: Configured Splunk for log ingestion, searching, and dashboard visualization.  
-  **Suspicious Event Detection**: Used **SPL (Search Processing Language)** queries to filter and analyze abnormal activities.  
-  **Alert Actions**: Triggered alert actions in Splunk to simulate real-time SOC responses.  
-  **Incident Reporting**: Documented findings with timelines, impacts, and recommended responses.  
-  **Escalation**: Configured email alerts to automatically escalate critical events to the **Tier 2 SOC team**.  

## 🛡️ Findings  

### 1️⃣ Multiple Failed Login Attempts  
- **Description**: Several failed login attempts were detected from multiple external IP addresses.  
- **Risk**: Possible brute-force or unauthorized access attempt.  
- **Response**: Classified as **High Priority**; alert actions triggered.  
- **Recommendation**: Block suspicious IPs, enforce MFA, and monitor authentication logs.  

---

### 2️⃣ Malware Activity Detection  
- **Description**: SPL queries revealed events indicating ransomware, rootkits, trojans, worms, and spyware.  
- **Risk**: Potential system compromise, persistence, and data theft.  
- **Response**: Classified as **High Priority**; alert actions configured.  
- **Recommendation**: Isolate affected hosts, perform malware scans, and update endpoint protections.  

---

### 3️⃣ Suspicious Host Activity (IP: 203.0.113.77)  
- **Description**: Logs revealed a sequence of events — successful login, file access, and subsequent malware detection.  
- **Risk**: Host compromise with risk of internal network propagation and data exfiltration.  
- **Response**: Classified as **High Priority**; Splunk email alert created and escalated to **Tier 2 SOC team**.  
- **Recommendation**: Isolate the host, conduct forensic analysis, reset credentials, and monitor for persistence.  

## 📤 Alert Reporting  
An **email alert** was configured in Splunk to notify the **Tier 2 SOC team** of the suspicious host activity (`203.0.113.77`). This ensured timely escalation of critical events for deeper investigation and remediation.  
