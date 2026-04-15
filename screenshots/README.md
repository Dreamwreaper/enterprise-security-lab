# Enterprise Web Application Security Lab

## Overview
This project demonstrates hands-on web application security testing, traffic analysis, and SIEM-based detection using a controlled lab environment.

The lab was built using OWASP Juice Shop, with traffic captured via Burp Suite and analyzed in Splunk to simulate real-world security monitoring.

---

## Objectives
- Deploy a vulnerable web application locally
- Capture and analyze HTTP traffic
- Identify suspicious patterns and behaviors
- Develop detection strategies using SIEM tools
- Map findings to security best practices

---

## Tools Used
- OWASP Juice Shop
- Burp Suite Community Edition
- Splunk Enterprise
- Docker / WSL2

---

## Lab Workflow
1. Deploy application locally  
2. Generate traffic and simulate attack scenarios  
3. Capture HTTP requests using Burp Suite  
4. Export logs and ingest into Splunk  
5. Develop detection queries  

---

## Key Scenario (Injection Test)

Test input:
' OR 1=1 -- admin

This demonstrates how malicious patterns appear in web traffic and how they can be detected in logs.

---

# Enterprise Web Application Security Lab

## Overview
This project demonstrates hands-on web application security testing, traffic analysis, and SIEM-based detection using OWASP Juice Shop, Burp Suite, and Splunk.

The goal was to simulate real-world attack scenarios, capture HTTP traffic, and develop detection strategies aligned with security operations and compliance frameworks.

---

## Tools Used

- OWASP Juice Shop  
- Burp Suite Community Edition  
- Splunk Enterprise  
- Docker / WSL2  

---

## Lab Workflow

1. Deployed OWASP Juice Shop locally  
2. Generated user traffic and simulated attack scenarios  
3. Captured HTTP requests using Burp Suite  
4. Exported logs and ingested them into Splunk  
5. Built detection queries to identify suspicious activity  

---

## SIEM Detection Example

```spl
index=main ("OR 1=1" OR "admin")
